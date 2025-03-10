# Differential amplifier -Design in LTspice using 180nm technology library


A differential amplifier is a type of electronic amplifier that amplifies the difference between two input voltages while rejecting any voltage that is common to both inputs. It is widely used in analog circuits, particularly in operational amplifiers (op-amps) and instrumentation systems.



## Key Characteristics:
- **Differential Mode Operation:** Amplifies the voltage difference between two inputs:  
  \[
  V_{out} = A_d (V_1 - V_2)
  \]
  where \( A_d \) is the differential gain.
- **Common-Mode Rejection:** It rejects common signals that appear on both inputs.
- **High Common-Mode Rejection Ratio (CMRR):** Useful in reducing noise.
- **Applications:** Used in **signal processing, sensor interfacing, audio amplification, and operational amplifiers**.



  **Design**
- ![WhatsApp Image 2025-03-10 at 22 37 23_a9d78f3e](https://github.com/user-attachments/assets/6f3a7197-72b1-46cd-8da1-8bff15f8f4d9)



**Circuit Diagram** :

- ![image](https://github.com/user-attachments/assets/99956fef-0035-4fb3-b6ed-3ab4fb55d398)




## DC Analysis

Transistor Operating Points --
M1 Qpoint:(**1.25V, 0.5mA**)  ,
M2 Qpoint: (**1.25V, 0.5mA**)

-- Transistor Dimensions --
Length  (L):  310.1092 nm  ,
Width   (W):  1.8782 µm
  


![image](https://github.com/user-attachments/assets/ce44d17d-b1b8-43e4-ab90-3e18e990eb3f)










 **a) As Vicm decreased to 1v**

![image](https://github.com/user-attachments/assets/3cc0c64c-5cb6-4070-a295-3969c69b5532)

**b) As Vicm increased to 1.4v**

![image](https://github.com/user-attachments/assets/8b5b486f-1617-400d-805f-deb1401c2227)

The reason for this observation is ,as we decrease the VG (here it is Vicm) value of a MOSFET in Saturation region the currrent flowing through that transistor will also decreases.AS Voutcm=VDD-ID*RD 
as ID decreses voutcm inccreases ,and if VG value increases ,it results in high current thus VoutCm decreases and the tail current responds to the changes by loweing its vp when vg decreses and incresing when vg incresing .

# Gain







