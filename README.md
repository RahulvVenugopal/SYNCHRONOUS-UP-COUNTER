### Name:Rahul V
### Register No:212223040163
### EX NO:5 SYNCHRONOUS UP COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

## Procedure

1.Open Quartus II and start the New Project Wizard.

2.Create a project and select your target FPGA device.

3.Create a Verilog HDL file and write the counter design.

4.Save the file and add it to the project.

5.Set it as the top-level entity.

6.lick Processing > Start Compilation to compile and check for errors.

7.Go to Tools > Netlist Viewers > RTL Viewer to view and save the RTL schematic.

8.Create a Vector Waveform File (.vwf): File > New > University Program VWF.

9.Use Node Finder to add clk, clr, en, and q[3..0] signals.

10.Apply input waveforms (clock, clear, enable) in the VWF editor.

11.Run simulation: Processing > Start Simulation.

12.View and save the timing diagram to verify counter functionality.

### PROGRAM
![Screenshot 2025-05-05 111411](https://github.com/user-attachments/assets/b841f318-edc6-4afe-af62-77893d7f20e6)


### RTL LOGIC UP COUNTER
![Screenshot 2025-05-05 111430](https://github.com/user-attachments/assets/c0f91626-6611-4179-a258-08d59f74d394)


### TIMING DIAGRAM FOR IP COUNTER
![Screenshot 2025-05-05 112618](https://github.com/user-attachments/assets/904c60a5-d1f0-4c61-add9-ed72af1c427d)

### TRUTH TABLE
![DE 11 b](https://github.com/user-attachments/assets/8ee63de0-3044-44f0-8563-a2f89e77afb4)
### RESULTS
Thus the 4-bit synchronous up counter is implemented succeessfully.
