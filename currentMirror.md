# 3.Current Mirror

## Aim :
Design and analyze the given current mirror circuit with the following specifications:

1. Voltage Gain (Av) > 10 V/V
2. Supply Voltage (Vdd) = 1.8V
3. Power Consumption (P) <= 1W
4. Design for 1:1 and 1:2 current ratio
5. Consider three cases for channel length (L) :
   * L = 180 nm
   * L = 500 nm
   * L = 1 μm
   * Maintain the same W/L ratio for all cases.
## Theory :
The current mirror is a fundamental building block in analog circuit design, primarily used for biasing and current amplification. It ensures that the output current closely follows the reference current, making it useful in differential amplifiers, operational amplifiers, and voltage regulators.

A basic current mirror consists of two MOSFETs operating in saturation mode. The reference current is set by a biasing resistor or a current source, and the output current is mirrored with minimal variation.

Key properties of a current mirror include:
- **High output resistance**, which ensures accurate current replication.
- **Low input resistance**, allowing efficient current sourcing.
- **Matching of transistor characteristics**, which influences performance and accuracy.
- **Design considerations**, such as channel length modulation and Early voltage effects, which impact current stability.

## Procedure :

Reffer Basic Differential Amplifier experiment for LTspice procedurs for DC, AC and Trancient analysis.








