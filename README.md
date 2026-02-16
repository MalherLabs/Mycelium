# Malher Mycelium
A fully modular Meshtastic device based on the ultra-low-power nRF52840. Supports 22 dBm with the HT-RA62 or up to 1W using the E22-900M30S. The compact core PCB scales via side modules (display, GPS, sensors). Designed in Mexico for the community.
## Pictures

| PCB Front (Top)                          | PCB Back (Bottom)                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-bare.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-bottom-bare.png?raw=true" height="500" alt="PCB Bottom Bare"> |
<details><summary>More Pictures (3D, Assembled, With Case)</summary>

  ### 3D Render
| PCB Front (Top)                          | PCB Back (Bottom)                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-ecad.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-bot-ecad.png?raw=true" height="500" alt="PCB Bottom Bare"> |

### PCB Assembled HT-RA62 Variant with GPS module
| PCB Assembled Front (Top)                          | PCB Assembled Back (Bottom)                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-populated_ht.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-bottom-populated.png?raw=true" height="500" alt="PCB Bottom Bare"> |

### PCB Assembled E22 Variant with OLED 1.3 Screen, GPS INA226 
| PCB Assembled Front (Top)                          |                         |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-populated_e22.png?raw=true" height="500" alt="PCB Top Bare"> |  |

### Fully Assembled Radio with optional Baofeng Clip
| Assembled Radio Front                        | Assembled Radio Back                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/radio-assembled-front.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/radio-assembled-back.png?raw=true" height="500" alt="PCB Bottom Bare"> |
  
</details>

  
## Features
- Compact base PCB: 39 mm × 65 mm, expandable as required
- nRF52840 Pro Micro–compatible module

### LoRa Radio Support
- Support for **1 W Ebyte E22-900M30S** or **Heltec HT-RA62** LoRa modules
- On-board **3.3 V to 5 V boost converter** to supply the E22 module when 1 W TX power is used

### Power Management
- On-board power switch (optional)
- PH2.0-2 battery connector, compatible with most lithium batteries (optional)
- Battery voltage sensing (optional)
- MOSFET-based power control to enable or disable the GPS module (optional)

### User Interface
- User button and reset button (optional)
- Support for **OLED displays**: (optional)
  - 1.3" SH1106  
  - 0.96" SSD1306 
- SMD buzzer for message and event notifications (optional)
- Header for **PEC11 rotary encoder** for menu navigation and canned messages (optional)

### Sensors and Expansion
- Support for **ATGM336H GPS module** (optional)
- Support for **INA226 current sensing** (optional)

## Variants & Assembly Options

The board is designed with **full modularity**. You can build exactly what you need:

- **Base** → Minimal, cheapest, lowest power consumption  
- **Standard** → Recommended for most users (ready-to-use daily driver)  
- **Extended** → Fully loaded (you can pick and choose any of the optional modules)


|  Module                                         | Base Variant                          | Standard Variant                      | Extended Variant                              |
|-------------------------------------------------|---------------------------------------|---------------------------------------|-----------------------------------------------|
| **nRF52840 ProMicro board**                     | ✅ Required                            | ✅ Required                            | ✅ Required                                    |
| **LoRa radio module**                           | ✅ Required<br>Choose one:<br>• HT-RA62 (22 dBm)<br>• E22-900M30S (30 dBm / 1 W) | ✅ Required<br>Choose one:<br>• HT-RA62 (22 dBm)<br>• E22-900M30S (30 dBm / 1 W)                         | ✅ Required<br>Choose one:<br>• HT-RA62 (22 dBm)<br>• E22-900M30S (30 dBm / 1 W)                                  |
| **+5V Boost Regulator**                         | ⚠️ Only if E22-900M30S is used        | ⚠️ Only if E22-900M30S is used        | ⚠️ Only if E22-900M30S is used                |
| **Power switch**                                | ❌ Add solder on JP1                   | ✅ Required                            | ✅ Required                                    |
| **Battery connector (PH2.0-2)**                 | ❌ Connect Battery directly to PCB     | ✅ Required                            | ✅ Required                                    |
| **Battery voltage sensing**                     | ❌                                     | ✅ Required                            | ✅ Required                                    |
| **Reset button**                                | ❌                                     | ✅ Required                            | ✅ Required                                    |
| **User button**                                 | ❌                                     | ✅ Required                            | ✅ Required                                    |
| **OLED display**<br>(1.3" SH1106 or 0.96" SSD1306) | ❌                                  | ❌                                     | ✅ Optional (choose one)                       |
| **GPS module** (ATGM336H)                       | ❌                                     | ❌                                     | ✅ Optional                                    |
| **GPS power MOSFET switch**                     | ❌                                     | ❌                                     | ⚠️ Required only if GPS is populated          |
| **SMD Buzzer** (message alert)                  | ❌                                     | ❌                                     | ✅ Optional                                    |
| **Rotary encoder ** (Canned Messages)           | ❌                                     | ❌                                     | ✅ Optional                                    |
| **INA226 current sense** (CJMCU-226 module)     | ❌ Add solder on JP4                   | ❌                                     | ✅ Optional                                    |

### How to choose your build
- **Base** → Ultra-compact, ultra-low-power node (perfect for solar or long-term deployment).
- **Standard** → The sweet spot for 95 % of users (all basic features + battery management).
- **Extended** → Add only the modules you actually want. Everything uses standard footprints/headers — no conflicts.


## Bill of Materials (BOM)

<details><summary>Base Variant – HT-RA62 (22 dBm)</summary>

| Designators     | Qty | Type                  | Part Number / Value      | Package | Link to Supplier                                                                 | Notes                  |
|-----------------|-----|-----------------------|--------------------------|---------|----------------------------------------------------------------------------------|------------------------|
| C4              | 1   | Ceramic Capacitor     | 22 µF / 16 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uF+16V+0805+capacitor) |                        |
| JP1, JP4        | 2   | Solder Bridge         | N/A                      | N/A     | N/A                                                                              | Solder bridges         |
| U2              | 1   | NRF52840 Module       | NRF52840 ProMicro        | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=NRF52840+ProMicro+module) | Core MCU               |
| U3              | 1   | LoRa Radio Module     | HT-RA62                  | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=HT-RA62+module)     |                        |
| N/A             | 1   | Antenna Connector     | SMA-Female               | SMA     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=IPEX+to+SMA-Female+connector+RG178) |                        |
</details>

<details><summary>Base Variant – E22-900M30S (30 dBm / 1 W)</summary>

| Designators              | Qty | Type                      | Part Number / Value      | Package | Link to Supplier                                                                 | Notes                  |
|--------------------------|-----|---------------------------|--------------------------|---------|----------------------------------------------------------------------------------|------------------------|
| C1, C2, C3               | 3   | Ceramic Capacitor         | 100 µF / 10 V            | 1206    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=100uF+10V+1206+capacitor) |                        |
| C4, C5, C6               | 3   | Ceramic Capacitor         | 22 µF / 16 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uF+16V+0805+capacitor) |                        |
| C7                       | 1   | Ceramic Capacitor         | 0.1 µF / 50 V            | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=0.1uF+50V+0805+capacitor) |                        |
| D1                       | 1   | Rectifier Diode           | SS34                     | DO-214AC| [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS34+diode)         |                        |
| JP1, JP4                 | 2   | Solder Bridge             | N/A                      | N/A     | N/A                                                                              | Solder bridges         |
| L1                       | 1   | Inductor                  | 22 µH                    | 1040    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uH+inductor+1040) |                        |
| R1                       | 1   | Resistor                  | 75 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=75K+0805+resistor) | 1% preferred           |
| R2                       | 1   | Resistor                  | 10 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10K+0805+resistor) | 1% preferred           |
| U1                       | 1   | LoRa Radio Module         | E22-900M30S              | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=E22-900M30S+module) |                        |
| U2                       | 1   | NRF52840 Module           | NRF52840 ProMicro        | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=NRF52840+ProMicro+module) |                        |
| U4                       | 1   | Step-Up Voltage Regulator | MT3608                   | SOT23-6 | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=MT3608+regulator)   | For 1W TX              |
| N/A                      | 1   | Antenna Connector         | SMA-Female               | SMA     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=IPEX+to+SMA-Female+connector+RG178) |                        |
</details>

<details><summary>Standard Variant – HT-RA62 (22 dBm)</summary>

| Designators              | Qty | Type                  | Part Number / Value      | Package | Link to Supplier                                                                 | Notes                  |
|--------------------------|-----|-----------------------|--------------------------|---------|----------------------------------------------------------------------------------|------------------------|
| C4                       | 1   | Ceramic Capacitor     | 22 µF / 16 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uF+16V+0805+capacitor) |                        |
| C9, C10, C15             | 3   | Ceramic Capacitor     | 0.1 µF / 50 V            | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=0.1uF+50V+0805+capacitor) |                        |
| J1                       | 1   | Battery Connector     | PH 2.0 mm 2-pin          | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=PH2.0-2+connector)  |                        |
| JP4                      | 1   | Solder Bridge         | N/A                      | N/A     | N/A                                                                              |                        |
| R5, R15                  | 2   | Resistor              | 10 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10K+0805+resistor) | 1% preferred           |
| R6                       | 1   | Resistor              | 1 MΩ 1%                  | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1Meg+0805+resistor) | 1% preferred           |
| R7                       | 1   | Resistor              | 1.5 MΩ 1%                | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1.5Meg+0805+resistor) | 1% preferred           |
| SW1                      | 1   | SPDT Power Switch     | SS-12D11                 | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS-12D11+switch)    |                        |
| SW2, SW3                 | 2   | Push Button           | 3×4×2 mm                 | 3×4×2   | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=3x4x2+push+button)  | User + Reset           |
| U2                       | 1   | NRF52840 Module       | NRF52840 ProMicro        | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=NRF52840+ProMicro+module) |                        |
| U3                       | 1   | LoRa Radio Module     | HT-RA62                  | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=HT-RA62+module)     |                        |
| N/A                      | 1   | Antenna Connector     | SMA-Female               | SMA     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=IPEX+to+SMA-Female+connector+RG178) |                        |
</details>

<details><summary>Standard Variant – E22-900M30S (30 dBm / 1 W)</summary>

| Designators              | Qty | Type                      | Part Number / Value      | Package | Link to Supplier                                                                 | Notes                  |
|--------------------------|-----|---------------------------|--------------------------|---------|----------------------------------------------------------------------------------|------------------------|
| C1, C2, C3               | 3   | Ceramic Capacitor         | 100 µF / 10 V            | 1206    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=100uF+10V+1206+capacitor) |                        |
| C4, C5, C6               | 3   | Ceramic Capacitor         | 22 µF / 16 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uF+16V+0805+capacitor) |                        |
| C7, C9, C10, C15         | 4   | Ceramic Capacitor         | 0.1 µF / 50 V            | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=0.1uF+50V+0805+capacitor) |                        |
| D1                       | 1   | Rectifier Diode           | SS34                     | DO-214AC| [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS34+diode)         |                        |
| J1                       | 1   | Battery Connector         | PH 2.0 mm 2-pin          | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=PH2.0-2+connector)  |                        |
| JP4                      | 1   | Solder Bridge             | N/A                      | N/A     | N/A                                                                              |                        |
| L1                       | 1   | Inductor                  | 22 µH                    | 1040    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uH+inductor+1040) |                        |
| R1                       | 1   | Resistor                  | 75 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=75K+0805+resistor) | 1% preferred           |
| R2, R5, R15              | 3   | Resistor                  | 10 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10K+0805+resistor) | 1% preferred           |
| R6                       | 1   | Resistor                  | 1 MΩ 1%                  | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1Meg+0805+resistor) | 1% preferred           |
| R7                       | 1   | Resistor                  | 1.5 MΩ 1%                | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1.5Meg+0805+resistor) | 1% preferred           |
| SW1                      | 1   | SPDT Power Switch         | SS-12D11                 | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS-12D11+switch)    |                        |
| SW2, SW3                 | 2   | Push Button               | 3×4×2 mm                 | 3×4×2   | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=3x4x2+push+button)  | User + Reset           |
| U1                       | 1   | LoRa Radio Module         | E22-900M30S              | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=E22-900M30S+module) |                        |
| U2                       | 1   | NRF52840 Module           | NRF52840 ProMicro        | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=NRF52840+ProMicro+module) |                        |
| U4                       | 1   | Step-Up Voltage Regulator | MT3608                   | SOT23-6 | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=MT3608+regulator)   | For 1W TX              |
| N/A                      | 1   | Antenna Connector         | SMA-Female               | SMA     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=IPEX+to+SMA-Female+connector+RG178) |                        |
</details>

<details><summary>Extended Variant – HT-RA62 (22 dBm)</summary>

| Designators              | Qty | Type                        | Part Number / Value      | Package | Link to Supplier                                                                 | Notes                                           |
|--------------------------|-----|-----------------------------|--------------------------|---------|----------------------------------------------------------------------------------|-------------------------------------------------|
| BZ1                      | 1   | Active Buzzer               | 9650 3V Active           | 9650    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=9650+3V+Active+Buzzer) | Optional buzzer                                 |
| C4, C11                  | 2   | Ceramic Capacitor           | 22 µF / 16 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uF+16V+0805+capacitor) |                                                 |
| C9, C10, C15             | 3   | Ceramic Capacitor           | 0.1 µF / 50 V            | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=0.1uF+50V+0805+capacitor) |                                                 |
| C12, C13, C14            | 3   | Ceramic Capacitor           | 10 nF / 50 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10nF+50V+0805+capacitor) | Required for rotary encoder                     |
| J1                       | 1   | Battery Connector           | PH 2.0 mm 2-pin          | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=PH2.0-2+connector)  |                                                 |
| Q1                       | 1   | P-Channel MOSFET            | AO3401                   | SOT-23  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=AO3401+mosfet)      | ⚠️ Required only if GPS module is populated     |
| Q2                       | 1   | N-Channel MOSFET            | AO3400                   | SOT-23  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=AO3400+mosfet)      | ⚠️ Required only if GPS module is populated     |
| R5, R8, R9, R10, R15     | 5   | Resistor                    | 10 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10K+0805+resistor) | 1% preferred; 5% also works                     |
| R6, R14, R16             | 3   | Resistor                    | 1 MΩ 1%                  | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1Meg+0805+resistor) | 1% preferred; 5% also works                     |
| R7                       | 1   | Resistor                    | 1.5 MΩ 1%                | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1.5Meg+0805+resistor) | 1% preferred; 5% also works                     |
| R11, R12, R13            | 3   | Resistor                    | 1 kΩ 1%                  | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1K+0805+resistor) | 1% preferred; 5% also works                     |
| SW1                      | 1   | SPDT Power Switch           | SS-12D11                 | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS-12D11+switch)    |                                                 |
| SW2, SW3                 | 2   | Push Button                 | 3×4×2 mm                 | 3×4×2   | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=3x4x2+push+button)  | User + Reset                                    |
| U2                       | 1   | NRF52840 Module             | NRF52840 ProMicro        | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=NRF52840+ProMicro+module) | Core microcontroller                            |
| U3                       | 1   | LoRa Radio Module           | HT-RA62                  | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=HT-RA62+module)     | 22 dBm option                                   |
| U7                       | 1   | Current Sense Module        | CJMCU-226 (INA226)       | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=CJMCU-226+module)   | Optional current monitoring                     |
| U8                       | 1   | GPS Module                  | ATGM336H                 | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=ATGM336H+GPS+module) | Optional GPS                                    |
| U9                       | 1   | OLED Display 0.96"          | SSD1306                  | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SSD1306+0.96in+OLED) | Optional 0.96" OLED                             |
| U10                      | 1   | OLED Display 1.3"           | SH1106                   | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SH1106+1.3in+OLED)  | Optional 1.3" OLED                              |
| N/A                      | 1   | Antenna Connector           | SMA-Female               | SMA     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=IPEX+to+SMA-Female+connector+RG178) |                                                 |
| N/A                      | 1   | Rotary Encoder              | EC11 20 mm Plum Handle   | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=EC11+20mm+Plum+Handle+encoder) | Required for rotary encoder                     |
| N/A                      | 1   | Encoder Knob / Cap          | Black CAP                | N/A     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=Black+CAP+for+EC11+encoder) | Required for rotary encoder                     |
</details>

<details><summary>Extended Variant – E22-900M30S (30 dBm / 1 W)</summary>

| Designators              | Qty | Type                        | Part Number / Value      | Package | Link to Supplier                                                                 | Notes                                           |
|--------------------------|-----|-----------------------------|--------------------------|---------|----------------------------------------------------------------------------------|-------------------------------------------------|
| BZ1                      | 1   | Active Buzzer               | 9650 3V Active           | 9650    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=9650+3V+Active+Buzzer) | Optional buzzer                                 |
| C1, C2, C3               | 3   | Ceramic Capacitor           | 100 µF / 10 V            | 1206    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=100uF+10V+1206+capacitor) |                                                 |
| C4, C5, C6, C11          | 4   | Ceramic Capacitor           | 22 µF / 16 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uF+16V+0805+capacitor) |                                                 |
| C7, C9, C10, C15         | 4   | Ceramic Capacitor           | 0.1 µF / 50 V            | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=0.1uF+50V+0805+capacitor) |                                                 |
| C12, C13, C14            | 3   | Ceramic Capacitor           | 10 nF / 50 V             | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10nF+50V+0805+capacitor) | Required for rotary encoder                     |
| D1                       | 1   | Rectifier Diode             | SS34                     | DO-214AC| [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS34+diode)         |                                                 |
| J1                       | 1   | Battery Connector           | PH 2.0 mm 2-pin          | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=PH2.0-2+connector)  |                                                 |
| L1                       | 1   | Inductor                    | 22 µH                    | 1040    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=22uH+inductor+1040) |                                                 |
| Q1                       | 1   | P-Channel MOSFET            | AO3401                   | SOT-23  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=AO3401+mosfet)      | ⚠️ Required only if GPS module is populated     |
| Q2                       | 1   | N-Channel MOSFET            | AO3400                   | SOT-23  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=AO3400+mosfet)      | ⚠️ Required only if GPS module is populated     |
| R1                       | 1   | Resistor                    | 75 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=75K+0805+resistor) | 1% preferred; 5% also works                     |
| R2, R5, R8, R9, R10, R15 | 6   | Resistor                    | 10 kΩ 1%                 | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=10K+0805+resistor) | 1% preferred; 5% also works                     |
| R6, R14, R16             | 3   | Resistor                    | 1 MΩ 1%                  | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1Meg+0805+resistor) | 1% preferred; 5% also works                     |
| R7                       | 1   | Resistor                    | 1.5 MΩ 1%                | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1.5Meg+0805+resistor) | 1% preferred; 5% also works                     |
| R11, R12, R13            | 3   | Resistor                    | 1 kΩ 1%                  | 0805    | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=1K+0805+resistor) | 1% preferred; 5% also works                     |
| SW1                      | 1   | SPDT Power Switch           | SS-12D11                 | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SS-12D11+switch)    |                                                 |
| SW2, SW3                 | 2   | Push Button                 | 3×4×2 mm                 | 3×4×2   | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=3x4x2+push+button)  | User + Reset                                    |
| U1                       | 1   | LoRa Radio Module           | E22-900M30S              | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=E22-900M30S+module) | 30 dBm / 1 W option                             |
| U2                       | 1   | NRF52840 Module             | NRF52840 ProMicro        | SMD     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=NRF52840+ProMicro+module) | Core microcontroller                            |
| U4                       | 1   | Step-Up Voltage Regulator   | MT3608                   | SOT23-6 | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=MT3608+regulator)   | Required for E22 1 W TX                         |
| U7                       | 1   | Current Sense Module        | CJMCU-226 (INA226)       | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=CJMCU-226+module)   | Optional current monitoring                     |
| U8                       | 1   | GPS Module                  | ATGM336H                 | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=ATGM336H+GPS+module) | Optional GPS                                    |
| U9                       | 1   | OLED Display 0.96"          | SSD1306                  | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SSD1306+0.96in+OLED) | Optional 0.96" OLED                             |
| U10                      | 1   | OLED Display 1.3"           | SH1106                   | Module  | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=SH1106+1.3in+OLED)  | Optional 1.3" OLED                              |
| N/A                      | 1   | Antenna Connector           | SMA-Female               | SMA     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=IPEX+to+SMA-Female+connector+RG178) |                                                 |
| N/A                      | 1   | Rotary Encoder              | EC11 20 mm Plum Handle   | PTH     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=EC11+20mm+Plum+Handle+encoder) | Required for rotary encoder                     |
| N/A                      | 1   | Encoder Knob / Cap          | Black CAP                | N/A     | [AliExpress](https://www.aliexpress.com/wholesale?SearchText=Black+CAP+for+EC11+encoder) | Required for rotary encoder                     |
</details>

## Important Notes
- This PCB is designed as a **modular and configurable platform**. Only populate the components required for the selected LoRa radio and desired feature set.
- **Never power on the device without a properly tuned 915MHz antenna connected.** Transmitting at 30dBm (1 Watt) without a load (antenna) will reflect the energy back into the E22 module, causing permanent damage to the power amplifier (PA).
- **Only one LoRa radio module must be assembled at a time** (HT-RA62 or E22-900M30S).
- When using the **E22-900M30S (1 W) LoRa module**, the **MT3608 boost converter (3.3 V → 5 V)** must be populated to ensure stable TX operation.
- This board uses a standard **JST PH2.0** connector. However, battery manufacturers sometimes swap the Positive (+) and Negative (-) wires. **Always verify the polarity** with a multimeter before plugging in a battery. 
- Optional feature modules can be assembled independently unless otherwise stated in the Variants section.
- The **GPS power control MOSFET must only be assembled if the GPS module is installed**.
- Power consumption varies significantly depending on the selected radio and optional modules (OLED, GPS, buzzer, sensors).
- This hardware is intended to run the **official Meshtastic firmware**. Custom firmware or unsupported configurations may require additional validation.
- This project is intended for **educational, experimental, and maker use**. It has not been certified for commercial, safety-critical, or life-critical applications.

## About Meshtastic

Meshtastic® is a registered trademark of Meshtastic LLC.  
The Meshtastic software components are released under various open-source licenses.  
For full details, please refer to the official [Meshtastic GitHub repository](https://github.com/meshtastic).

## License

© 2026 Malher Labs. All rights reserved.

The design files in this repository (schematics, PCB layouts, Gerber files, BOM, 3D case models, documentation, images, and related materials) are shared openly so that people in Mexico and beyond can build their own Meshtastic radios for personal use and help grow the off-grid communication community.

We want to make it easy for hobbyists, hikers, emergency responders, and makers in Jalisco and all over México to experiment and stay connected — that's why we're making the files available!

### What you can do:
- Download and use the files for your **personal, non-commercial projects**.
- Manufacture **one or more units** for yourself, your family, friends, or local community groups (as long as it's non-commercial and not for resale).
- Share the **exact original files** (without changes) with others in México or anywhere else, as long as you:
  - Keep this full license notice intact
  - Give clear credit: "Design by Malher Labs – www.malherlabs.com"
  - Include a link back to this GitHub repository

### What is not allowed:
- Any **commercial use** by third parties, including selling, reselling, offering for sale, manufacturing for profit, using in paid services, crowdfunding campaigns, or any business activity.
- **Modifying**, remixing, adapting, reverse-engineering, or creating derivative versions of the schematics, PCB, Gerber files, BOM, or 3D case models.
- Removing or changing this copyright notice, the attribution to Malher Labs, or the license terms.
- Uploading or redistributing the files to other platforms/repositories without permission (linking to this repo is welcome and encouraged).

If you prefer not to fabricate it yourself, or if you want an assembled unit, kit, or ready-to-use radio, check out the official store:  
https://www.malherlabs.com

We are happy to receive feedback, photos of your builds, range test results, or suggestions via issues in this repo or through the website. If you're interested in collaboration, bulk orders for community groups, or any other kind of partnership, please reach out — we'd love to support the growth of Meshtastic in México!

The Meshtastic firmware has its own separate license (mainly GPL-3.0). This notice applies only to the hardware design files and 3D models in this repository.

Thank you for building with us — ¡sigamos conectados sin fronteras! 📡
