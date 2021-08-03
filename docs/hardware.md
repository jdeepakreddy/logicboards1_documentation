# Hardware Documentation

## Key Components MNP

- MPU: STM32MP157CAC3
- DDR3L: AS4C256M16D3LC-12BCN
- eMMC: S40FC004C1B2C00000
- PMIC: STPMIC1BPQR
- Wireless: LBEE59B1LV-278

## Reference Docs / Files

### Datasheets
[STM32MP157C/F Datasheet](files/datasheets/STM32MP157.pdf) <br>
[DDR3L RAM Datasheet](files/datasheets/DDR3L.pdf) <br>
[eMMC Datasheet](files/datasheets/eMMC.pdf)<br>
[PMIC Datasheet](files/datasheets/STPMIC.pdf)<br>
[Wireless Module Datasheet](files/datasheets/LBEE59B1LV-278.pdf)<br>

### Reference Manual
[STM32MP157 Reference Manual](https://www.st.com/resource/en/reference_manual/rm0436-stm32mp157-advanced-armbased-32bit-mpus-stmicroelectronics.pdf)<br>

### Application Notes / Guides
[STM32MP157 hardware development Application note (AN5031)](files/application_notes/AN5031.pdf)<br>
[DDR memory routing guidelines Application note (AN5122)](files/application_notes/AN5122.pdf) <br>
[HDI PCB Design Guide](files/application_notes/HDI-Design-Guide.pdf)

### STM32MP157C-DK2 Reference Files (MB1272C)
[MB1272C User Manual](files/MB1272C/stm32mp1-dk2_usermanual.pdf)<br>
[MB1272C Schematic](files/MB1272C/schematic_MB1272C.pdf)<br>
[MB1272C BOM (.xlsx format)](files/MB1272C/MB1272-DK2-C01_BOM.xlsx)<br>
[MB1272C Altium Design Files](files/MB1272C/design_files_MB1272C.zip)<br>
[MB1272C Fabrication Files](files/MB1272C/fab_files_MB1272C.zip)

### STM32MP157A-EV1 Reference Files (MB1263)
[MB1263A User Manual](files/MB1263A/MB1263A_UM.pdf)<br>
[MB1263A Schematic](files/MB1263A/MB1263_SCH.pdf)<br>
[MB1263A BOM (.xlsx format)](files/MB1263A/MB1263-C02.xlsx)<br>
[MB1263A Altium Design Files](files/MB1263A/MB1263C_Altium_Files.zip)<br>
[MB1263A Fabrication Files](files/MB1263A/MB1263C_FabFiles.zip)

### DSI-LCD Reference Files (MB1407C)
[MB1407C Schematic](files/MB1407C/schematic_MB1407C.pdf)<br>
[MB1407C BOM (.xlsx format)](files/MB1407C/MB1407-LCD-C01_BOM.xlsx)<br>
[MB1407C Altium Design Files](files/MB1407C/design_files_MB1407C.zip)<br>
[MB1407C Fabrication Files](files/MB1407C/fab_files_MB1407C.zip)


## Logicboard 1 Files Rev 1.0.0

### Schematic
[Logicboard 1A Rev 1.0.0 Schematic (PDF)](files/logicboard1A/Schematics/Rev_1.0.0/LB1A_DCA7M4_R512MB_F4GB_REV1.0.0.pdf)

### PCB Fabrication Files
[Logicboard 1A PCB Fabrication Files (ZIP)](files/logicboard1A/PCB_Fabrication/Logicboard1A_Rev1.0.0.zip)

### Bill of Materials

[Logicboard 1A Bill of Materials (PDF)](files/logicboard1A/BOM/logicboard1A_BOM.pdf) <br>

[Logicboard 1A Bill of Materials (.XLSX)](files/logicboard1A/BOM/BOM_Logicboard_1A.xlsx)

### Assembly Files
[Logicboard 1A Front Assembly (PDF)](files/logicboard1A/Assembly/Front_Assembly_Drawing.pdf) <br>

[Logicboard 1A Back Assembly (PDF)](files/logicboard1A/Assembly/Back_Assembly_Drawing.pdf)


### 3D Files
[Logicboard 1A Bill of Materials (STEP)](files/logicboard1A/3DFiles/LB1A_DCA7M4_R512MB_F4GB.step)


## Logicboard 1 Files Rev 2.0.0
### Schematic
[Logicboard 1A Rev 2.0.0 Schematic (PDF)](files/logicboard1A/Schematics/Rev_2.0.0/LB1A_DCA7M4_R512MB_F4GB_REV2.0.0.pdf)


## Logicboard 1 Files Rev 3.0.0
### Schematic



### PCB Fabrication Files
### Bill of Materials
### Assembly Files
### 3D Files

## Design Notes

### Power Management IC

#### PMIC Power On Sequence

- PWR_ON_RESET => BUCK3 => BUCK1, BUCK4, LDO2, LDO5 => LDO4 <br>
- BUCK2, LDO1, LDO3, LDO6, REFDDR enable by I2C

#### PMIC Factory Default Voltages

<span style="color:blue">**Buck Converters**</span><br>

- **BUCK1 (VOUT1)** = Default 1.2V; Imax = 2000mA; Application = Core supply. 
- **BUCK2 (VOUT2)** = Default 1.1V; Imax = 1600mA; <span style="color:red"> **NOT ON BY DEFAULT** </span>Application = Core
- **BUCK3 (VOUT3)** = Default 1.8V; Imax = 1000mA; Application = VIO. 
- **BUCK4 (VOUT4)** = Default 3.3V; Imax = 3000mA; Application = Application CPU or GP.

<span style="color:blue">**LDOs**</span><br>

- **LDO1** = Default 1.8V; Imax = 800mA; <span style="color:red"> **NOT ON BY DEFAULT** </span> Application = Core supply.
- **LDO2** = Default 2.9V; Imax = 800mA; Application = Core supply.
- **LDO3** = Default 1.8V; Imax = 150mA; <span style="color:red"> **NOT ON BY DEFAULT** </span> Application = Core supply.
- **LDO4** = <span style="color:green">**Fixed 3.3V**</span>; Imax = 200mA; Application = Core supply.
- **LDO5** = Default 2.9V; Imax = 800mA; Application = Core supply.
- **LDO6** = Default 1.0V; Imax = 350mA; <span style="color:red"> **NOT ON BY DEFAULT** </span>Application = Core supply.


### Microprocessor Unit (MPU)

#### I2C1 Peripherals

- DSI 
- HDMI
- GPIO Expansion Headers

#### I2C4 Peripherals

- PMIC
- USB-C


## Logicboard 1A board bringup

### Connections checklist / Debug

   <span style="color:red"> TO ADD </span>




## ToDo
1. Implement Bluetooth Connections.
2. Connect all GPIOs to board to board connectors.