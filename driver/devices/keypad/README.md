# keypad

Status: design placeholder, excluded from compilation and verification counts.
Software item: SI-P-06 GUI (Class B per software_items.yaml).
Build variants: TREPTOFLO, INSUFLO.
Responsibility: Membrane keypad direct GPIO scan with debounce.
Hardware: Custom FFC membrane keypad; GPIO (HAD Table 8)
Allocation source: FAD Table 19 (keypad -> GUI input handler)
Legacy (L496 project): Encoder_button_limit_driver, button part only. The retract limit / contact datum is read by the SAFETY MCU (FAD Table 19) and moves to the SAFETY project. Clause 4.4 legacy assessment or re-development is required before any L496 code is copied (docs/LEGACY_PORTING_MAP.md).
inc/: public API; src/: implementation; test/: unit verification.
Requirements (SR-P-###), unit design (SU-P-###), timing and fault behaviour: TBD.
