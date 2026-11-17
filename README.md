
# ESP32 Function Generator

## Project Overview

The ESP32 Function Generator is controlled using a Python
graphical interface communicating with an ESP32 microcontroller
through USB serial communication.

The ESP32 generates analog waveforms using its internal DAC.
The output can be monitored using an oscilloscope.

## System Architecture

![ESP32 Function Generator Architecture](docs/images/system_architecture.png)

### Main Components

- Python GUI
- USB serial communication
- ESP32 microcontroller
- Internal DAC
- Oscilloscope

## ESP32 Firmware

Firmware development branch: `esp32-firmware`

Firmware version: `firmware-v1.0.0`

Open `esp32_function_generator/esp32_function_generator.ino`
in Arduino IDE.

The supplied sketch targets a classic ESP32 with an internal
DAC (GPIO25 / DAC1).

Its source supports Arduino-ESP32 core 2.x/3.x via conditional
compilation. Verify the actual board/core combination before
flashing.

The firmware sketch is unchanged from the supplied completed-project
archives.

Internal firmware version: `1.0.0`

Serial communication:
- Baud rate: 115200
- Protocol: newline-terminated ASCII

Use the `python-gui` branch for the matching PC controller.

## Version History

- `firmware-v1.0.0`: Import and review the existing ESP32
  function generator sketch.
- No second distinct firmware version was present in the
  supplied archives.

## Verification

Record the actual ESP32 board, Arduino core version,
firmware upload result, and oscilloscope observations.

Firmware compilation and hardware operation have not
been verified during repository packaging.

## Development and Collaboration

Future firmware work can use branches such as
`feat/firmware-description` or `fix/firmware-description`,
with pull requests targeting `esp32-firmware`.

Issue and Pull Request label definitions are available
in `.github/labels.json`. Create these labels manually
on GitHub if needed.

Git tags are repository-wide. Component version tags
should use prefixes such as `firmware-` and `gui-`.

GUI V2 is a milestone name for a compatible visual update.
