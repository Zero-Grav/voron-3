# SKR 1.4 pinout usage by MCU <!-- omit in toc -->

- [Motors](#motors)
  - [mcu_xye](#mcu_xye)
  - [mcu_z](#mcu_z)
- [Endstops](#endstops)
- [Heaters](#heaters)
- [Thermistors](#thermistors)
- [Other](#other)

## Motors
| Name          | Pin  |
|---------------|------|
| X_STEP_PIN    | 2.2  |
| X_DIR_PIN     | 2.6  |
| X_ENABLE_PIN  | 2.1  |
| X_UART_PIN    | 1.10 |
| Y_STEP_PIN    | 0.19 |
| Y_DIR_PIN     | 0.20 |
| Y_ENABLE_PIN  | 2.8  |
| Y_UART_RX     | 1.9  |
| Z_STEP_PIN    | 0.22 |
| Z_DIR_PIN     | 2.11 |
| Z_ENABLE_PIN  | 0.21 |
| Z_UART        | 1.8  |
| E0_STEP_PIN   | 2.13 |
| E0_DIR_PIN    | 0.11 |
| E0_ENABLE_PIN | 2.12 |
| E0_UART       | 1.4  |
| E1_STEP_PIN   | 1.15 |
| E1_DIR_PIN    | 1.14 |
| E1_ENABLE_PIN | 1.16 |
| E1_UART_RX    | 1.1  |

### mcu_xye
X: X / B motor  
Y: Y / A motor  
E0: Extruder motor  
E1: PT100 step stick  
E1_UART_RX: extruder > sensor_pin

### mcu_z
X: Z0 motor  
Y: Z1 motor  
Z: Z2 motor  
E0: Z3 motor

## Endstops
| Name        | Pin  | mcu_xye                 | mcu_z                   |
|-------------|------|-------------------------|-------------------------|
| X_STOP_PIN  | 1.29 | stepper_x > endstop_pin |                         |
| Y_STOP_PIN  | 1.28 | stepper_y > endstop_pin |                         |
| Z_STOP_PIN  | 1.27 |                         | stepper_z > endstop_pin |
| E0_DET_PIN  | 1.26 |                         |                         |
| E1_DET_PIN  | 1.26 |                         |                         |
| PWR_DET_PIN | 1.0  |                         |                         |

## Heaters
| Name | Pin | mcu_xye                     | mcu_z                           |
|------|-----|-----------------------------|---------------------------------|
| HE0  | 2.7 | extruder > heater_pin       | temperature_fan chamber > pin   |
| HE1  | 2.4 | heater_fan hotend_fan > pin | heater_fan controller_fan > pin |
| BED  | 2.5 |                             |                                 |

## Thermistors
| Name           | Pin  | mcu_xye   | mcu_z                                |
|----------------|------|-----------|--------------------------------------|
| TH0 (H0 Temp)  | 0.24 |           | temperature_fan chamber > sensor_pin |
| TH1 (H1 Temp)  | 0.23 |           |                                      |
| TB  (Bed Temp) | 0.25 |           | heater_bed > sensor_pin              |

## Other
| Name  | Pin  | mcu_xye   | mcu_z                   |
|-------|------|-----------|-------------------------|
| FAN   | 2.3  | fan > pin | heater_bed > heater_pin |
| SERVO | 2.0  |           |                         |
| PROBE | 0.10 |           | probe > pin             | 
