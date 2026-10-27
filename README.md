# ESP32-C3 Sensor Board

4-layer environmental sensor board built around the ESP32-C3, designed in KiCad as part of the Udemy course *Advanced PCB Design with KiCad 9*. The design follows the course project. I did the schematic capture, layout, and fabrication outputs.

![3D view](docs/Demo_3D_View.png)

## Features

- **MCU:** ESP32-C3-WROOM-02 (Wi-Fi / BLE), external 32 Mbit SPI flash (W25Q32JV)
- **USB:** USB-C, CP2102N USB-UART bridge, USBLC6-2SC6 ESD protection, resettable fuse
- **Power:** MCP73871 Li-Po charger with power-path management, LM1117 3.3 V LDO, JST-PH battery connector
- **Sensors:** BME280 (temperature / humidity / pressure), TEMT6000 ambient light, electret microphone with MAX4466 amplifier
- **Storage / UI:** microSD slot, status LEDs, Boot and Reset buttons
- **Debug:** test points on the SPI bus, pin headers for expansion

## Board

| | |
|---|---|
| Layers | 4 (F.Cu, In1.Cu, In2.Cu, B.Cu) |
| Thickness | 1.6 mm |
| Components | 88 footprints, mostly 0805 passives |
| Tool | KiCad 10 |

## Schematic

Hierarchical, 4 sheets: root, ESP32-C3 / USB / flash, sensors, user interface.
Full PDF: [docs/Demo_Schematic_pdf.pdf](docs/Demo_Schematic_pdf.pdf)

## Files

| Path | Contents |
|---|---|
| `Demo.kicad_pro` | KiCad project |
| `*.kicad_sch` | Schematic sheets |
| `Demo.kicad_pcb` | PCB layout |
| `docs/Demo_Schematic_pdf.pdf` | Schematic, all sheets |
| `docs/Demo_3D_View.png` | 3D view |
| `docs/Demo_BOM.csv` | Bill of materials |
| `fabrication/gerbers.zip` | Gerbers and drill files, ready for upload to a PCB manufacturer |

## Libraries

The custom footprint library (`ESP32_Project_Footprints`) and its 3D models were provided by the course and are not redistributed here. The footprints are embedded in `Demo.kicad_pcb`, so the layout opens and can be inspected without them. Updating the PCB from the schematic requires the original library.

## Status

Design only. Not yet fabricated or tested.
