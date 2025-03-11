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

As we decrease the gate voltage (VG), which in this case is Vicm, of a MOSFET operating in the saturation region, the drain current (ID) flowing through the transistor also decreases. This relationship is crucial in understanding the circuit behavior.



### Key Observations:
- The output common-mode voltage is given by:
  
  ```
  Vout_cm = VDD - ID * RD
  ```
  
- When \( I_D \) decreases, \( V_{out,cm} \) increases.
- When \( V_G \) increases, \( I_D \) also increases, leading to a decrease in \( V_{out,cm} \).
- The tail current responds to these changes:
  - It lowers its \( V_P \) when \( V_G \) decreases.
  - It increases \( V_P \) when \( V_G \) increases.

This behavior is essential in differential amplifier circuits and other analog applications where precise control of \( V_G \) is needed to maintain desired output characteristics.



**Finding Vicm maximum and minimum values**
Vicm max

![image](https://github.com/user-attachments/assets/66d00bfc-0119-4e35-b71d-cfcd5431eb4c)
Vicm min

![image](https://github.com/user-attachments/assets/4547f12b-c0cc-4a7d-a65d-20630d086f4c)

**Finding maximum input swing and maximum output swing**
![image](https://github.com/user-attachments/assets/80f2e143-1f32-4bb3-b083-edf07fac2304)



We found that the maximum input swing is 0.38vp-p and Maximum output swing is 1.376v.





# Gain

![image](https://github.com/user-attachments/assets/3483f9a6-87e5-4c67-a91f-606bdc926fec)








