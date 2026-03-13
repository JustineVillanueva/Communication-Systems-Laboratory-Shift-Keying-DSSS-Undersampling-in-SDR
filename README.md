# Communication Systems Laboratory: Shift Keying, DSSS, and Undersampling in software defined radio (Experiments 15-20)
### Objective
To study and analyze various digital modulation and demodulation techniques—including ASK, FSK, BPSK, QPSK, and DSSS—and to investigate the effects of undersampling using software-defined radio (SDR) platforms.

---
### Materials / Components Used
- Emona Telecoms-Trainer 101 (ETT-101)
- Dual Channel 20MHz Oscilloscope
- ETT-101 Oscilloscope Leads
- ETT-101 Patch Leads

---
## Laboratory Experiment 15: Amplitude Shift Keying
This laboratory experiment introduces amplitude shift keying (ASK), a digital modulation technique where the amplitude of a carrier signal is varied according to the digital data.

### ASK Characteristics
- ASK represents digital data using different carrier amplitudes.
- A logic 1 is transmitted using a carrier signal.
- A logic 0 is transmitted by reducing or removing the carrier.
- ASK is one of the simplest digital modulation techniques, but it is sensitive to noise because amplitude variations can easily be affected by interference.
  
### Circuit Diagram
<details>
  <summary>Experiment 15 Diagram</summary>


**Part A: Generating an ASK Signal**

**Figure 15.3**
![Experiment 15 Setup](Diagrams/Exp15-Diagrams/Exp15_Fig15.3.jpg)


**Figure 15.5**
![Experiment 15 Setup](Diagrams/Exp15-Diagrams/Exp15_Fig15.5.jpg)


**Part B: Demodulating an ASK signal using an envelope detector**

**Figure 15.7**
![Experiment 15 Setup](Diagrams/Exp15-Diagrams/Exp15_Fig15.7.jpg)


**Part C: Restoring the recovered digital signal using a comparator**

**Figure 15.9**
![Experiment 15 Setup](Diagrams/Exp15-Diagrams/Exp15_Fig15.9.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 15 Result</summary>


**Part A Result**

![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_A.png)


Step 7: Connect the set-up in Figure 2
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_A7.png)

Step 13: Compare the signals
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_A13.png)


**Part B Result**

Step 17: Modify the set-up as shown in Figure 6/7
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_B17.png)


**Part C**

Step 20: Set the Variable DC control to the middle
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_C20.png)

</details>

### Observation
The experiment demonstrated how digital data can control the amplitude of a carrier signal. When the input data was high, the carrier appeared with full amplitude, representing a logic 1. When the input was low, the carrier amplitude decreased or disappeared, representing a logic 0. This shows how ASK can transmit binary information through amplitude variations.

---
## Laboratory Experiment 16: Frequency Shift Keying
This laboratory experiment demonstrates frequency shift keying (FSK), where digital data is represented by changing the frequency of a carrier signal.

### FSK Characteristics
- FSK uses two different frequencies to represent binary data.
- Logic 1 is represented by a higher frequency (mark) and Logic 0 is represented by a lower frequency (space).
- The amplitude of the carrier remains constant.
- FSK provides better noise immunity than ASK.
  
### Circuit Diagram
<details>
  <summary>Experiment 16 Diagram</summary>


**Part A: Generating an FSK Signal**

**Figure 16.3: FSK Signal**
![Experiment 16 Setup](Diagrams/Exp16-Diagrams/Exp16_Fig16.3.jpg)


**Part B: Demodulating an FSK signal using filtering and an envelope detector**

**Figure 16.5: FSK Generation-Demodulation**
![Experiment 16 Setup](Diagrams/Exp16-Diagrams/Exp16_Fig16.5.jpg)


**Part C: Restoring the recovered data using a comparator**

**Figure 16.9: FSK Generation-Demodulation-Restoration**
![Experiment 16 Setup](Diagrams/Exp16-Diagrams/Exp16_Fig16.9.jpg)


</details>

### Oscilloscope Display
<details>
  <summary>Experiment 16 Result</summary>


**Part A Result**

Step 12: Set to dual position to view the Sequence Generator module's output and the FSK Signal
![Experiment 16 FSK](Simulation/Exp16-Waveforms/Exp16_A12.png)


**Part B Result**

Step 18: Turn the Tuneable LPF's cut-off frequency control fully clockwise.
![Experiment 16 FSK](Simulation/Exp16-Waveforms/Exp16_B18.png)

Step 21: Connect the channel 2 to the envelope detector's output
![Experiment 16 FSK](Simulation/Exp16-Waveforms/Exp16_B21.png)


**Part C Result**

Part C Output
![Experiment 16 FSK](Simulation/Exp16-Waveforms/Exp16_C_output.png)


</details>

### Observation
The experiment showed that the carrier frequency changes depending on the digital input signal. When the input was logic 1, the carrier frequency increased, while a logic 0 produced a lower frequency. This demonstrated how digital data can be transmitted by switching between two different carrier frequencies.

---
## Laboratory Experiment 17: Binary Phase Shift Keying
This laboratory experiment focuses on binary phase shift keying (BPSK), where the phase of the carrier signal changes to represent digital data.

### BPSK Characteristics
- FSK uses two different carrier phases to represent binary data.
- Logic 1 is represented by a carrier with 0° phase and Logic 0 is represented by a carrier with 180° phase shift.
- The amplitude and frequency of the carrier remain constant.
- BPSK is widely used in digital communication systems due to its reliability.
  
### Circuit Diagram
<details>
  <summary>Experiment 17 Diagram</summary>


**Part A: Generating a BPSK Signal**

**Figure 17.3: BPSK Generation**
![Experiment 17 Setup](Diagrams/Exp17-Diagrams/Exp17_Fig17.3.jpg)


**Part B: Demodulating a BPSK Signal using a product detector**

**Figure 17.5: BPSK Generation-Product Detection**
![Experiment 17 Setup](Diagrams/Exp17-Diagrams/Exp17_Fig17.5.jpg)


**Part C: Restoring the recovered data using a comparator**

**Figure 17.7: BPSK Generation-Product Detection-Restoration**
![Experiment 17 Setup](Diagrams/Exp17-Diagrams/Exp17_Fig17.7.jpg)


</details>

### Oscilloscope Display
<details>
  <summary>Experiment 17 Result</summary>

**Part A Result**

![Experiment 17 BPSK](Simulation/Exp17-Waveforms/Exp17_A.png)


**Part B Result**

![Experiment 17 BPSK](Simulation/Exp17-Waveforms/Exp17_B.png)


**Part C Result**

![Experiment 17 BPSK](Simulation/Exp17-Waveforms/Exp17_C.png)


**Extra Part: Noise**

Noise is at 0dB
![Experiment 17 BPSK](Simulation/Exp17-Waveforms/Exp17_Noise_0dB.png)

Noise is at -6dB
![Experiment 17 BPSK](Simulation/Exp17-Waveforms/Exp17_Noise_-6dB.png)

Noise is at -20dB
![Experiment 17 BPSK](Simulation/Exp17-Waveforms/Exp17_Noise_-20dB.png)


</details>

### Observation
The experiment demonstrated the generation and recovery of a BPSK signal. The carrier phase shifted by 180° according to the input data to produce the BPSK signal. A product detector was then used to demodulate the signal and recover the baseband data. Finally, a comparator restored the recovered signal into a clear digital waveform representing the original binary data.

---
## Laboratory Experiment 18: Quadrature Phase Shift Keying
This laboratory experiment introduces quadrature phase shift keying (QPSK), an advanced modulation technique that allows the transmission of two bits per symbol.

### QPSK Characteristics
- FSK uses four different phase states to represent binary data.
- Each phase state represents two bits of data.
- Possible phases typically include 0°, 90°, 180°, and 270°.
- QPSK improves spectral efficiency compared to BPSK.
- It is commonly used in modern digital communication systems.
  
### Circuit Diagram
<details>
  <summary>Experiment 18 Diagram</summary>

**Part A: Generating a QPSK signal**

**Figure 18.4: The data bits is split into a stream of even and odd bits**
![Experiment 18 Setup](Diagrams/Exp18-Diagrams/Exp18_Fig18.4.jpg)

**Figure 18.6: Even bits to Channel 1 and PSK_I to Channel 2**
![Experiment 18 Setup](Diagrams/Exp18-Diagrams/Exp18_Fig18.6.jpg)

**Figure 18.8: Odd bits to Channel 1 and PSK_Q to Channel 2**
![Experiment 18 Setup](Diagrams/Exp18-Diagrams/Exp18_Fig18.8.jpg)

**Figure 18.10: QPSK Modulator**
![Experiment 18 Setup](Diagrams/Exp18-Diagrams/Exp18_Fig18.10.jpg)



**Part B: Using phase discrimination to pick-out one of the QPSK signal's BPSK signals**

**Figure 18.12: Implements most of one arm of a QPSK demodulator**
![Experiment 18 Setup](Diagrams/Exp18-Diagrams/Exp18_Fig18.12.jpg)

**Figure 18.14: The added comparator completes one arm of a QPSK demodulator**
![Experiment 18 Setup](Diagrams/Exp18-Diagrams/Exp18_Fig18.14.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 18 Result</summary>

**Part A Result**

Step 10: Comparison of the two digital signals
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_A1-10.png)

Comparison of the even bits with the multiplier output
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_A11-17.png)

Comparison of the odd bits with the multiplier output
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_A18-21.png)

Step 24: The adder module's G control is turned fully anti-clockwise
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_A22-24.png)

Step 25: The adder module's g control is adjusted to obtain a 4Vpp output
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_A25.png)



**Part B Result**

Phase Shifter in 0 degree position: Clockwise
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_B_CW-0-deg.png)

Phase Shifter in 0 degree position: Counter Clockwise
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_B_CCW-0-deg.png)

Phase Shifter in 180 degree position: Clockwise
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_B_CW-180-deg.png)

Phase Shifter in 180 degree position: Counter Clockwise
![Experiment 18 QPSK](Simulation/Exp18-Waveforms/Exp18_B_CCW-180-deg.png)

</details>

### Observation
The experiment demonstrated how a QPSK signal can be generated by combining two binary data streams that modulate the phase of a carrier signal, resulting in four distinct phase states representing different symbol combinations. This shows how QPSK transmits two bits per symbol, improving bandwidth efficiency compared to BPSK. Using phase discrimination, one of the BPSK components of the QPSK signal was successfully isolated and detected, allowing the corresponding data stream to be recovered. The results illustrate that a QPSK signal can be interpreted as two orthogonal BPSK signals whose individual data can be extracted through proper phase detection.

---
## Laboratory Experiment 19: DSSS Modulation and Demodulation
This laboratory experiment demonstrates direct sequence spread spectrum (DSSS), a technique used to spread a signal over a wider bandwidth to improve security and resistance to interference.

### DSSS Characteristics
- DSSS multiplies the data signal with a high-rate pseudo-random spreading code.
- This spreads the signal over a much wider bandwidth.
- The receiver uses the same spreading code to recover the original signal.
- DSSS improves resistance to noise and interference.
- It is used in wireless communication systems such as Wi-Fi.
  
### Circuit Diagram
<details>
  <summary>Experiment 19 Diagram</summary>

**Part A: Generating a DSSS signal using a simple message**

**Figure 19.2: DSSS Signal**
![Experiment 19 Setup](Diagrams/Exp19-Diagrams/Exp19_Fig19.2.jpg)



**Part C: Using the product detector to recover the message**

**Figure 19.5: Product Detector**
![Experiment 19 Setup](Diagrams/Exp19-Diagrams/Exp19_Fig19.5.jpg)

**Figure 19.6: DSSS Modulator - Product Detector**
![Experiment 19 Setup](Diagrams/Exp19-Diagrams/Exp19_Fig19.6.jpg)



**Part D: DSSS and deliberate interference (jamming)**

**Figure 19.9: DSSS Modulator - Channel - Product Detector**
![Experiment 19 Setup](Diagrams/Exp19-Diagrams/Exp19_Fig19.9.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 19 Result</summary>

**Part A Result**

A generated DSSS signal
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_A.png)



**Part C Result**

Added a product detector to the DSSS Modulator
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_C.png)

Step 19: Tuneable Low-pass filter cut-off frequency control is turned clockwise
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_C19.png)

Step 21: Modified the set-up to make the demodulator's local carrier a different PN sequence to the transmitter's carrier
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_C21.png)



**Part D Result**

Step 28: The VCO module is used to generate a variable frequency jamming signal
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D28.png)

Step 29: DSSS signal on Channel 1 and recovered message on Channel 2
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D29.png)

Step 30: The jamming signal is added by turning the g control clockwise and stopping in the middle of its travel
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D30-1.png)
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D30-2.png)

Step 31: The jamming signal's frequency is varied by turning the VCO frequency adjust control left and right

Minimum:
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D31-1-minfreq.png)

Maximum:
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D31-2-maxfreq.png)

Step 34: The jamming signal is increased to maximum by turning the g control fully clockwise
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D34.png)

Step 38: Modified the set-up to force the VCO module's output to sweep continuously
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D38.png)

Step 40: Modified the set-up to use the noise generator to model a jamming signal
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D40.png)

Step 42: Jamming signal is at -6dB
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D42.png)

Step 44: Jamming signal is at 0dB
![Experiment 19 DSSS](Simulation/Exp19-Waveforms/Exp19_D44.png)

</details>

### Observation
The experiment demonstrated how a DSSS signal spreads a message signal using a PN sequence, producing a wideband transmission. A product detector and low-pass filter were able to recover the original message when the correct PN sequence was used, while using a different sequence prevented proper recovery. I also learned that when jamming signals and noise were introduced and their strength and frequency were varied, the system was still able to recover the message to some extent, showing the interference resistance of DSSS systems.

---
## Laboratory Experiment 20: Undersampling in Software Defined Radio
This laboratory experiment explores the concept of undersampling in software defined radio (SDR), where signals are sampled at a rate lower than the Nyquist rate but still reconstructed correctly under specific conditions.

### Undersampling Concept
- Undersampling occurs when the sampling rate is lower than twice the signal frequency.
- SDR systems often use undersampling to process high-frequency signals with lower sampling rates.
- Aliasing is intentionally used to shift signals into a lower frequency band for processing.
  
### Circuit Diagram
<details>
  <summary>Experiment 20 Diagram</summary>

**Part A: Setting up a bandwidth limited signal**

**Figure 20.2: DSBSC Modulator**
![Experiment 20 Setup](Diagrams/Exp20-Diagrams/Exp20_Fig20.2.jpg)



**Part B: Direct down-conversion using undersampling**

**Figure 20.4: DSBSC Modulator - Demodulation**
![Experiment 20 Setup](Diagrams/Exp20-Diagrams/Exp20_Fig20.4.jpg)


</details>

### Oscilloscope Display
<details>
  <summary>Experiment 20 Result</summary>

**Part A Result**

Step 6: DSBSC Signal envelope forming the same shape as the message
![Experiment 20](Simulation/Exp20-Waveforms/Exp20_A6.png)



**Part B Result**

Step 8: The channel 2 shows the under-sampled DSBSC signal when connected to the S/H output 
![Experiment 20](Simulation/Exp20-Waveforms/Exp20_B8.png)

Step 10: The channel 2 shows the recovered message when connected to the baseband LPF output
![Experiment 20](Simulation/Exp20-Waveforms/Exp20_B10.png)



**Part C Result**

Step 19: Changed the master signal's 8KHz digital output to a VCO digital output.
![Experiment 20](Simulation/Exp20-Waveforms/Exp20_C19.png)

Step 21: VCO frequency control is varied to try and correct the frequency error
![Experiment 20](Simulation/Exp20-Waveforms/Exp20_C21.png)


</details>

### Observation
In this experiment, the DSBSC signal produced an envelope that followed the shape of the original message signal. When the signal was connected to the sample-and-hold output, an undersampled version of the DSBSC waveform was observed, and when the signal passed through the baseband low-pass filter, the original message was recovered. The digital source was then changed to a VCO digital output, and adjustments to the VCO frequency were required to correct frequency errors, highlighting the importance of proper frequency alignment for accurate signal recovery during undersampling.

---
## Learnings Summary
These experiments demonstrated how digital data can be transmitted and recovered using different modulation techniques. ASK and FSK showed how amplitude and frequency variations encode binary data, while BPSK and QPSK illustrated phase modulation, with QPSK combining two data streams to improve bandwidth efficiency.

DSSS modulation introduced the concept of spreading a message signal with a PN sequence to produce a wideband signal. The experiments showed that the original message could be recovered using a product detector and low-pass filter when the correct PN sequence was used, and the system maintained some resilience even under jamming, highlighting DSSS’s interference resistance.

Finally, the undersampling lab demonstrated how a DSBSC signal can be sampled below the Nyquist rate, producing a step-like waveform that, when filtered through a baseband low-pass filter, recovers the original message. Attempts to use a VCO digital source emphasized the critical need for precise frequency alignment to ensure accurate signal recovery during undersampling.

Collectively, these labs reinforced the principles of digital modulation, phase and frequency manipulation, and advanced signal processing techniques such as QPSK, DSSS, and undersampling in software-defined radio, providing insight into efficient and reliable data transmission in modern communication systems.
