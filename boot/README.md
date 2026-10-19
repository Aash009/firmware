# Boot and update (SI-P-03, Class C)

Two parts, one software item:

| Folder | Image | Purpose |
|---|---|---|
| loader/ | Separate boot image, own signing key, own tag `boot/vX.Y.Z` | Second-stage boot: signature check of the active bank, dual-bank rollback |
| update_client/ | Linked into the application image | Receives a signed image over USB and writes the inactive bank |

Rules:
- loader/ includes nothing from application/, system/ or driver/ (tools/ci/layer_rules.yaml).
  It calls STM32U5 HAL/LL directly, so an application driver change never rebuilds the boot image.
- A rebuilt application must leave the boot image byte-identical; the release record cites both hashes.
- The immutable first stage (OEMiROT pattern) is ST-supplied and is tracked as SOUP (OPEN-020).

Source: FAD §14.1–14.4, FAD Table 8 row 3.
