# ZX Spectrum +2 (Grey) External Tape Input PCB

This is a simple PCB layout for building circuit designed by
[JoulesperCoulomb](https://youtu.be/qUIv-A_DOc0?t=1213), please
watch the video for all the details.

![PCB](https://github.com/jameshpdp/Spectrum-2-TapeIn/blob/main/images/Spectrum%2B2-TapeIn.png)

Board size 40mm x 30mm. Gerber files under `export/`, original KiCad project under
`Spectrum+2-TapeIn.KiCad/`.

## Building

Building this circuit shold be straghtforward with one exception. It is recommended to solder wires directly to the PCB1 pads and avoid using pin header there.

NOTE: While PCB1 connector footprint allows for soldering KK 254 / KF 2510  pin header, great care should be taken to solder those correctly. The problem is not the pin header itself, but the cable you need to use to connect it to the main board. Most pre-crimped cables available at the time of writing (2023) are the cross-wired ones (pin 1 to 5, pin 2 to 4, pin 4 to 2, pin 5 to 1). Which means if you do not pay attention you may end up cross-connecting MIC and EAR. At best, nothing will work. At worst, you may damage that precious ULA. Just get the wires with the KK 254 / KF 2510 connector on one end and carefully solder wires according to the skilscreen markings.

[Interactive BOM](https://htmlpreview.github.io/?https://github.com/jameshpdp/Spectrum-2-TapeIn/blob/main/bom/ibom.html)

| Reference         | Item     | Count |
| ----------------- | -------- | ----- |
| C1, C2            | 20 nF    |     2 |
| C3                | 22 uF    |     1 |
| R1-R4, R6, R7, R9 | 100 kOhm |     7 |
| R5                | 470 kOhm |     1 |
| R8                | 68 kOhm  |     1 |
| D2            | 1N5819   |     1 |
| U1                | LM358    |     1 |
| DECK1, PCB1 (opt) | Molex KK-254 AE-6410 | 1 (2) |

Molex KK 254 / KF 2510 connectors optional, required only if you want to avoid cutting/modifing existing tape deck wiring. Otherwise you can simply solder wires to the corresponding pads as marked on the PCB.

## Revision Hisory
Rev. C -- first public release

Rev. D -- KK 254 / 2510 connectors (optional), removed D1, extra details on the silkscreen
