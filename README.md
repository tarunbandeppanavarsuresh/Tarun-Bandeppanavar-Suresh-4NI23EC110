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
# Design and Analysis of Current Mirror Circuit

### AIM:

**Design Question :**  
Design and analyze the current mirror circuit with the following specifications:
- **Voltage Gain (Av)** > -10 V/V
- **V<sub>DD</sub>** = 1.8 V
- **Power consumption (P)** ≤ 1 mW

Perform the DC analysis, transient analysis, and AC analysis while maintaining the same (W/L) ratio for different values of Length (L). Additionally, calculate the maximum output swing and bandwidth.

### 2. THEORY:

A **current mirror** is a circuit used to replicate a reference current across a different branch, maintaining a constant current regardless of load variations. It is widely used for biasing circuits and active loads in amplifiers.


- A reference current **I<sub>REF</sub>** is set through **M1**, setting its gate-source voltage **V<sub>GS</sub>**.
- The gates of **M1** and **M2** are connected, ensuring that both transistors share the same **V<sub>GS</sub>**.
- As both transistors are identical, **M2** will conduct a current equal to **I<sub>REF</sub>**.
- The output current remains constant, independent of load changes.

### 3. CIRCUIT DESIGN:

<img width="300" alt="image" src="https://github.com/user-attachments/assets/d704f45f-412a-4603-af62-702fedc6eeda" />


#### Step 1: Determine Total Current (I<sub>TOTAL</sub>)
- **I<sub>TOTAL</sub>** = P/V<sub>DD</sub> = 1 mW / 1.8 V = 0.555 mA

#### Step 2: Determine Reference Current (I<sub>REF</sub>)
- For a **1:1 ratio**:
  - **I<sub>REF</sub>** = I<sub>TOTAL</sub>/2 = 0.555 mA / 2 = 0.2775 mA
 
![image](https://github.com/user-attachments/assets/0649d851-dfb6-4162-84c4-1ffdc10c0633)
 
  
For a **1:2 ratio**:
  - **I<sub>REF</sub>** = I<sub>TOTAL</sub>/3 = 0.555 mA / 3 = 0.185 mA
  - **I<sub>D</sub>** = 2 * I<sub>REF</sub> = 0.37 mA

![image](https://github.com/user-attachments/assets/f6371f01-9c69-4de6-9c90-fde983918384)



#### 3.1 **1:1 Ratio Current Mirror:**
##### Circuit Parameters:

| **Parameter**  | **PMOS (M1)** | **PMOS (M2)** | **NMOS (M3)** |
|----------------|---------------|---------------|---------------|
| Length         | 180 nm        | 180 nm        | 180 nm        |
| Width          | 2.35 µm        | 2.35 µm        | 2.9 µm        |

#### DC Analysis Results:

![R1_1](https://github.com/user-attachments/assets/a50c858f-22f5-4d15-b670-1d9a564a0269)

Change i length of MOSFET we will observe change in V<sub>out</sub> and I<sub>D</sub>

| **Length (L)** | **Width (W1)** | **Width (W2)** | **Width (W3)** | **I<sub>REF</sub>** | **I<sub>D</sub>** | **V<sub>out</sub>** |
|----------------|----------------|----------------|----------------|--------------------|------------------|--------------------|
| 180 nm         | 2.35 µm         | 2.35 µm         | 2.9 µm         | 0.277 mA           | 0.27711 mA       | 0.552 V            |
| 500 nm         | 2.35 µm         | 2.35 µm         | 8.37 µm       | 0.277 mA           | 0.284 mA         | 0.289 V            |
| 1 µm           | 2.35 µm         | 2.35 µm         | 19.11 µm       | 0.277 mA           | 0.285 mA         | 0.213 V            |

##### Transient Analysis:

![image](https://github.com/user-attachments/assets/edeba8c8-251b-47ad-b4b9-4b16a21c471e)

- **Gain (Av)** = -300 mV / 25 mV = -12 V/V

##### AC Analysis:

![image](https://github.com/user-attachments/assets/7d2621a9-57d7-4648-863d-f748e7732f27)

- **Gain (Av)** = 21.6 dB
- **-3 dB Bandwidth Frequency** = 770.570 MHz

#### 3.2 **1:2 Ratio Current Mirror:**
##### Circuit Parameters:

| **Parameter**  | **PMOS (M1)** | **PMOS (M2)** | **NMOS (M3)** |
|----------------|---------------|---------------|---------------|
| Length         | 180 nm        | 180 nm        | 180 nm        |
| Width          | 2.5 µm        | 5 µm          | 3.897 µm      |

#### DC Analysis Results:

![image](https://github.com/user-attachments/assets/8fdc2223-f361-4b75-a34a-a2b1a26ec5a9)


| **Length (L)** | **Width (W1)** | **Width (W2)** | **Width (W3)** | **I<sub>REF</sub>** | **I<sub>D</sub>** | **V<sub>out</sub>** |
|----------------|----------------|----------------|----------------|--------------------|------------------|--------------------|
| 180 nm         | 2.5 µm         | 5 µm           | 3.897 µm       | 0.185 mA           | 0.370 mA         | 0.682 V            |
| 500 nm         | 2.5 µm         | 5 µm           | 10.825 µm      | 0.185 mA           | 0.380 mA         | 0.288 V            |
| 1 µm           | 2.5 µm         | 5 µm           | 21.65 µm       | 0.185 mA           | 0.382 mA         | 0.212 V            |

##### Transient Analysis:

![image](https://github.com/user-attachments/assets/1cf0bd13-b2df-4e3f-b8fc-6d3d11b21ccd)

- **Gain (Av)** = -280 mV / 25 mV = -11.2 V/V

##### AC Analysis:

![image](https://github.com/user-attachments/assets/9235b7dd-2f3e-48e2-8204-7926f8caaa73)

- **Gain (Av)** = 21 db  (20.984 dB) 
- **Bandwidth Frequency** = 815.968 MHz

### 4. DESIGN B: Differential Amplifier

Using the same design specifications:
- **V<sub>DD</sub>** = 3.3 V
- **P** ≤ 3 mW
- **V<sub>ICM</sub>** = 1.65 V
- **V<sub>ocm</sub>** = 1.7 V
- **V<sub>P</sub>** = 0.5 V

#### Circuit Parameters:

| **Parameter** | **PMOS (M3)** | **PMOS (M4)** | **NMOS (M1)** | **NMOS (M2)** | **NMOS (M5)** | **NMOS (M6)** |
|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Length        | 180 nm        | 180 nm        | 180 nm        | 180 nm        | 1 µm          | 1 µm          |
| Width         | 2.214 µm      | 2.214 µm      | 1.82 µm       | 1.82 µm       | 200 µm        | 100 µm        |

#### DC Analysis Results:

![image](https://github.com/user-attachments/assets/c86ec858-5f5d-4636-87f8-10492e8f7805)



#### Transient Analysis Results:

![image](https://github.com/user-attachments/assets/57c7b767-d19f-4bb3-9cd9-43514a6cab93)

- **Gain (Av)** = -65 mV / 2 mV = - V/V

#### AC Analysis Results:

![image](https://github.com/user-attachments/assets/1cb91b94-ca65-4fa8-b988-378302523f9f)

- **Gain (Av)** = 8.299 dB

### 5. INFERENCE:

- **Length Increase**: When the length of the NMOSFET is increased, keeping the W/L ratio constant:
  - **V<sub>out</sub>** decreases.
  - **Drain current (I<sub>D</sub>)** increases slightly.
  - **Output resistance** increases due to reduced channel-length modulation.
  - Longer **L** improves **current matching** and **stability** in the current mirror.

#### Comparison of Features between 1:1 and 1:2 Ratio Current Mirror:

| **Feature**                  | **1:1 Ratio Current Mirror** | **1:2 Ratio Current Mirror** | **Inference** |
|------------------------------|-----------------------------|-----------------------------|--------------|
| **Current Accuracy**          | Higher accuracy            | Slight mismatch              | 1:1 provides better current matching |
| **Transistor Sizing**         | Smaller uses less area         | Larger uses more area            | 1:1 is more efficient in chip  |
| **Power Consumption**         | Lower, due to smaller devices | Higher, due to larger devices | 1:2 uses more power. |


- The **differential amplifier** performs better with a **current mirror** instead of a resistor load.
- Using **current mirrors** enhances the **gain and stability** of the amplifier and **reduces offset variations**.

-- 
### **Conclusion**
- The experiment **successfully demonstrates how varying the current mirror ratio impacts the performance of an amplifier**.
- **Current mirror loads provide significant gain enhancement over resistive loads**, making them ideal for **differential amplifiers and operational amplifiers**.
- **A balance between gain and bandwidth must be considered** based on circuit requirements.
- The **results validate theoretical expectations**, confirming the accuracy and efficiency of current mirrors in analog design.

---
