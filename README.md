
---

# Pocket Jammer Project

## Overview
This project is a simple pocket-sized jammer designed using EasyEDA. The jammer circuit includes key components such as an RF oscillator, RF amplifier, band-pass filter, and an SMA connector for the antenna. Additionally, an LED indicator is added to show when the device is powered on.

## Components
- **Crystal Oscillator**
- **RF Amplifier (MGA-68563)**
- **Band-Pass Filter (LFCN-2250)**
- **SMA Connector (KEP902)**
- **Voltage Regulator (AMS1117-3.3)**
- **Resistors**
  - 10Ω (x2)
  - 1kΩ (x1)
- **Capacitors**
  - 10nF (x2)
  - 100nF (x1)
- **Inductor**
  - 10µH (x1)
- **LED** (with current-limiting resistor 68Ω)

## Schematic
The circuit is designed to jam signals within a specific frequency range. The crystal oscillator generates the RF signal, which is amplified by the RF amplifier. The band-pass filter ensures that only the desired frequency range is transmitted. The SMA connector allows for an external antenna connection.

### Schematic Diagram
```
Power Supply
    |
    |---------> AMS1117-3.3 ---------> Vcc
                      |              |
                      |              +-------> LED -------> Resistor (68Ω) -------> GND
                      |---------> 10µH Inductor
                                   |
                      |---------> MGA-68563 (RF Amplifier)
                      |                    |
                      |                    |
                    GND              +-----+----+
                      |              |          |
                      |             10nF      1kΩ (bias resistor)
                      |              |          |
                      |         Crystal         |
                      |         Oscillator      |
                      |                         |
                     GND                       GND
                      |
                      |------------------> LFCN-2250 (Band-Pass Filter)
                                                  |
                                                  |---------> SMA Connector
                                                  |
                                                 GND
```

## PCB Layout
Ensure proper placement of components to minimize signal path lengths and reduce noise:
1. **Crystal Oscillator** near the RF amplifier input.
2. **Band-Pass Filter** close to the RF amplifier output.
3. **SMA Connector** positioned for easy antenna connection.
4. Implement a ground plane to provide a low-impedance path for return currents and to shield the signal traces.

## Assembly
1. **Place Components**: Solder the components onto the PCB as per the schematic.
2. **Check Connections**: Verify all connections are correct.
3. **Power Up**: Connect to a suitable power supply and verify the LED indicator lights up.
4. **Testing**: Use an RF signal analyzer to verify the jammer's output frequency and performance.

## Safety and Legal Compliance
- Ensure your design complies with local laws and regulations regarding the use of RF jammers.
- Use the device responsibly and only for educational or authorized purposes.


## Acknowledgments
Special thanks to the resources and community at EasyEDA for providing the tools and support to complete this project.

## Contributing
Feel free to fork this repository, make improvements, and submit pull requests. Contributions are welcome!

## Contact
For any questions or support, please contact yachitguliani2005@gmail.com


