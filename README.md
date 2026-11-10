# 2S Battery Charger

USB-C powered charger for a 2-cell (2S) Li-ion battery pack, designed in
KiCad. The board requests a higher voltage from a USB-C Power Delivery
source (CH224K), charges the pack with a switching charger (MP26123) and
balances the two cells with a bleed-resistor circuit.

## Main components

| Ref | Part | Role |
|-----|------|------|
| J1 | SS-52400-002 | USB-C connector |
| F1 | 0ZCG0260FF2C | Resettable fuse on VBUS |
| U2 | CH224K | USB-C PD sink controller |
| U3 | USBLC6-2SC6 | ESD protection for USB data lines |
| U1 | MP26123 | 2-cell Li-ion switching charger |
| L1 | 4.7 µH | Buck inductor |
| D1, D4 | SS34 | Schottky diodes |
| R9 | 100 mΩ | Charge current sense |
| D2, D3 | LED | Charge status (CHGOK, ACOK) |
| SW1 | Push button | Connected to the EN pin of the charger |
| IC1, IC2 | HY2213-BB3A | Per-cell voltage detection for balancing |
| Q1, Q2 | AO3400A | Balancing switches |
| R13, R14 | 62 Ω | Balancing (bleed) resistors |
| J2 | 1x03 pin header | Battery: VBAT, BAT_MID, GND |

Full bill of materials: [`2S-BATTERY-CHARGER.csv`](2S-BATTERY-CHARGER.csv).
