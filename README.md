# Tarun-Bandeppanavar-Suresh-4NI23EC110
# Aim :
  Basic CS amplifier Characterization in LTspice
using 180 nm technology library.
# Components Required : 
  Mosfet(nmos4 ,pmos4 ), Resistor(1k), voltage supply(1.8V,0.9V) and connecting wires.
# Theory :
A MOSFET is a type of transistor used for amplifying or switching electronic signals. 

It is widely used in digital and analog circuits due to its high efficiency and fast switching speed.

In saturation mode, an NMOS transistor operates under the conditions:

Vgs > Vth (Gate-to-Source Voltage greater than Threshold Voltage)

Vds ≥ Vov (Drain-to-Source Voltage greater than Overdrive Voltage)

The current equation in saturation mode is given by Id = (1/2) kn Vov², 

where:
Vov = Vgs - Vth

The voltage gain is given by: Av = -gm Rd  or Av = Vout/Vin

A MOSFET in saturation and acts as a constant current source, making it useful for amplifier circuits.

Drain current equation: *Id = (1/2) kn Vov², where *Vov = Vgs - Vth.

The amplifier gain follows Av = -gm Rd.

# Procedure:
• Create a New Project

• Set Up the values for MOSFET

• Configure the NMOS transistor (CMOSN) with:
  Length: 180nm
  Width: 0.2um
  
• Perform DC Analysis

• Connect all circuit components properly.
  Apply:
  Vdd = 1.8V
  Vin = 0.9V
  
• Run DC analysis to obtain:
  Vout
  Id
  
• Run Transient Analysis
  Apply a sine wave input:
  Vin = 0.9V
  Amplitude = 50mV
  Frequency = 1kHz
  Run transient analysis
  
• Run AC Analysis
  Include all required library files.
  Run AC analysis with:
  Start and end frequency: 0.1Hz to 1THz

# Calculation :
 
          
