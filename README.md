# Magic Wand PCB

![3D View of Magic Wand PCB](Docs/image_2026-06-14_18-38-41.jpg)

## Overview
This project is a custom printed circuit board designed in Altium Circuit Maker that functions as a "Magic Wand". By waving the board in the air, the sequential flashing of the LEDs creates a Persistence of Vision (POV) effect. 

## Circuit Details
* **Clock Signal:** A 555 timer generates an adjustable clock pulse (controlled via onboard potentiometers).
* **Binary Counter:** An SN74HC161N 4-bit counter tracks the pulses.
* **Decoder/Driver:** A CD74HC138E 3-to-8 decoder interprets the binary count to sequentially drive 8 LEDs.

## Project Structure
* **Docs**: Contains schematic: ![Schematic](Docs/image_2026-06-14_18-36-40.jpg) and PCB routing layout: ![Layout](Docs/image_2026-06-14_18-46-59.jpg)
* **Hardware**: Contains the Altium Circuit Maker design files and BOM (Bill of Materials).
* **Manufacturing**: Contains generated Gerber and NC Drill files ready for fabrication.

## Bill of Materials (BOM)

| Comment       | Description                                                                                       | Designator                     | Quantity |
|:--------------|:--------------------------------------------------------------------------------------------------|:-------------------------------|---------:|
| Keystone 2466 | Battery holder, AAA, 1 cell, PC mount                                                             | B1, B2, B3                     |        3 |
| 47uf          | Electrolytic capacitor Radial lead 2.5 mm 10 µF 16 V 20 % (Ø) 4 mm Panasonic EEA-GA1C100H 1 pc(s) | C1                             |        1 |
| 0.1 uf        | SERVAL Cap Lent 104                                                                               | C2, C3, C4, C5, C6             |        5 |
| 5MM LED WHT   | LED Uni-Color Green 2-Pin T-1 3/4 Bulk                                                            | D1                             |        1 |
| 5MM LED GRN   | LED Uni-Color Green 2-Pin T-1 3/4 Bulk                                                            | D2, D3, D4, D5, D6, D7, D8     |        7 |
| Switch On/Off | Slide Switch, 500 V, -20 to 70 degC, 3-Pin THD, RoHS                                              | ON                             |        1 |
| 100K          | Res Cermet Trimmer 500 Ohm 10% 1/2W 1(Elec)/1(Mech)Turn 2.6mm (7 X 7 X 5.8mm) Pin Thru-Hole Bulk  | PotA, PotB                     |        2 |
| 100 ohm       | Res Carbon Film 1K Ohm 5% 1/4W -400ppm/°C to 0ppm/°C Conformal AXL Thru-Hole T/R                  | R1, R2, R3, R4, R5, R6, R7, R8 |        8 |
| LMC555CN/NOPB | CMOS Timer, 8-pin MDIP, Pb-Free                                                                   | U1                             |        1 |
| TI SN74HC393N | Texas Instruments - SN74HC393N - Counter/Divider Dual 4-Bit Binary UP 14-Pin PDIP Tube            | U2, U3                         |        2 |
| TI CD74HC138E | TEXAS INSTRUMENTS   CD74HC138E   Logic Type:Decoder / Demultiplexer                               | U4                             |        1 |
