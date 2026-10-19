# update_client

Status: design placeholder, excluded from compilation and verification counts.
Software item: SI-P-03 Update client and bootloader (Class C per software_items.yaml).
Build variants: TREPTOFLO, INSUFLO.
Responsibility: Receive a signed image over the USB service port, write it to the inactive bank, verify it and request the bank swap. Linked into the application image; owned by the boot item.
Allocation source: FAD §14.2 update sequence; FAD Table 19 (USB-C)
Legacy (L496 project): DFU_application, rewrite (different MCU, dual-bank flash and signing). Clause 4.4 legacy assessment or re-development is required before any L496 code is copied (docs/LEGACY_PORTING_MAP.md).
inc/: public API; src/: implementation; test/: unit verification.
Requirements (SR-P-###), unit design (SU-P-###), timing and fault behaviour: TBD.
