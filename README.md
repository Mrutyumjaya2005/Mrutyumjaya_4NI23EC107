# 1.Analysis of CS amplifier
## Aim : 
To perform DC, AC and transient analysis of a CS amplifier circuit using LTSpice 
## Components Required :
N-MOSFET(nmos4,pmos4),Resistor(1k),Power Supply(DC:1.8V, 0.9V)
## Theory :
A NMOS common-source (CS) amplifier amplifies small input signals by operating the NMOS transistor in the saturation region, where it acts as a voltage-controlled current source. Proper amplification requires that the transistor satisfies Vds ≥ Vgs - Vth, the drain current (Id) is controlled by the gate voltage (Vgs).
1. DC Analysis  
   - Ensures the MOSFET operates in the saturation region.  
   - Determines the DC operating point.  
   - Helps in biasing resistor selection and stabilizing the circuit against parameter fluctuations.  
2. Transient Analysis  
   - Examines the circuit response to time-varying signals.  
   - Helps detect signal distortion, DC shift, and phase distortion.  
3. AC Analysis  
   - Determines the small-signal gain (Av = -gm * Rd).  
   - Analyzes the frequency response of the amplifier.  
   - Helps in designing circuits for desired bandwidth and stability.  
## Circuit 1 :
<img width="697" alt="image" src="https://github.com/user-attachments/assets/bf3a4080-9d46-453f-bc41-7a489a9dfc04" />

## Procedure :
1.Open the ltspice software,merge the library file for getting accurate values of NMOS and PMOS.

2.Select the components which are needed to us like for circuit 1 we need 1k resistor,1 CMOSN,two voltage sources(1.8v,0.6v),ground from the components list.

3.Place them all components in necessory way which is helpfull ,connect all the components as in given circuit .

4.Link the specification of list of properties of mosfet like threshold voltage, temperature etc.

5.lets do the DC Analysis first by opting a simulation , we get .op so after placing it we will get the values of it. thet will displayed.

6.After that lets take Transient analysis of 5m cycle so in input and output waveforms in 5 complete cycle, so here we get and seperate and combined waveforms of input and output.

7.For AC analysis, we should do some changes like converting DC SOURCE to sinosoidal waveform (1.2,50m,1T),after that select the AC simulation from the given options of simulation after giving values of ( Decade,20,01,1T).So we will get a output after placing node to output waveform .

8.Here we put the values of l=500nm,w=1.08um,etc

## DC Analysis :
<img width="737" alt="image" src="https://github.com/user-attachments/assets/963f7951-c848-4dae-ab47-1c79a68d69c4" />

Id = 2.7*e-5 A

Vds = 1.772v

W = 1.08um and L=500nm.

source voltage = 1.8v and 0.9v

P = V * I

I = P / V

I = 50μW / 1.8V

I = 27.7μA

## AC Analysis :

<img width="953" alt="image" src="https://github.com/user-attachments/assets/b86adc96-28af-4287-9771-9cff6d3ec8e2" />

1.Sweep Type = Decade.

2. Number of Points per Decade = 20.

3. Start Frequency = 0.1 Hz.

4. Stop Frequency = 1THz

## Transient Analysis :

### Input Waveform :

<img width="960" alt="image" src="https://github.com/user-attachments/assets/1ea4788c-3913-4fb3-9c60-bdca1564bda6" />

### Output Waveform :

<img width="956" alt="image" src="https://github.com/user-attachments/assets/f602b903-3544-40b6-988c-168f537f106c" />

## Calculations:

GIVEN : power= 50um, l=500nm, vdd= 1.8v.

so that P=VI, I=2.7*e-5 after calculation.

Frequency 1 kHz, V1=1.8V, V2=0.6V.
## Circuit 2 :
<img width="757" alt="image" src="https://github.com/user-attachments/assets/4011a599-cd02-43c8-898f-094c58a4eee4" />


## DC Analysis :
<img width="929" alt="image" src="https://github.com/user-attachments/assets/b435384d-9cbd-4441-a93c-d9aadcda0d6b" />

## Transient Analysis : 

## Input Waveform : 
<img width="959" alt="image" src="https://github.com/user-attachments/assets/de1e6927-c5ab-4814-b2ed-77e05395f981" />

## Output Waveform :
<img width="956" alt="image" src="https://github.com/user-attachments/assets/841e355b-8a60-47c5-8bf3-759d59d3d429" />

## AC Analysis : 
<img width="959" alt="image" src="https://github.com/user-attachments/assets/247f6925-8b3a-4d8d-ae98-2ce946499129" />

## Gain :
<img width="494" alt="image" src="https://github.com/user-attachments/assets/32a65f14-0136-40c4-bc09-577375b91196" />



## Inference :

In a MOSFET, during the saturation region, the drain current (Id) is directly proportional to the channel width (W) and varies linearly with the W/L ratio. Our task is to find the W value using the given values of L, Id, V1, and V2. A MOSFET works as an amplifier only in the saturation region. By performing DC analysis on a given circuit, we can determine the DC operating point. AC analysis helps determine parameters such as bandwidth and gain. These values can be extracted from the given graph. Transient analysis provides the input and output waveforms, allowing us to determine voltage values. The MOSFET gain increases with the mid-band frequency range.



# 2.Basic Differential amplifier design using LTspice. 

## Aim : 
Design and Analyze the MOS differential amplifier circuitfor the following specifications 

## Components Required : 
N-MOSFET(nmos4),Resistor(1.9k,0.4k),Power Supply(DC:2.2V, 1.2V),Current source(1,mA),Signal generator

## Theory : 
A differential amplifier is an electronic circuit that amplifies the difference between two input signals while rejecting any signals that are common to both inputs (common-mode signals). It is a fundamental building block in analog circuits, commonly used in instrumentation, operational amplifiers (op-amps), and signal processing applications.

### Basic Circuit Configuration :
A basic differential amplifier consists of :

1.Two inputs V1 and V2 

2.Two Resistors to set gain 

3.Power supply 

4.An operational amplifer


## Two different modes of differentail amplifier :
### 1.Common mode :
Common modes siganl : (V1 + V2)/2
### 2.Diferential mode :
The difference between two inputs : V1 - V2 

## Working principle : 

1. The output voltage is proportional to the difference between the two input voltages.

2. If both the inputs receive the same siganl (common-mode signal), the ideal differential amplifier suppresses it.

3. The gain of the amplifier depends on the circuit configuration and reisistor values.

Vout = Ad (V1-V2)

Here Ad is differential gain 
### Procedure :

1.Open the LTspice software, merge the library file for getting accurate values of NMOS.

2.Select the components which are needed to us like for circuit 1 we need 1.9k & 0.4k resistor,2 CMOSN, three voltage sources(1.2v,2.2v),ground from the components list.

3.Place them all components in necessory way which is helpfull, connect all the components as in given circuit .

4.Link the specification of list of properties of mosfet like threshold voltage, temperature etc.

5.Lets do the DC Analysis first by opting a simulation, we get .op so after placing it we will get the values of it, thet will displayed.

6.After that lets take Transient analysis of 5m cycle so in input and output waveforms in 5 complete cycle, so here we get and seperate and combined waveforms of input and output.

7.For AC analysis, we should do some changes like converting DC SOURCE to sinosoidal waveform (1.2,50m,1T),after that select the AC simulation from the given options of simulation after giving values of (Decade,20,01,1T). So we will get a output after placing node to output waveform .
   
## Circuit 1 : 

![WhatsApp Image 2025-02-28 at 15 16 03_e3a84599](https://github.com/user-attachments/assets/6917714d-b7bd-490f-a6b4-31d43140dfc1)

## DC Analysis :

![WhatsApp Image 2025-02-28 at 15 15 10_4dfb6ea7](https://github.com/user-attachments/assets/f52cc7c4-a3c7-4ad5-9108-c6e548bce3a9)

Id1 = 0.5mA 

Id2 = 0.5mA 

Vocm = 1.25 V

vocm2 = 1.25 V

## Transient Analysis : 

### Input waveform :

<img width="959" alt="image" src="https://github.com/user-attachments/assets/ef69bdd7-b670-46f3-aeee-594077248434" />

Vin = 1.25 - 1.15 V
​
### output waveform :

<img width="958" alt="image" src="https://github.com/user-attachments/assets/707c6743-8837-4a8f-ab7d-4ebffa7cc3c7" />

Vout = 1.32 - 1.18 V

### Input and Output combined waveforms :

<img width="958" alt="image" src="https://github.com/user-attachments/assets/0f87ed18-5165-41bf-a273-44ff5aca5ad3" />

Gain = Vout / Vin 

     = (1.32 - 1.18) / (1.25 - 1.15)

     = 1.4 

Gain in dB = 20 * log (1.4)

           = 2.92 dB
           
## AC Analysis :

<img width="956" alt="image" src="https://github.com/user-attachments/assets/30515397-0c44-4db9-9fb8-5ceaca1d5a57" />

## Circuit 2 :

<img width="711" alt="image" src="https://github.com/user-attachments/assets/676238e1-448b-49a3-8e1d-b98288153865" />

## DC Analysis :

<img width="476" alt="image" src="https://github.com/user-attachments/assets/b4a5c03f-b720-4f49-ab0b-f8447bfdf0bb" />

Id1 = 0.5 mA

Id2 = 0.5 mA

Vocm =  1.25 V

vocm2 =  1.25 V

## Transient Analysis :

### Input waveform :

<img width="959" alt="image" src="https://github.com/user-attachments/assets/303feebc-8d6d-4900-a5eb-d8358d1b2a00" />

Vin = 1.25 - 1.15 V

### Output waveform :

<img width="960" alt="image" src="https://github.com/user-attachments/assets/f4effb79-c054-4d6c-b046-25b8c6eafb3b" />

Vocm = 1.44 -1.04

### Input and Output combined waveforms :

<img width="960" alt="image" src="https://github.com/user-attachments/assets/33c0d542-0d88-4174-ab7a-d9aa32f3ce6e" />

Gain = vocm / Vin 

     = (1.44 - 1.04) / (1.25 - 1.15)

     = 4

Gain in dB = 4 * log (1.4)

           = 12.04 dB
           

## AC Analysis :

<img width="959" alt="image" src="https://github.com/user-attachments/assets/b922bb41-3ac8-46e9-88e2-cca99184bc2c" />


## Circuit 3 :

<img width="675" alt="image" src="https://github.com/user-attachments/assets/10d9d352-88fc-4971-b161-098aabe0e551" />

## DC Analysis :

<img width="476" alt="image" src="https://github.com/user-attachments/assets/71235100-a527-4b8d-8dba-92873747affb" />

Id1 = 0.5 mA 

Id2 = 0.5 mA

Vocm =  1.25 V

vocm2 = 1.25 V 

## Transient Anaysis :

### Input waveform :

<img width="957" alt="image" src="https://github.com/user-attachments/assets/b2c0c423-6897-46be-b74d-94518ef990f5" />

Vin = 1.25 - 1.15

### Output waveform :

<img width="956" alt="image" src="https://github.com/user-attachments/assets/c34cc8ac-4c2f-4424-8dd0-47caad2f9770" />

Vout = 1.44 - 1.04

### Input and Output combined waveform :

<img width="960" alt="image" src="https://github.com/user-attachments/assets/090f0d92-f27f-4346-835e-42a4fc593231" />

Gain = vocm / Vin 

     = (1.44 - 1.04) / (1.25 - 1.15)

     = 4

Gain in dB = 4 * log (1.4)

           = 12.04 dB
           

## AC Analysis :

<img width="959" alt="image" src="https://github.com/user-attachments/assets/49dbdf2f-e301-4c39-a878-a3e129983475" />

## Inference 

1.Differential Gain – The amplifier provides significant gain for differential signals, confirming its suitability for applications requiring precise signal amplification.

2.Common-Mode Rejection – The circuit successfully suppresses common-mode signals, making it ideal for noise-resistant applications.

3.Biasing and Stability – Proper biasing ensures stable operation, and any variations in resistor values or transistor parameters influence the gain.

4.Practical Limitations – Small deviations from theoretical values were observed due to component tolerances, non-ideal transistor characteristics, and power supply variations.
