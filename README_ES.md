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
| **Pantalla OLED** | ❌ | ❌ | ✅ Opcional |
| **Módulo GPS** | ❌ | ❌ | ✅ Opcional |
| **MOSFET de energía GPS** | ❌ | ❌ | ⚠️ Solo si hay GPS |
| **Buzzer SMD** | ❌ | ❌ | ✅ Opcional |
| **Encoder rotatorio** | ❌ | ❌ | ✅ Opcional |
| **INA226 (CJMCU-226)** | ❌ JP4 | ❌ | ✅ Opcional |

### Cómo elegir tu configuración
- **Base** → Nodo ultra compacto y de ultra bajo consumo (ideal para solar o despliegues largos).
- **Standard** → El mejor balance para el 95 % de los usuarios.
- **Extended** → Agrega solo los módulos que realmente necesitas.

## Important Notes
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
