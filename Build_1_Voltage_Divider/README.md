# Build 1: Voltage Divider with Load

## Overview
Built a voltage divider circuit to understand how loading effects real circuits compared to theory.

## Theory
For a voltage divider with no load:
- Formula: V_out = V_in × (R2 / R1 + R2)
- Calculation: V_out = 5V × (10kΩ / 20kΩ) = 2.5V

With a 1kΩ load resistor in parallel on R2:
- Parallel resistance: (10kΩ × 1kΩ) / (10kΩ + 1kΩ) = 909Ω
- New calculation: V_out = 5V × (909Ω / 10,909Ω) = 0.417V

## Parts Used
- 2x 10kΩ resistor (1/2W)
- 1x 1kΩ resistor (1/2W)
- Power supply (5V)
- Breadboard
- Multimeter
- Jumper wires

## Measurements

| Condition | Measured | Expected | Error |
|-----------|----------|----------|-------|
| No load | 2.5V | 2.5V | 0% |
| With 1kΩ load | 0.420V | 0.417V | 0.7% |

## What I Learned
This project showed that real circuits behave differently from theory when there's a load. The 1kΩ resistor acted as a load, drawing current and changing the voltage divider ratio. My measurements matched theory within 1%, which proves that even with real components, the math works, just have to account for loading effects in circuit design.

## Photos
[See images: circuit setup, no load multimeter reading, with load circuit, with load multimeter reading]
