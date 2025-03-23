
# Current mirrors – Design in LTspice using 180 nm technology lib

 The project aims to develop efficient mirror circuits, simulate their performance, and analyze the results in terms of gain, accuracy, and power consumption. The mirror circuits are essential in various applications such as analog signal processing, biasing, and reference generation for different analog circuits like amplifiers and voltage regulators.

 ### Design question
 Design and analyse current mirror circuit as active load in amplifier circuit

 
#### Design Requirements :

Gain: 𝐴𝑣>-10𝑉/𝑉
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





​


