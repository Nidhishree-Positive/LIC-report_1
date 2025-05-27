# Design and Simulation of 555 Timer-Based Astable and Monostable Multivibrators for Pulse Generation and Width Control Applications

## Introduction
The 555 timer integrated circuit (IC) is one of the most popular and versatile components used in analog electronics. It was introduced by Signetics in 1972 and has since found widespread applications in timers, oscillators, pulse generation, and waveform shaping circuits. The 555 timer can operate primarily in three modes: astable, monostable, and bistable. In this project, we focus on the astable and monostable modes to generate precise pulse waveforms and control pulse widths for applications such as pulse width modulation (PWM), timing delays, and triggering circuits.

The objective of this project is to design and simulate two experimental setups using the 555 timer IC in LTspice simulation software. 
* The first setup is an astable multivibrator generating a PWM waveform with a fixed pulse width of approximately 0.5 milliseconds.
* The second setup is a monostable multivibrator triggered by the output of the astable circuit after passing through a differentiator and clipper stage.
   The monostable circuit produces a single output pulse whose width can be varied externally by changing component values.

By simulating these circuits, we aim to understand the working principles of the 555 timer in generating and controlling pulse signals and to explore the practical aspects of triggering monostable pulses from an astable source.

here is the pin diagram of **IC 555**

![image](https://github.com/user-attachments/assets/90601a02-fba2-424b-b39a-154398aa21e0)

### block diagram of IC 555

![image](https://github.com/user-attachments/assets/79ba7aa2-2163-4e6b-b4ec-69a2d2c33e2a)

**Internal Circuit of 555 Timer IC**
The 555 timer IC consists of:

Voltage Divider: Three equal resistors form a voltage divider providing reference voltages at 1/3 and 2/3 of Vcc.

Two Comparators:

Trigger Comparator: Checks if trigger voltage (Pin 2) is below 1/3 Vcc to set the flip-flop.

Threshold Comparator: Checks if threshold voltage (Pin 6) is above 2/3 Vcc to reset the flip-flop.

SR Flip-Flop: Controls output state based on comparator inputs.

Discharge Transistor: Connected to Pin 7; turns ON to discharge timing capacitor when output is LOW and OFF when output is HIGH.

Output Stage: Push-pull transistor provides the output signal on Pin 3.

Control Voltage (Pin 5): Allows external adjustment of the 2/3 Vcc threshold voltage for timing control.

Operation.
Operation:

* When Pin 2 voltage < 1/3 Vcc → Output goes HIGH, discharge transistor OFF (capacitor charges).

* When Pin 6 voltage > 2/3 Vcc → Output goes LOW, discharge transistor ON (capacitor discharges).

This internal setup enables the 555 timer to work as a stable oscillator or timer.



## Objective 

1. To design and simulate a 555 timer in astable mode generating a PWM waveform with a pulse width of approximately 0.5 ms.

2. To build a differentiator and clipper circuit that converts the astable output into a suitable trigger pulse for a monostable 555 timer.

3. To design a monostable 555 timer circuit triggered by the clipped pulse, with externally adjustable pulse width.

4.  To analyze the waveforms generated in each stage through LTspice transient simulations.


## Methodology and Circuit overview 

The overall system comprises three main blocks:

**Astable 555 Timer Circuit** – generates a continuous square wave (PWM).

**Differentiator and Clipper Circuit** – converts the astable square wave into short trigger pulses suitable for monostable operation.

**Monostable 555 Timer Circuit** – produces a single output pulse when triggered, with adjustable duration.




