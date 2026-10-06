# FT-891 macOS controller

## Goal
Native macOS app to control a Yaesu FT-891 via USB CAT.
Features (v1): [frequency read/set, mode, band, VFO A/B, S-meter, PTT]

## Stack
[Swift + SwiftUI] / [Python + ...]
macOS [version], Apple Silicon / Intel: [Apple Silicon]

## Hardware
- Port: /dev/cu.[...] (Enhanced COM port)
- CAT rate: [4800/9600/...] baud, 8N1 [9600]
- CAT reference: /docs/

## Rules
- Use only commands documented in /docs; cite the command when implementing.
- Serial layer separate from UI; testable without the radio (mock port).
- Small steps; I test against the real radio before moving on.