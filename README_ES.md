## 🌐 Language / Idioma

🇲🇽 **Usuarios de México y habla hispana**  
➡️ Estás leyendo la versión en Español

🇺🇸 **International users**  
➡️ [Read the documentation in English](README.md)


# Malher Mycelium
[![License: All Rights Reserved](https://img.shields.io/badge/License-All%20Rights%20Reserved-red)](LICENSE)

Un dispositivo Meshtastic totalmente modular basado en el microcontrolador de ultra bajo consumo nRF52840. Soporta 22 dBm con el HT-RA62 o hasta 1 W usando el E22-900M30S. La PCB principal es compacta y se puede expandir mediante módulos laterales (pantalla, GPS, sensores). Diseñado en México para la comunidad.

## Pictures

| PCB Frente (Top)                          | PCB Reverso (Bottom)                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-bare.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-bottom-bare.png?raw=true" height="500" alt="PCB Bottom Bare"> |

<details><summary>Más imágenes (3D, ensamblado, con case)</summary>

### Render 3D
| PCB Frente (Top)                          | PCB Reverso (Bottom)                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-ecad.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-bot-ecad.png?raw=true" height="500" alt="PCB Bottom Bare"> |

### PCB ensamblada – Variante HT-RA62 con módulo GPS
| PCB Ensamblada Frente (Top)                          | PCB Ensamblada Reverso (Bottom)                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-populated_ht.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-bottom-populated.png?raw=true" height="500" alt="PCB Bottom Bare"> |

### PCB ensamblada – Variante E22 con pantalla OLED 1.3", GPS e INA226
| PCB Ensamblada Frente (Top)                          |                         |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/pcb-top-populated_e22.png?raw=true" height="500" alt="PCB Top Bare"> |  |

### Radio completamente ensamblado con clip Baofeng opcional
| Radio Ensamblado Frente                        | Radio Ensamblado Reverso                        |
|--------------------------------------|--------------------------------------|
| <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/radio-assembled-front.png?raw=true" height="500" alt="PCB Top Bare"> | <img src="https://github.com/MalherLabs/Mycelium/blob/main/Images/radio-assembled-back.png?raw=true" height="500" alt="PCB Bottom Bare"> |

</details>


## Features
- PCB base compacta: 39 mm × 65 mm, expandible según se requiera
- Módulo compatible tipo Pro Micro con nRF52840

### Soporte para radio LoRa
- Soporte para módulos LoRa **Ebyte E22-900M30S (1 W)** o **Heltec HT-RA62**
- Convertidor **boost integrado de 3.3 V a 5 V** para alimentar el módulo E22 cuando se usa transmisión de 1 W

### Gestión de energía
- Interruptor de encendido en la PCB (opcional)
- Conector de batería PH2.0-2 compatible con la mayoría de baterías de litio (opcional)
- Sensado de voltaje de batería (opcional)
- Control de energía por MOSFET para habilitar o deshabilitar el módulo GPS (opcional)

### Interfaz de usuario
- Botón de usuario y botón de reset (opcional)
- Soporte para **pantallas OLED** (opcional):
  - 1.3" SH1106  
  - 0.96" SSD1306
- Buzzer SMD para notificaciones de mensajes y eventos (opcional)
- Header para **encoder rotatorio PEC11** para navegación de menús y mensajes predefinidos (opcional)

### Sensores y expansión
- Soporte para **módulo GPS ATGM336H** (opcional)
- Soporte para **sensado de corriente INA226** (opcional)

## Variantes y opciones de ensamblaje

La placa está diseñada con **modularidad total**. Puedes ensamblar exactamente lo que necesites:

- **Base** → Mínima, la más económica y de menor consumo
- **Standard** → Recomendada para la mayoría de los usuarios (uso diario)
- **Extended** → Totalmente equipada (elige solo los módulos que quieras)

| Módulo | Variante Base | Variante Standard | Variante Extended |
|------|------|------|------|
| **Placa ProMicro nRF52840** | ✅ Requerido | ✅ Requerido | ✅ Requerido |
| **Módulo LoRa** | ✅ Elegir uno:<br>• HT-RA62 (22 dBm)<br>• E22-900M30S (30 dBm / 1 W) | ✅ Igual | ✅ Igual |
| **Regulador Boost +5 V** | ⚠️ Solo si se usa E22 | ⚠️ Solo si se usa E22 | ⚠️ Solo si se usa E22 |
| **Interruptor de encendido** | ❌ Puente JP1 | ✅ Requerido | ✅ Requerido |
| **Conector de batería (PH2.0)** | ❌ Conexión directa | ✅ Requerido | ✅ Requerido |
| **Sensado de batería** | ❌ | ✅ Requerido | ✅ Requerido |
| **Botón Reset** | ❌ | ✅ Requerido | ✅ Requerido |
| **Botón Usuario** | ❌ | ✅ Requerido | ✅ Requerido |
| **Pantalla OLED**<br>(1.3" SH1106 or 0.96" SSD1306) | ❌ | ❌ | ✅ Opcional |
| **Módulo GPS** | ❌ | ❌ | ✅ Opcional |
| **MOSFET de energía GPS** | ❌ | ❌ | ⚠️ Solo si hay GPS |
| **Buzzer SMD** | ❌ | ❌ | ✅ Opcional |
| **Encoder rotatorio** | ❌ | ❌ | ✅ Opcional |
| **INA226 (CJMCU-226)** | ❌ JP4 | ❌ | ✅ Opcional |

### Cómo elegir tu configuración
- **Base** → Nodo ultra compacto y de ultra bajo consumo (ideal para solar o despliegues largos).
- **Standard** → El mejor balance para el 95 % de los usuarios.
- **Extended** → Agrega solo los módulos que realmente necesitas.

## Listado de Materiales (BOM)

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

## Notas Importantes
- Esta PCB está diseñada como una **plataforma modular y configurable**.
- **Nunca energices el dispositivo sin una antena de 915 MHz conectada.**
- **Solo se debe ensamblar un módulo LoRa a la vez.**
- El **E22-900M30S requiere obligatoriamente el boost MT3608**.
- Verifica siempre la **polaridad de la batería** antes de conectarla.
- El MOSFET de energía GPS solo debe ensamblarse si se instala el GPS.
- El consumo varía significativamente según los módulos instalados.
- Diseñado para usar el **firmware oficial de Meshtastic**.
- Proyecto orientado a **uso educativo, experimental y maker**.

## ¿Listo para usar?
¿No quieres ensamblarlo tú?

Unidades ensambladas y kits disponibles en:  
👉 https://www.malherlabs.com

## About Meshtastic

Meshtastic® es una marca registrada de Meshtastic LLC.  
Los componentes de software de Meshtastic se publican bajo diversas licencias open-source.  
Para más detalles consulta el repositorio oficial de Meshtastic en GitHub.

## License

© 2026 Malher Labs. Todos los derechos reservados.

Los archivos de diseño de este repositorio (esquemáticos, PCB, Gerbers, BOM, modelos 3D, documentación e imágenes) se comparten para permitir el uso **personal y no comercial**, con el objetivo de fortalecer la comunidad Meshtastic en México.

### Está permitido:
- Usar los archivos para proyectos personales.
- Fabricar unidades para uso propio o comunitario sin fines de lucro.
- Compartir los archivos originales sin modificaciones, conservando este aviso y dando crédito a Malher Labs.

### No está permitido:
- Uso comercial por terceros.
- Modificar o crear derivados del diseño.
- Revender o redistribuir los archivos en otras plataformas.

Si prefieres una unidad ensamblada, visita:  
https://www.malherlabs.com

## Disclaimer

Este proyecto se proporciona **tal cual**, sin garantías de ningún tipo.

- El uso del diseño es bajo tu propia responsabilidad.
- Malher Labs no se hace responsable por daños, fallas o problemas legales.
- El uso de radiofrecuencia debe cumplir la normativa local (IFT en México).
- El firmware de Meshtastic tiene su propia licencia; este aviso aplica solo al hardware.
