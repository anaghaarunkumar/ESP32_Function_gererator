# ESP32 Function Generator Hardware

## Circuit Diagram

![ESP32 Circuit](images/esp32_circuit.png)

## Hardware Components

- ESP32-WROOM-32 development board
- USB cable
- Jumper wires
- Breadboard
- Oscilloscope

## Pin Connections

| ESP32 Pin | Function                       |
|-----------|----------                      |
| GPIO25    | DAC analog waveform output     |
| GND       | Common ground                  |
| GPIO2     | Status LED, where available    |
| USB       | Power and serial communication |

## Working Principle

The ESP32 receives waveform configuration commands
from the Python GUI through USB serial communication.

The firmware uses Direct Digital Synthesis (DDS)
to generate waveform samples.

The internal DAC converts these samples into an
analog voltage that can be observed on an oscilloscope.

## Testing

Record the actual observed waveforms, frequency,
amplitude and DC offset during hardware testing.