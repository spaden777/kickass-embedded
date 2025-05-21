# Firmware Dev Notes

## Build System
- `make all`: Builds firmware image and linker map using Makefile.
- Artifacts are output to the `build` directory, as defined in CI pipeline.

## Test Strategy
- `make test`: Executes unit tests using embedded-targeted framework or simulation.
- Tests include state machine logic, edge condition handling, and timing checks.

## Deployment
- `echo "Deploy logic here"` is a placeholder.
- Replace with `st-flash write firmware.bin 0x8000000` or OTA update command for real hardware.

## CI/CD Summary
The CI pipeline (`ci-sample.yml`) runs build, test, and deploy steps via GitLab CI.  
All stages are configured to ensure firmware quality and reproducibility across hardware targets.

## UART Debug
- TX on PA2, RX on PA3
- Baud rate: 115200
- Disabled in production firmware

## Peripheral Map
- I2C1: Temp sensor, EEPROM
- SPI2: OLED display
- UART3: Debug serial
