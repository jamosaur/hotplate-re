# hotplate-re

Reverse engineering a super cheap AliExpress hotplate.

From my initial research, it appears that there are 2 versions of this product.

- White PCB Rev
- Purple PCB Rev

**This will be focusing on the white PCB revision as that is the one that I have.**

### The main differences between the two are:

- White doesn't have countersunk screws on the plate surface (effectively making the plate size about 50% smaller), purple revision does.
- White's thermistor is just taped to the plate surface, purple appears to be attached with silicone and then taped.
- White uses non-heat shielded wires to the thermistor.

## Components / BOM

Reference image with designators

![hotplate-re-designators](https://github.com/jamosaur/hotplate-re/assets/4105611/afd66c2e-a305-4796-a51b-e32107714642)


| Designator | Value/Model | LCSC | Notes |
| --- | --- | --- | --- |
| SW1 | XKB Connectivity TS-1010-C-A | [link](https://www.lcsc.com/product-detail/Tactile-Switches_XKB-Connectivity-TS-1010-C-A_C692458.html)
| SW2 | XKB Connectivity TS-1010-C-A | [link](https://www.lcsc.com/product-detail/Tactile-Switches_XKB-Connectivity-TS-1010-C-A_C692458.html)
| J3 | 12pin usb-c | [link](https://www.lcsc.com/product-detail/USB-Connectors_Korean-Hroparts-Elec-TYPE-C-31-M-13_C223906.html) | Not a match, but kinda in spec?
| U1 | CH224K | [link](https://www.lcsc.com/product-detail/USB-ICs_WCH-Jiangsu-Qin-Heng-CH224K_C970725.html) | PD Sink
| U2 | MP2451 | [link](https://www.lcsc.com/product-detail/DC-DC-Converters_Monolithic-Power-Systems-MP2451DJ_C400566.html) | Step down switching regulator
| U3 | STC8H3K64S2 | [link](https://www.lcsc.com/product-detail/Microcontroller-Units-MCUs-MPUs-SOCs_span-style-background-color-ff0-STC-span-Micro-STC8H3K64S2-45I-TSSOP20_C2901851.html) | MCU
| Q1 | NCE6050KA | [link](https://www.lcsc.com/product-detail/MOSFETs_Wuxi-span-style-background-color-ff0-NCE-span-Power-Semiconductor-NCE6050KA_C96013.html)
| D1 | SS24 | [link](https://www.lcsc.com/product-detail/Schottky-Barrier-Diodes-SBD_Shandong-Jingdao-Microelectronics-SS24_C115726.html)
| L1 | ?
| C1 | ?
| C2 | ?
| C3 | ?
| C4 | ?
| C5 | ?
| C6 | ?
| C7 | ?
| C8 | ?
| C9 | ?
| R1 | 10k
| R2 | NC
| R3 | 10k
| R4 | NC
| R5 | 10k
| R6 | 10k
| R7 | 10k
| R8 | 10k
| R9 | 1k
| R10 | 100k (86.1k)
| R11 | 100k (86.1k)
| R12 | 24k
| R13 | 75k
| R14 | 10k
| R15 | 91k
| R16 | 510


### Board Information

#### Main Board

Size: 49.9 x 44.5 mm (at widest)

#### Heating Plate

Size: 55.85 x 55.89 mm
Resistance: 5.7 ohms @ 24.4c
Actual usable size: 39.25 x 39.25 mm
