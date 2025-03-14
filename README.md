
# Characterisation of Basic CS amplifier in LTspice using 180 nm technology library

This project focuses on the characterisation of the common source amplifier using 180nm technology library (The 180nm technology library is a semiconductor fabrication process with a minimum feature size of 180 nanometers, commonly used in CMOS manufacturing for VLSI design and analog/mixed-signal circuits).
  To operate the mosfet as amplifier , the operating point should be at saturation region with meeting the conditions- VDS>VOV or VGD<Vt(for nmos). By simulating the circuit under different configurations, such as transient and AC analysis, we can observe its behavior under various conditions and how the circuit response as we replace drain resitor with a mosfet.

 # Circuit diagram

![Screenshot (56)](https://github.com/user-attachments/assets/dc9ff2c8-b40b-4a14-9e69-009b69f01c98)


  # To fix the operating point in saturation region

Given pin as 100u watts ,thus pin=VDD*ID,

ID=100uwatts/1.8v=5.55*10^-5 A.

from the datasheet we got to know that vtn=0.36624 v.
 
 if we apply these values in the condition discussed above we will obtain the VD,
 VGD<vtn
 VG-VD<0.36624     (here,VG=0.9V)

 VD>0.9-0.36624
 VD>0.53376V

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
where the above one is gain plot and below oneis phase plot.


# Result


ID=5.555 * 10^-5 A
VDS=1v
Vin(DC offset)=0.9v
Gain(large signal analysis)=7.783dB


# Inference

1) As ID is directly proportional to w (ID=1/2*kn*vov^2)in saturation region and inversly proportional to l , we can decrease or increase the drain current by varying the aspect ratio.If wee decrease the channel length in a MOSFET , the short channel effect namely channel length modulation come into play and result in increment in ID .

2)As we are using a common source amplifier the output waveform is inverted due to phase shift betwenn input and the output.

# Circuit 2

# Circuit Diagram

# To set the DC operating point in Saturation region

for NMOS 

VDS1>VOV
VD1>0.9-0.36624
VD1>0.53376 V ,let VD1 be 0.7v

since VD1=VD2,

VD2=0.7v

for PMOS ,
VSD2>VSG2-|VTP|
1.8-0.7>1.8-Vb -0.399           (VG2=Vb)
Vb>0.301

let Vb=0.7v

from simulation we got this DC operating point and both the mosfets are in saturation region

![Screenshot (59)](https://github.com/user-attachments/assets/83c28ca6-1ad0-4e2b-a684-df081d440fc2)

# Transient Analysis
![Screenshot (60)](https://github.com/user-attachments/assets/06f4e7f7-74f3-47b9-8be7-ff2672344e10)

Gain=Vout p-p/Vin p-p
Gain= (1.4-0.3657)/0.1
Gain=10.343
Gain=20.293dB


# AC analysis
![Screenshot (61)](https://github.com/user-attachments/assets/9e170ed4-4fd0-4eca-bdc2-bdc4d2ae4981)

# Result
ID=5.55 *10^-5 A
VDS1=0.9v
Gain = 20.2929dB

# Inference
1)In comparison with the circuit 1 , circuit 2 has high gain due to no passive component(resitor ) to limit the gain 

2)Bandwidth of circuit 2 is lesser than the bandwidth of circuit 1

3)we can observe smooth output waveform in circuit 2 as an acive PMOS  load ,has better bandwidth meaning smooth and undistorted waveform.



















 












  



  

  

  




