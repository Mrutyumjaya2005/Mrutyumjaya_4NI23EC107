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

7.For AC analysis, we should do some changes like converting DC SOURCE to sinosoidal waveform( 0.6,50m,1T),after that select the AC simulation from the given options of simulation after giving values of ( Decade,20,01,1T).So we will get a output after placing node to output waveform .

8.Here we put the values of l=500nm,w=1.08um,etc

## DC Analysis :
<img width="737" alt="image" src="https://github.com/user-attachments/assets/963f7951-c848-4dae-ab47-1c79a68d69c4" />

Id = 2.7*e-5 A

Vds = 1.772v

W = 1.08um and L=500nm.

source voltage = 1.8v and 0.9v

## AC Analysis :

<img width="953" alt="image" src="https://github.com/user-attachments/assets/b86adc96-28af-4287-9771-9cff6d3ec8e2" />

## Transient Analysis :

### Input Waveform :

<img width="960" alt="image" src="https://github.com/user-attachments/assets/1ea4788c-3913-4fb3-9c60-bdca1564bda6" />

### Output Waveform :

<img width="956" alt="image" src="https://github.com/user-attachments/assets/f602b903-3544-40b6-988c-168f537f106c" />

## Calculations:

GIVEN : power= 50um, l=500nm, vdd= 1.8v.

so that P=VI, I=2.7*e-5 after calculation.

Frequency 1 kHz, V1=1.8V, V2=0.6V.

## Inference :

1. In a MOSFET, during the saturation region, the drain current (Id) is directly proportional to the channel width (W) and varies linearly with the W/L ratio. Our task is to find the W value using the given values of L, Id, V1, and V2.  

2. A MOSFET works as an amplifier only in the saturation region. By performing DC analysis on a given circuit, we can determine the DC operating point.  

3. AC analysis helps determine parameters such as bandwidth and gain. These values can be extracted from the given graph.  

4. Transient analysis provides the input and output waveforms, allowing us to determine voltage values. The MOSFET gain increases with the mid-band frequency range.  

5. From the analysis, we determine the Q-point as (1.644V, 2.7 × 10⁻⁵ A), with Vout = 0.5V and Vin = 200mV.

## Circuit 2 :
