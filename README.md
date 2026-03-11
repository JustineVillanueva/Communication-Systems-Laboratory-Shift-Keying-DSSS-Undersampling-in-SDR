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
![Experiment 15 Setup](Diagrams/Exp15-Diagrams/Exp15_Fig15.3.jpg)


**Part C: Restoring the recovered digital signal using a comparator**

**Figure 15.9**
![Experiment 15 Setup](Diagrams/Exp15-Diagrams/Exp15_Fig15.5.jpg)

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 15 Result</summary>


**Part A Result**

![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_A.jpg)


Step 7: Connect the set-up in Figure 2
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_A7.jpg)

Step 13: Compare the signals
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_A13.jpg)


**Part B Result**

Step 17: Modify the set-up as shown in Figure 6/7
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_B17.jpg)


**Part C**

Step 20: Set the Variable DC control to the middle
![Experiment 15 ASK](Simulation/Exp15-Waveforms/Exp15_C20.jpg)

</details>

### Observation
The experiment demonstrated how digital data can control the amplitude of a carrier signal. When the input data was high, the carrier appeared with full amplitude, representing a logic 1. When the input was low, the carrier amplitude decreased or disappeared, representing a logic 0. This shows how ASK can transmit binary information through amplitude variations.

---
## Laboratory Experiment 16: Frequency Shift Keying
This laboratory experiment demonstrates frequency shift keying (FSK), where digital data is represented by changing the frequency of a carrier signal.

### FSK Characteristics
- FSK uses two different frequencies to represent binary data.
- Logic 1 is represented by a higher frequency and Logic 0 is represented by a lower frequency.
- The amplitude of the carrier remains constant.
- FSK provides better noise immunity than ASK.
  
### Circuit Diagram
<details>
  <summary>Experiment 16 Diagram</summary>

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 16 Result</summary>

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

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 17 Result</summary>

</details>

### Observation
The experiment demonstrated how digital data can be transmitted by shifting the phase of the carrier signal. A phase reversal of 180° was observed when the input data changed between logic states. This phase change represents the binary information while maintaining constant amplitude and frequency.

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

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 18 Result</summary>

</details>

### Observation
The experiment showed how QPSK transmits two bits simultaneously by shifting the phase of the carrier among four possible phase states. This allows more efficient use of bandwidth compared to BPSK, since each symbol carries twice the amount of information.

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

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 19 Result</summary>

</details>

### Observation
The DSSS system spread the original data signal across a wider frequency range using a pseudo-random spreading sequence. At the receiver, the same spreading code was used to despread the signal and recover the original data. This demonstrated how DSSS improves signal robustness and reduces susceptibility to interference.

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

</details>

### Oscilloscope Display
<details>
  <summary>Experiment 20 Result</summary>

</details>

### Observation
The experiment demonstrated how a bandpass signal can be sampled at a rate lower than the Nyquist rate while still preserving the information. The undersampling process caused the signal to appear at a different frequency due to aliasing, illustrating how software defined radio systems can efficiently process high-frequency signals using lower sampling rates.

---
## Learnings Summary
Through these experiments, I learned how digital information can be transmitted using different modulation techniques such as ASK, FSK, BPSK, and QPSK. These methods demonstrate how carrier signals can be modified in amplitude, frequency, or phase to represent digital data. The DSSS experiment further showed how spreading techniques improve signal security and resistance to interference. Finally, the undersampling experiment introduced concepts used in software defined radio, where signals can be efficiently processed using controlled aliasing and lower sampling rates.
