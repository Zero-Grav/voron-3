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

