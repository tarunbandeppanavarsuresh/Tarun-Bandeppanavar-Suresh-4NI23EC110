
# Aim
  Design and analyze the mos differential amplifier circuit for the following specification.
# Components Required
  NMOS,Resistor,voltage source,current source
# Theory
  A differential amplifier rejects common-mode signals by design, leveraging the fact that it amplifies only the difference between the voltages at the two inputs (non-inverting and inverting), while it rejects any signals that are common to both inputs. This ability to reject common-mode signals is due to its common-mode rejection mechanism. 
# Question
  Design and analyse the differential amplifier for the following specification Vdd = 1.8v P <=2.8mw ,Vicm = 0.95v ,Vp = 0.4v,Vocm = 1.1v perform DC analysis , transient analysis,frequency response and extract the parameters 
# Circuit 1(Resistor)
![WhatsApp Image 2025-03-02 at 22 50 09_fb120edd](https://github.com/user-attachments/assets/8c4b758e-f0c6-4ee9-9d65-1365b5a0e593)
# Calculation(theoretical)
  Vdd = 1.8v
  Vp = 0.4v
  P = 2.2mw
  Vicm = 0.95v
  Vocm = 1.11v
  Iss = P/v
   = 2.2*10^-3 /1.8
  Iss = 1.2222 mA
Id1 = Id2=Iss/2=0.611mA
Rd =( Vdd -Vocm)/Id1
   = (1.8-1.11)/0.611*10^-3
   = 1.145k ohm
Rss = Vp/Iss
    = 0.4/1.22*100^-3
Rss = 327.33 ohm

# DC Analysis
  since to get apropiate Id obtained in theoretical we should vary w/l
  so for this circuit
    W = 180nm
    L = .109*10^-3 m
![WhatsApp Image 2025-03-02 at 22 49 22_652ecb05](https://github.com/user-attachments/assets/42f119bd-2ca4-4ca5-8060-1b5a8d8fcc1c)



Q point = (Vgs,Id) = (0.5497v,0.611mA)
Now we can vary vdd so that we can know how the q point varies accordingly
for Vdd


 





