
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

 By simulating , we obtained the operating point of the mosfet as given below in the figure ,with aspect ratio of 13/7.
 ![Screenshot (46)](https://github.com/user-attachments/assets/93988854-fb81-4521-b8f6-5ac9b161bb27)

 
# Transient anaysis

By providing a sine wave with DC offset of 0.9v, amplitude 50mv and with frequency 1kHZ in the input we obtained the responc of the circuit with respect to time .

![image](https://github.com/user-attachments/assets/bcd25a03-5797-412c-87b0-0796417c1afb)

The gain of the circuit with the inputas a sine wave of frequency 1kHZ is given by Gain=voutp-p/vinp-p
Gain=91.120-0.8750/0.1
Gain=2.44999
Gain=7.7832dB



# AC analysis

Through AC analysis we can obtain the frequency responce of the circuit with various range of frequency , here we are providing a frequency range of 0.1-1T HZ.

![Screenshot (54)](https://github.com/user-attachments/assets/094d99fa-97d1-43f6-8e83-7294508dcf1e)






 












  



  

  

  




