# loader

Status: design placeholder, excluded from compilation and verification counts.
Software item: SI-P-03 Update client and bootloader (Class C per software_items.yaml).
Build variants: TREPTOFLO, INSUFLO.
Responsibility: Second-stage boot: verify the active bank signature (ECDSA P-256), boot it, and switch to the other bank after two consecutive failed boots. Separate image with its own signing and release tag (boot/vX.Y.Z); does not link application, system or driver code.
Allocation source: FAD §14.1 boot chain; FAD Table 8 row 3
Open: The immutable first stage (OEMiROT) is ST-supplied code: add it to the SOUP manifest and FAD Table 20 (OPEN-020).
inc/: public API; src/: implementation; test/: unit verification.
Requirements (SR-P-###), unit design (SU-P-###), timing and fault behaviour: TBD.
