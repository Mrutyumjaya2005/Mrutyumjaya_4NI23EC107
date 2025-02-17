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
