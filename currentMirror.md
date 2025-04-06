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

## Calculation

### Given:
- **Supply Voltage**: V<sub>dd</sub> = 1.8V  
- **Power Consumption**: P ≤ 1mW  

### Total Current:
I<sub>total</sub> = P / V<sub>dd</sub> = 1mW / 1.8V = 0.555mA  

### 1:1 Ratio:
I<sub>total</sub> = I<sub>ref</sub> + I<sub>x</sub>  
Since I<sub>ref</sub> = I<sub>x</sub>:  
I<sub>ref</sub> = I<sub>total</sub> / 2 = 0.2775mA  

### 1:2 Ratio:
I<sub>total</sub> = I<sub>ref</sub> + I<sub>x</sub>  
Given I<sub>x</sub> = 2 × I<sub>ref</sub>:  
I<sub>ref</sub> = I<sub>total</sub> / 3 = 0.185mA  
I<sub>x</sub> = 2 × I<sub>ref</sub> = 0.370mA  

## L = 180 nm
### 1:1 W/L Ratio
![Screenshot 2025-03-23 100040](https://github.com/user-attachments/assets/dc126297-68cd-444b-9fd7-d2d4c5e92f02)

### DC Analysis
![Screenshot 2025-03-23 100056](https://github.com/user-attachments/assets/9dde0e14-5826-4171-88f3-96dc7273cd21)


### Transient Analysis
![Screenshot 2025-03-23 145031](https://github.com/user-attachments/assets/33032405-d34d-401b-8953-a6d55a45376f)


### AC Analysis
![Screenshot 2025-03-24 193744](https://github.com/user-attachments/assets/54154034-e8e8-46e4-8d99-7a88cc447468)


### 1:2 W/L Ratio
![Screenshot 2025-03-23 145056](https://github.com/user-attachments/assets/489c0a7b-942d-446b-9e5e-1e5e4d03af63)
### DC Analysis
![Screenshot 2025-03-23 145051](https://github.com/user-attachments/assets/6a09d7b0-9c07-4cdc-81c4-d1a29e1eba4e)


### Transient Analysis
![Screenshot 2025-03-23 100143](https://github.com/user-attachments/assets/90a858f0-8825-4611-b537-b4d5abeddde5)
- The waveform shows further amplification due to the 1:2 ratio.

### AC Analysis
![Screenshot 2025-03-23 160619](https://github.com/user-attachments/assets/f1712368-3be6-48b4-910d-3e674a100f67)
- The measured **-3dB voltage gain (Av) = 21 dB**

## L = 500 nm
### 1:1 W/L Ratio
![Screenshot 2025-03-23 153233](https://github.com/user-attachments/assets/409d0f9d-8f15-40d4-9bed-f16c3417e18d)
### DC Analysis
![Screenshot 2025-03-23 151351](https://github.com/user-attachments/assets/cf83b071-d6c3-440a-aa0f-8095fa97afe6)


### Transient Analysis
![Screenshot 2025-03-23 153125](https://github.com/user-attachments/assets/8c131f5d-e25f-4604-879f-d01f484c4356)

### AC Analysis
![Screenshot 2025-03-23 155846](https://github.com/user-attachments/assets/65e79d5c-d3ef-451c-bf11-d9b36f27a418)


### 1:2 W/L Ratio
![Screenshot 2025-03-23 154601](https://github.com/user-attachments/assets/f3b0471f-f9c2-4767-9019-3c929cf64cc1)
#### DC Analysis
![Screenshot 2025-03-23 154529](https://github.com/user-attachments/assets/063bd85a-409b-4803-b57b-61718d55594e)


### Transient Analysis
![Screenshot 2025-03-23 155012](https://github.com/user-attachments/assets/afb1eb82-8b97-4280-a9b8-3cfef9475189)

### AC Analysis
![Screenshot 2025-03-23 234324](https://github.com/user-attachments/assets/fc4673c6-132f-44ed-a8bb-c001de8d5a47)

### Inference for L = 500 nm
- The 1:2 ratio again results in higher gain due to increased transconductance (gm).
- The slightly lower gain compared to L = 180 nm suggests increased output resistance.
- The transient response confirms that the circuit amplifies the signal appropriately.

## L = 1 μm
### 1:1 W/L Ratio
![Screenshot 2025-03-23 221625](https://github.com/user-attachments/assets/5300706d-1f59-49ac-864c-792d2f2e8bd0)
### DC Analysis
![Screenshot 2025-03-23 221605](https://github.com/user-attachments/assets/9b5fba75-59c2-437c-aad1-48f1ae2fb435)

### Transient Analysis
![Screenshot 2025-03-23 221756](https://github.com/user-attachments/assets/49684e7c-0773-42e4-bc6f-1caf52b4e202)

### AC Analysis
![Screenshot 2025-03-23 222039](https://github.com/user-attachments/assets/31858b96-2313-4fe4-96e3-0ba49bc3e8e6)

### 1:2 W/L Ratio
![Screenshot 2025-03-23 222455](https://github.com/user-attachments/assets/9f89a288-07d3-4574-880a-26f6596ef5be)
### DC Analysis
![Screenshot 2025-03-23 222445](https://github.com/user-attachments/assets/ec56772a-6dda-4478-a7b8-f451a024abc6)

### Transient Analysis
![Screenshot 2025-03-23 222711](https://github.com/user-attachments/assets/6945e913-d36b-4bad-95e8-c49c9adce00c)

### AC Analysis
![Screenshot 2025-03-23 223005](https://github.com/user-attachments/assets/ea922b4c-dd11-4253-827b-2acc1c90fa6e)

# MOS Differential Amplifier With Current Mirror
## Aim

Design and analyze the MOS differential amplifier circuit for the given specifications:

- **Supply Voltage (Vdd):** 3.3V
- **Power Consumption (P):** ≤ 3mW
- **Input Common Mode Voltage (Vicm):** 1.72V
- **Output Differential Common Mode Voltage (Vdcm):** 1.81V
- **Threshold Voltage (Vp):** 0.7V
- **Current Mirror Implementation:** Used for biasing the differential amplifier

## Theory

A **current mirror** is a circuit that replicates (mirrors) the current from one active device to another, ensuring a constant current source or sink. In the context of a **MOS differential amplifier**, the current mirror plays a crucial role in biasing and ensuring proper operation.


## Calculation

- **Determine Iss (Source Current):**\
  Iss = Power / Vdd\
  Iss = 3mW / 3.3V = 0.909mA

## Circuit 

![Screenshot 2025-03-24 234316](https://github.com/user-attachments/assets/49249614-f17f-4b81-890a-8fe5d7a3681f)

## DC Analysis

![Screenshot 2025-03-24 234328](https://github.com/user-attachments/assets/9e0c06ad-e09a-439d-9a5d-adbff2425cdd)

## Transient Analysis
![Screenshot 2025-03-24 234402](https://github.com/user-attachments/assets/2ea344f8-40b4-4a46-a28f-565a534f19aa)


## AC Analysis
![Screenshot 2025-03-25 001855](https://github.com/user-attachments/assets/d3ae10f8-5ae0-4248-9e66-eb1282e93ae4)


