# Tarun-Bandeppanavar-Suresh-4NI23EC110
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
 
# Aim
Conduct DC analysis, Transient analysis, and AC analysis of a Common Source (CS) amplifier circuit and extract key parameters using LTSpice.

# Components
MOSFET: nmos4, pmos4
Resistor: 1k ohm
Voltage Supply: 1.8V, 0.9V
**Connecting Wires`
