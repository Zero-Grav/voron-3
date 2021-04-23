# klipper-config

Klipper config for Voron 2.4 
- 2x SKR 1.4 Turbo
- 7x TMC2209
- 1.8 degree steppers Z/E (LDO)
- 0.9 degree steppers for A/B (LDO)

## Setup
Clone this repository into `klipper_config`:
```
cd klipper_config
git clone https://github.com/nielsvz/voron-2.git
```

Load these config files by adding an include statement to printer.cfg:
```
[include voron-2/klipper_config/*.cfg]
```

## Slicer configuration

## Start gcode
PrusaSlicer:  
```
M140 S0
M104 S0 ; uncomment to remove set&wait temp gcode added automatically after this start gcode
print_start EXTRUDER_TEMP=[first_layer_temperature] BED_TEMP=[first_layer_bed_temperature] NOZZLE_SIZE=[nozzle_diameter] FILAMENT_TYPE=[filament_type]
```

SuperSlicer:  
```
M190 S0
M109 S0 ; uncomment to remove set&wait temp gcode added automatically after this start gcode
print_start EXTRUDER_TEMP={first_layer_temperature[initial_extruder] + extruder_temperature_offset[initial_extruder]} BED_TEMP=[first_layer_bed_temperature] CHAMBER_TEMP=[chamber_temperature] NOZZLE_SIZE=[nozzle_diameter] FILAMENT_TYPE=[filament_type]
```


## End gcode

PrusaSlicer and SuperSlicer:
```
print_end
```
