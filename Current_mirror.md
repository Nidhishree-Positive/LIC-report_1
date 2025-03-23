
# Current mirrors – Design in LTspice using 180 nm technology lib

 The project aims to develop efficient mirror circuits, simulate their performance, and analyze the results in terms of gain, accuracy, and power consumption. The mirror circuits are essential in various applications such as analog signal processing, biasing, and reference generation for different analog circuits like amplifiers and voltage regulators.

 ### Design question
 Design and analyse current mirror circuit as active load in amplifier circuit

 ![image](https://github.com/user-attachments/assets/e2d73e61-9f25-4349-953c-d155459e57b7)

 
#### Design Requirements :

Gain: 𝐴𝑣>-10𝑉/𝑉 or >=20dB
​
Supply Voltage: 𝑉𝐷𝐷=1.8𝑉

Power Dissipation: 𝑃<1𝑚𝑊

Current Mirror Ratio: 1:1 , 1:2 ,1:3,1:4,2:1

#### Design Steps :

Step 1: Power Budget & Total Current

Given: 𝑃_total<1𝑚𝑊,  𝑉𝐷𝐷=1.8𝑉

I_Total = P/ VDD =1mW/1.8v ≈0.56mA

Since: 𝐼_total= 𝐼_ref+𝐼_x

I_ref =I_x = I_total/2≈0.28mA 



#### 1) Current Mirror Ratio: 1:1

![image](https://github.com/user-attachments/assets/c79aab91-e055-40a0-ad5a-1d7a1451f223)



The drain current with channel length modulation is expressed as:

ID = (1/2) * μn * Cox * (W/L) * (VGS - Vth)^2 * (1 + λ * VDS)

For a 1:1 current mirror, we have the relationship:

Iref = IX

Using the equation for both transistors:

(1/2) * μn * Cox * (W1/L1) * (VGS1 - Vth)^2 * (1 + λ * VDS1) = (1/2) * μn * Cox * (W2/L2) * (VGS2 - Vth)^2 * (1 + λ * VDS2)

For matched transistors in a 1:1 ratio:

W1/L1 = W2/L2

The equation simplifies to:

(VGS1 - Vth)^2 * (1 + λ * VDS1) = (VGS2 - Vth)^2 * (1 + λ * VDS2)

If VGS1 = VGS2, then:

(1 + λ * VDS1) = (1 + λ * VDS2)

This implies VDS1 = VDS2, ensuring the current mirror operation remains consistent.

The aspect ratio of MOSFET M3 and M2 is made equal, and 𝑉𝑥=𝑉𝑜𝑢𝑡. 

where for Mosfet M3&M2 w=100um and l=180nm
 for Mosfet M1 w=101.628um and l=180nm.

 #### a) DC analysis

 ![image](https://github.com/user-attachments/assets/b32945c8-d131-4ddd-b039-e9958d88d201)

 b)AC analysis
 
 ![image](https://github.com/user-attachments/assets/03e279a0-5c05-4015-8546-dcc5536321a4)
 
###### Gain is 29.229 dB



#### 2)Current Mirror Ratio: 1:2

![image](https://github.com/user-attachments/assets/d8b78a27-0af7-4581-9117-ad407c3378f0)

since the ration is 1:2 

let I_ref=0.185mA and I_x=2*I_ref =0.37mA 
since the I_total is remined same p_total remains same

Here ,The aspect ratio of MOSFET M2 is twice of M3, and 𝑉𝑥=𝑉𝑜𝑢𝑡. 

where for Mosfet M3  w=1000um and l=180nm
 Mosfet M2  w=2000um and l=180nm
 Mosfet M1 w=72.6968um and l=180nm.


#### a)DC analysis

![image](https://github.com/user-attachments/assets/ec7c5bbc-c5fe-4390-ace8-8edb2b88bc86)

b) AC analysis

![image](https://github.com/user-attachments/assets/5bef8a38-1091-4a86-ac47-26c68f25ec38)

##### gain is 29.469dB.

#### 2)Current Mirror Ratio: 1:3

![image](https://github.com/user-attachments/assets/368bb5cb-3322-46a2-836f-5331fcd0af71)


since the ration is 1:3

let I_ref=0.138mA and I_x=3*I_ref =0.4166mA 

since the I_total is remined same p_total remains same

Here ,The aspect ratio of MOSFET M2 is thrice of M3, and 𝑉𝑥=𝑉𝑜𝑢𝑡. 

where for Mosfet M3  w=10um and l=180nm
 Mosfet M2  w=30um and l=180nm
 Mosfet M1 w=158.712um and l=180nm.

 a)DC analysis
 
 ![image](https://github.com/user-attachments/assets/9582d59a-64b7-44ac-8f29-cdb5c7ef59fe)
 
b)AC Analysis

![image](https://github.com/user-attachments/assets/602c17c2-0e9e-49e5-903a-ee58b140802a)

 ##### Gain is 29.648 dB.


#### 2)Current Mirror Ratio: 1:4

![Screenshot 2025-03-23 192304](https://github.com/user-attachments/assets/db4ba3fd-d48a-4960-bf43-89ab1f47cb20)


since the ration is 1:4

let I_ref=0.111mA and I_x=4*I_ref =0.444mA 

since the I_total is remined same p_total remains same

Here ,The aspect ratio of MOSFET M1 is four times of M2, and 𝑉𝑥=𝑉𝑜𝑢𝑡. 

where for Mosfet M3  w=91.0128um and l=180nm
 Mosfet M2  w=400um and l=180nm
 Mosfet M1 w=100um and l=180nm.

 a)DC Analysis

 ![Screenshot 2025-03-23 192524](https://github.com/user-attachments/assets/403ae4ad-0a74-4ee8-85a4-346d175f6203)

b)AC analysis

![Screenshot 2025-03-23 192701](https://github.com/user-attachments/assets/f1f7fbe7-378f-4672-82aa-0b8fe7f01b42)

##### The gain is 30.258dB.


#### 2)Current Mirror Ratio: 2:1

![image](https://github.com/user-attachments/assets/2ae6c8f3-0468-4fb0-ab77-db5f40307081)


since the ration is 2:1

let I_ref=0.37037mA and I_x=0.1851mA 

since the I_total is remined same p_total remains same

Here ,The aspect ratio of MOSFET M1 is twice of M2, and 𝑉𝑥=𝑉𝑜𝑢𝑡. 

where for Mosfet M1  w=20um and l=180nm
 Mosfet M2  w=100um and l=180nm
 Mosfet M3 w=42.9285um and l=180nm.

 a)DC Analysis
 
 ![image](https://github.com/user-attachments/assets/ed324fb9-c770-41dd-927f-a278694eb6f5)

b)AC Analysis

![image](https://github.com/user-attachments/assets/f0d98ccf-994d-4840-877a-921fcd41d227)

##### The gain is 31.344dB.


#### Analysis when length of th emosfet differs retaining the aspect ratio

![image](https://github.com/user-attachments/assets/470a5c1c-0623-4777-a37a-facbd8701419)

![WhatsApp Image 2025-03-23 at 22 04 23_52b2d672](https://github.com/user-attachments/assets/55b98c43-40fe-4776-a62e-a012acaa9be0)


#### Analysis of copying / mirroring of current when current mirror ratio is varied 

![image](https://github.com/user-attachments/assets/fe8a0036-c6a9-4573-8597-96d24b35d810)


![WhatsApp Image 2025-03-23 at 22 04 22_429f3496](https://github.com/user-attachments/assets/eaa51c02-b837-45e6-8400-79d88d7feed3)


#### Differential amplifier using Current mirror

a) Circuit diagram

![image](https://github.com/user-attachments/assets/5e85aec2-eec6-4e95-9177-62c464eaea68)

b) DC Analysis

![image](https://github.com/user-attachments/assets/aec12805-b87c-4942-8591-d6e305598e3f)

![image](https://github.com/user-attachments/assets/1200ef08-f85a-4d2f-a246-aac23e2ad918)

Finding vin maximum


![Screenshot 2025-03-23 212556](https://github.com/user-attachments/assets/057586c0-8679-45af-9696-3952fda7350e)

##### maximum input swing is 0 to 1.516v

![image](https://github.com/user-attachments/assets/286d8da4-d9e9-4e86-858c-0564f3edd1f2)

##### maximum output swing is 0.886v to 2.17v 

c) Transient Analysis

![image](https://github.com/user-attachments/assets/dfa9b3d2-02fa-4df6-96dd-07c0494c70b8)

d) AC Analysis
![image](https://github.com/user-attachments/assets/b60e21ad-3f60-4aed-9f91-55dddf5c312d)
##### Gain is 29.48dB
