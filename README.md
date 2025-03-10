# Lab1
# Experiment 1
# Aim :
  Basic CS amplifier Characterization in LTspice
using 180 nm technology library.
# Components Required : 
  Mosfet(nmos4 ,pmos4 ), Resistor(1k), voltage supply(1.8V,0.7V) and connecting wires.
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
  Vin = 0.7V
  
• Run DC analysis to obtain:
  Vout
  Id
  
• Run Transient Analysis
  Apply a sine wave input:
  Vin = 0.7V
  Amplitude = 50mV
  Frequency = 1kHz
  Run transient analysis
  
• Run AC Analysis
  Include all required library files.
  Run AC analysis with:
  Start and end frequency: 0.1Hz to 1THz

# Calculation :

The Drain current (Id) Can be determined:

P = V * I

I = P / V

I = 50μW / 1.8V

I = 27.7μA


# Transient Analysis
To observe the amplifier's behavior over time, a Transient analysis is performed with the following parameter:

Stop Time = 5ms.

This enables us to investigate the response of the amplifier to the Sinusoidal input signal in the time domain, capturing its transient performance.


# AC Analysis
The AC analysis helps us study the frequency response of the amplifier. The parameters used for this simulation are:

Sweep Type = Decade.

Number of Points per Decade = 20.

Start Frequency = 0.1 Hz.

Stop Frequency = 1THz.

A probe is placed at the Drain (output) and another at Vg (input) to visualize the frequency response.

This helps in understanding the amplifier's gain and bandwidth.

# Inference :

The width of a MOSFET directly influences its current-carrying capacity, which in turn impacts the overall circuit's efficiency.

When operating in the saturation region, the MOSFET's performance is optimized.

Conducting transient analysis is essential for assessing the circuit's responsiveness to dynamic signals, particularly in high-speed applications.

AC analysis plays a vital role in designing amplifiers with tailored gain and understanding their frequency-dependent behavior.

By performing comprehensive analysis, designers can ensure the amplifier circuit is properly designed, optimized, and stable.

# Circuit 2: CMOS Amplifier Simulation
# (the graph and circuit diagram are uploaded above)
 
# Aim :
Conduct DC analysis, Transient analysis, and AC analysis of a Common Source (CS) amplifier circuit and extract key parameters using LTSpice.

# Components :
MOSFET: nmos4, pmos4
Resistor: 1k ohm
Voltage Supply: 1.8V, 0.9V
**Connecting Wires`

# Drain Current Expression :

Id = (1/2) * kn * Vov^2

# Theory :
MOSFETs play a crucial role in electronics due to their:

Compact size
Low power consumption
Simple structure
Compatibility with VLSI technology

# AC Analysis
A sinusoidal input is included in the AC analysis through a modification of gate voltage.

# Sinusoidal Input Voltage

DC Offset: 0.9V
Amplitude: 50mV
Frequency: 1kHz
Frequency Sweep Parameters

Type: Decade
Sweeps per Decade: 20
Start Frequency: 0.1Hz
Stop Frequency: 1THz
By analyzing the AC, one can determine gain, bandwidth, phase, and other characteristics of the amplifier's frequency response.

# DC Analysis
Our approach in conducting DC analysis involves identifying the quiescent operating point (ID) and node voltages that are required to operate the MOSFET.

Supply Voltage (VDD): 1.8V
Gate Voltage (VG): 0.9V
Power Budget (P): 50μW
P = VDD * ID

ID = P/VDD

ID = 50μW / 1.8V

ID = 27.7μA
Vout=1.77223



# Transient Analysis
By examining the transient response of the amplifier, it is possible to determine its behavior over time when subjected to the sinusoidal input.

# Parameters

Stop Time: 5m (5 milliseconds)
The transient analysis provides information about the amplifier's time-domain behavior, such as distortion, settling time, and waveform reproduction.

# Loop gain 
  loop gain = 36.72 db


# Inference 

The width of a MOSFET has a direct impact on its drain current, with NMOS transistors exhibiting a more pronounced effect than PMOS transistors. Increasing the width of a MOSFET enhances its gain. Furthermore, an inversion of the input signal is observed at the output, resulting in a 180-degree phase shift between the input and output waveforms.

