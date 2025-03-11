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



 ## **Design**
![1](https://github.com/user-attachments/assets/6d1403f0-fde2-4250-a651-bb2438928f18)




## **Circuit Diagram** :

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



**Finding Maximum input and output swing**

### Common-Mode Input Voltage Calculation:
- **Maximum Vicm:**
  
  ```
  Vicm_max = Vocm + Vth = 1.25 + 0.447 = 1.697V
  ```
  
- **Minimum Vicm:**
  
  ```
  Vicm_min = Vth + Vp = 0.447 + 0.4 = 0.847

 - **Maximum input swing =0.856 v**
  
-**Maximum vout** 
Vout_max=Vdd =2.2v
-**minimum vout**
Vout_min=Vov=VGS-VT=1.2-0.4-0.477=0.353v

-**Maximum output swing is 1.847 v**
  

**Through simulation**
Vicm max

![image](https://github.com/user-attachments/assets/66d00bfc-0119-4e35-b71d-cfcd5431eb4c)

Vicm min

![image](https://github.com/user-attachments/assets/4547f12b-c0cc-4a7d-a65d-20630d086f4c)


-# Differential Amplifier Gain Equation 
The differential gain equation for a **differential amplifier** with a **tail resistor \( R_S \)**, using the **small-signal model**.

## Equation  

The differential voltage gain \( A_v \) is given by:  


A_v = {g_m *R_D}/{1 + 2g_m R_S}


Where:  
- \( g_m \) = Transconductance of the MOSFET  
- \( R_D \) = Drain resistance  
- \( R_S \) = Tail resistor (source resistance in MOSFET)  

## Observations  
- **Without \( R_S \) (ideal current source at the tail):**  
  \[
  A_v = g_m * R_D
  \]
- **With \( R_S \):** The gain decreases due to degeneration.  
- **If \( R_S \) is large**, gain is significantly reduced.  
- **If \( R_S \) is small**, gain is close to \( g_m R_D \).  

## Conclusion  
The presence of a **tail resistor \( R_S \)** reduces the differential gain by introducing **negative feedback**.










