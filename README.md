
# Characterisation of Basic CS amplifier in LTspice using 180 nm technology library

This project focuses on the characterisation of the common source amplifier using 180nm technology library (The 180nm technology library is a semiconductor fabrication process with a minimum feature size of 180 nanometers, commonly used in CMOS manufacturing for VLSI design and analog/mixed-signal circuits).
  To operate the mosfet as amplifier , the operating point should be at saturation region with meeting the conditions- VDS>VOV or VGD<Vt(for nmos). By simulating the circuit under different configurations, such as transient and AC analysis, we can observe its behavior under various conditions and how the circuit response as we replace drain resitor with a mosfet.

 # Circuit diagram

  ![Screenshot (45)](https://github.com/user-attachments/assets/b188d6d3-412c-4485-9f8f-ce5e27137738)

  # To fix the operating point in saturation region

Given pin as 100u watts ,thus pin=VDD*ID 
ID=100uwatts/1.8v=5.55*10^-5 A.

from the datasheet we got to know that vtn=0.36624 v.
 
 if we apply these values in the condition discussed above we will obtain the VD,
 VGD<vtn
 VG-VD<0.36624     (here,VG=0.9V)

 VD<0.9-0.36624
 VD<0.53376V

 then let's fix our VDS as 1v.

 Applying KVL in the loop , we will get

 RD=(VDD-VD)/ID

 RD=(1.8-1)/5.555^-5
 
 RD=14.414K ohm







  



  

  

  




