# Differential amplifier -Design in LTspice using 180nm technology library


A differential amplifier is a type of electronic amplifier that amplifies the difference between two input voltages while rejecting any voltage that is common to both inputs. It is widely used in analog circuits, particularly in operational amplifiers (op-amps) and instrumentation systems.



## Key Characteristics:
- **Differential Mode Operation:** Amplifies the voltage difference between two inputs:  

  V_out = A_d (V_1 - V_2)
 
  where ( A_d ) is the differential gain.
- **Common-Mode Rejection:** It rejects common signals that appear on both inputs.
- **High Common-Mode Rejection Ratio (CMRR):** Useful in reducing noise.
- **Applications:** Used in **signal processing, sensor interfacing, audio amplification, and operational amplifiers**.



 ## **Design**
![1](https://github.com/user-attachments/assets/6d1403f0-fde2-4250-a651-bb2438928f18)




## **Circuit Diagram** :

- ![image](https://github.com/user-attachments/assets/99956fef-0035-4fb3-b6ed-3ab4fb55d398)




### DC Analysis

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

### Equation  

The differential voltage gain \( A_v \) is given by:  


A_v = -{g_m *R_D}/{1 + 2g_m R_S}


Where:  
- \( g_m \) = Transconductance of the MOSFET  
- \( R_D \) = Drain resistance  
- \( R_S \) = Tail resistor (source resistance in MOSFET)  

### Observations  
- **Without \( R_S \) (ideal current source at the tail):**  
  \[
  A_v = g_m * R_D
  \]
- **With \( R_S \):** The gain decreases due to degeneration.  
- **If \( R_S \) is large**, gain is significantly reduced.  
- **If \( R_S \) is small**, gain is close to \( g_m R_D \).  

**Conclusion**  
The presence of a **tail resistor \( R_S \)** reduces the differential gain by introducing **negative feedback**.

## Transient Analysis 

When we applied **VG1=Vicm+0.144**  (Since Vicm_max=1.344v and vicm_min=0.703v and 1.3444-1.2=0.144v(least value),thus we will get a linear output)
and **VG2=Vicm-0.144**



![image](https://github.com/user-attachments/assets/62503ed1-320c-4bdf-98ae-c34b14579440)




**A_v = 4.001v/v=12.04db**

## AC Analysis

![image](https://github.com/user-attachments/assets/f4ce08f9-c6f9-477f-a43c-49c350fdbeb3)



From AC anlysis the Gain we obtained is **12.12db** and bandwidth is **0 to 22.205G Hz**.



## When the Resitor is being replaced with a constant current source


### Circuit diagram

![image](https://github.com/user-attachments/assets/5aacb5c9-e15f-4ed4-b440-a5815b4fb5aa)
### DC Analysis
![image](https://github.com/user-attachments/assets/303f3f1c-6078-4ef5-9269-f336ee12df8d)

Transistor Operating Points --
M1 Qpoint:(**1.25V, 0.5mA**)  ,
M2 Qpoint: (**1.25V, 0.5mA**)

-- Transistor Dimensions --
Length  (L):  180 nm  ,
Width   (W):  5.8317 µm

**Finding maximum input swing and Maximum out swing**
![image](https://github.com/user-attachments/assets/0b1ae400-ee46-464c-b9ef-d6ece6b021ce)
![image](https://github.com/user-attachments/assets/eff4d8e2-3535-4b35-aff0-17a68481450d)

Thus the Maximum input swing is **0.959 vp-p**


![image](https://github.com/user-attachments/assets/f0b55ad2-78e5-4244-b841-9d9a5f708021)
**The Maximum output swing is (2.18-0.9v)=1.28vp-p.**
.


- **When Vicm is reducedd to 1v**
- ![image](https://github.com/user-attachments/assets/92d1ea02-444e-4433-b7ec-2fb9b2e7e8b9)
**When Vicm is increased to 1.5v**
  ![image](https://github.com/user-attachments/assets/34485884-bab8-440b-adb1-cf90e007fd34)

  In a **MOSFET-based differential amplifier with a constant current source**, when the **common-mode input voltage (V_ICM) is changed**, the output voltage (**V_out**) remains constant, but the positive input voltage (**V_P**) varies accordingly. This behavior can be explained as follows:

### Explanation

1. **Constant Current Source Effect**
   - The current source ensures that the total tail current remains **constant**, independent of V_ICM (within operating limits).
   - As a result, the sum of the currents through both transistors remains fixed.

2. **Effect on Input Transistors**
   - When **V_ICM decreases**, both the gate and source voltages of the MOSFETs decrease.
   - When **V_ICM increases**, both the gate and source voltages increase accordingly.
   - Since the tail current is constant, the source voltage **tracks** the gate voltage variation.

3. **Why V_P Varies but V_out Remains Constant**
   - **V_P (the voltage at the non-inverting input)** decreases when V_ICM decreases and increases when V_ICM increases.
   - However, **V_out remains constant** because the differential pair's operation is mainly determined by the **differential mode voltage (V_id = V_P - V_N)** rather than the common-mode voltage.
   - The **current division** between the two MOSFETs does not change, so the output voltage (which depends on the drain currents) remains stable.

#### Key Takeaway
- **V_P follows the variation in V_ICM**: It decreases when V_ICM decreases and increases when V_ICM increases.
- **V_out remains unchanged** due to the **common-mode rejection property** of differential amplifiers.

## Gain Equation

The differential voltage gain (**A_d**) of a MOSFET-based differential amplifier is given by:


A_d = -g_m *R_D


where:
- **g_m** = transconductance of the MOSFET, given by \( g_m = \frac{2I_D}{V_{GS} - V_{TH}} \)
- **R_D** = drain resistance
- **I_D** = drain current
- **V_{GS}** = gate-to-source voltage
- **V_{TH}** = threshold voltage of the MOSFET

The common-mode gain (**A_cm**) is ideally low due to the constant current source and is given by:


A_{cm} = o ( if we use a ideal current source with infinite output impedance)


## Key Takeaway
- The **differential gain** is primarily determined by **g_m R_D**, while the **common-mode rejection** is enhanced by a high source resistance.
- Commom mode rejection ration is infinite as A_cm=0 v/v.
  

### Transient Analysis
![image](https://github.com/user-attachments/assets/06d6f8cc-6c49-4759-9594-b0da2124fbbe)

**Gain (A_v) = 4.025v/vv/v= 12.095db**


### Frequency Responce

![Screenshot 2025-03-11 222029](https://github.com/user-attachments/assets/035d3b4f-573e-435e-851e-0f14b3779968)

## Advantages of Using a Current Source Instead of a Resistor

1. **Higher Common-Mode Rejection Ratio (CMRR)** - Reduces common-mode noise.
2. **Better Bias Stability** - Ensures a constant operating point.
3. **Increased Gain** - A current source has high impedance, boosting gain.
4. **Improved Linearity** - Less distortion due to stable tail current.
5. **Wider Swing & Lower Offset** - Provides better voltage headroom.
6. **Power Efficiency** - Reduces voltage drop and power consumption.
7. 
**From the above design and analysis we can understand these points**


## When Current source replaced with mosfet

#### Circuit Diagram

![image](https://github.com/user-attachments/assets/db49016e-f0ba-4ecf-a48e-14dd69a886ff)

### DC Analysis

![image](https://github.com/user-attachments/assets/11fab853-c312-4a21-942b-410250a371db)

Transistor Operating Points --
M1 Qpoint:(**1.25V, 0.5mA**)  ,
M2 Qpoint: (**1.25V, 0.5mA**)

-- Transistor Dimensions --
M1 & M2
Length  (L):  740 nm  ,
Width   (W): 19.99 µm

M3
Length  (L):  500.1005nm ,
Width   (W): 41.054 µm


**Finding Maximum input swing and output swing**

![image](https://github.com/user-attachments/assets/37bce295-95f4-4af4-86fe-1d34807b4fea)
![image](https://github.com/user-attachments/assets/c837b2d9-80a5-4053-b2df-dfc25a0446fd)
**Through DC Sweep we got the maximum input swing as 0.769vp-p**

**When Vi_cm is reduced to 1v**

![image](https://github.com/user-attachments/assets/79565146-8088-43d8-b3d2-63649a940766)
**When Vi_cm is incresed to 1.4v**
![image](https://github.com/user-attachments/assets/efba8a80-301a-4d6c-8335-b43dc30f7dd8)
The MOSFET in saturation acts as an **active current source**, but its output impedance is lower than an ideal current source.
- **When V_ICM decreases:**
  - The gate-source voltage (**V_GS**) of the current source MOSFET decreases.
  - This reduces the tail current, affecting differential pair operation.
  - **V_out increases**, **I_D decreases**, and **V_P decreases**.
- **When V_ICM increases:**
  - **V_GS** of the current source MOSFET increases, slightly increasing tail current.
  - **V_out decreases**, **I_D increases**, and **V_P increases**.
  - This variation can cause **reduced common-mode rejection** and **gain variations**.


### Transient Analysis

![image](https://github.com/user-attachments/assets/f3bdc669-72b6-4085-b619-1fb6f3dcdc3c)

**A_v= 5v/v = 13.97db**

### Frequency Responce 
![image](https://github.com/user-attachments/assets/a76af1da-9751-4818-a21a-0af46541794e)
 Advantages of Using a MOSFET Current Source Instead of a Resistor

1. **Higher Common-Mode Rejection Ratio (CMRR)** - Reduces common-mode noise.
2. **Better Bias Stability** - Ensures a constant operating point.
3. **Increased Gain** - A current source has high impedance, boosting gain.
4. **Improved Linearity** - Less distortion due to stable tail current.
5. **Wider Swing & Lower Offset** - Provides better voltage headroom.
6. **Power Efficiency** - Reduces voltage drop and power consumption.
7. **Better Current Control** - MOSFETs allow precise tail current control, enhancing performance.
From the above analysis we can undrstand these points


## When we use active load 

### Circuit Diagram
![image](https://github.com/user-attachments/assets/40d2634d-ae2d-4199-8b83-b328bfa633a7)
### DC Analysis
![image](https://github.com/user-attachments/assets/d85b42a6-7b61-4407-92d4-4f926217c162)


Transistor Operating Points --
M1 Qpoint:(**1.25V, 0.5mA**)  
M2 Qpoint: (**1.25V, 0.5mA**)
 



-- Transistor Dimensions --
M1 & M2
Length  (L):  180 nm  ,
Width   (W): 1000 µm

M5 & M4
Length  (L):  182.145 nm ,
Width   (W): 1.05899 µm

M3
Length  (L):  110.99 nm ,
Width   (W): 9.499 µm

## Transient Analysis
![image](https://github.com/user-attachments/assets/322ff4c8-31d0-4660-8ea0-1ecf37430684)
Av= 19.8744v/v=25.96db (large signalgain with vinp=0.009v)

## Frequency responce
![image](https://github.com/user-attachments/assets/6ea4cda5-7b54-4d07-86f8-4eb13c0b9744)

Gain A-v= 31.98db (small signal gain with AC amplitude 1v)
Bandwidth 0Hz to 114.2719MHz


In a differential amplifier, PMOS transistors are preferred as active loads instead of resistors due to their superior performance and PMOS active loads enhance gain, reduce chip area, and improve voltage swing, making them ideal for differential amplifiers in IC design.



## Comparison

DC Analysis*
| Configuration                     | Increase in Vg                                | Decrease in Vg                                | Comparison                                       |
|----------------------------------|--------------------------------|--------------------------------|------------------------------------------------|
| With Source Resistors (RS)       | Increases drain current (Id). | Reduces drain current (Id).  | Unstable biasing due to temperature effects.  |
|                                  | Q-point shifts up but unstable | Q-point shifts down, reducing gain. | Requires careful resistor selection. |
|                                  | Requires higher supply voltage. | Can move MOSFET into cutoff region. | Gain is lower compared to other configurations. |
| With Current Source              | Increases drain current, but remains stable due to constant tail current. | Decreases drain current but maintains better stability. | More stable than RS configuration. |
|                                  | Q-point shifts up slightly.   | Less shift in Q-point compared to RS configuration. | Requires an additional current source for biasing. |
|                                  |                              |                              | Improved CMRR and gain.  |
| MOSFET as Current Source         | Provides controlled increase in Id. | Maintains a nearly constant tail current. | Highly stable biasing. |
|                                  | Q-point remains in saturation region. | Q-point shift is minimal. | Needs a well-designed current mirror. |
|                                  | More predictable behavior.   | Better temperature compensation. | Improved performance over passive resistor loads. |
| MOSFET as Current Source & Active Load | Best biasing stability. | Q-point remains nearly constant due to high output resistance. | The most stable configuration. |
|                                  | Very high gain, minimal Q-point variation. | Best overall performance. | Maximizes gain and voltage swing. |
|                                  | Maximizes voltage headroom. | Requires careful design to optimize performance. | |




































