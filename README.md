<p align="center">
  <strong>Modular Analysis of Analog FM and Digital PCM Telecommunications Engineering</strong>
</p>

---

## PART 1: ANALOG FREQUENCY MODULATION AND DEMODULATION

This laboratory session introduces the fundamental principles of Analog Frequency Modulation (FM) and Demodulation, which are the cornerstones of high-fidelity radio broadcasting and various communication systems. Unlike Amplitude Modulation (AM), where the carrier's power changes, FM maintains a constant amplitude while varying the frequency to carry information.

### **Signal Synthesis (Modulation)**

In the field of Telecommunications Engineering, Signal Synthesis—specifically Modulation—is the fundamental process of preparing an information signal for transmission. In Analog Frequency Modulation (FM), synthesis involves embedding a low-frequency message signal (such as voice or music) into a high-frequency carrier wave by varying the carrier’s instantaneous frequency.

<details>
  <summary><strong>Wiring Diagram (click to expand)</strong></summary>

  ![Pic 1](LAB%20PICS/1.jpg)
  
  ![Pic 2](LAB%20PICS/2.jpg)
  
  ![Pic 3](LAB%20PICS/3.jpg)

</details>

<details>
  <summary><strong>Results (click to expand)</strong></summary>

  ![Result 11](LAB%20PICS/11.jpg)
  
  ![Result 22](LAB%20PICS/22.jpg)
  
  ![Result 33](LAB%20PICS/33.jpg)
  
  ![Result 44](LAB%20PICS/44.jpg)
  
  ![Result 55](LAB%20PICS/55.jpg)
  
  ![Result 66](LAB%20PICS/66.jpg)

</details>

### **Signal Recovery (Demodulation)**

In the world of electronics, we take information (like your voice or a text message) and hitch it onto a high-frequency carrier wave to send it across the airwaves. This is modulation. Signal recovery is the process at the receiver's end that strips away that carrier wave to get back the original, meaningful data.

<details>
  <summary><strong>Wiring Diagram (click to expand)</strong></summary>

  ![Pic 7](LAB%20PICS/7.jpg)
  
  ![Pic 8](LAB%20PICS/8.jpg)
  
  ![Pic 9](LAB%20PICS/9.jpg)
  
  ![Pic 10](LAB%20PICS/10.jpg)
  
  ![Pic 11-](LAB%20PICS/11-.jpg)
  
  ![Pic 12](LAB%20PICS/12.jpg)

</details>

<details>
  <summary><strong>Results (click to expand)</strong></summary>

  ![R1](LAB%20PICS/R1.png)
  
  ![R2](LAB%20PICS/R2.png)
  
  ![R3](LAB%20PICS/R3.png)
  
  ![R4](LAB%20PICS/R4.png)

</details>

---

## PART 2: SAMPLING AND RECONSTRUCTION

Welcome to the bridge between the analog world we live in and the digital world where we process data. Sampling and Reconstruction are the two halves of a single mission: turning a continuous wave into a list of numbers and then back into a wave again.

### **SAMPLING PROCESS**

The continuous message signal is converted into a series of pulses using a Dual Analog Switch (acting as a sampling gate):
Sampling Clock: A high-frequency pulse train (Sampling Signal) is used to open and close the switch at regular intervals.

Sampled Output: The output consists of "slices" of the original message. We observe how the pulse amplitude follows the original waveform’s shape, creating a Pulse Amplitude Modulated (PAM) signal.
<details>
  <summary><strong>Wiring Diagram (click to expand)</strong></summary>

  <!-- sampling results placeholder -->

  ![Pic 13](LAB%20PICS/13.jpg)
  ![Pic 14](LAB%20PICS/14.jpg)
  ![Pic 15](LAB%20PICS/15.jpg)
</details>
<details>
  <summary><strong>Results (click to expand)</strong></summary>


  ![Pic 16](LAB%20PICS/16.jpg)
  ![Pic 17](LAB%20PICS/17.jpg)
  ![Pic 18](LAB%20PICS/18.jpg)
  ![Pic 19](LAB%20PICS/19.jpg)
</details>


### **Signal Reconstruction**
To return the discrete samples back to their original analog form:

Filtering: The sampled signal is passed through a Tuneable Low-Pass Filter.

Recovery: The filter removes the high-frequency "switching" components, leaving behind the smooth, original baseband message.
<details>
  <summary><strong>Wiring Diagram (click to expand)</strong></summary>


  ![Pic 20](LAB%20PICS/20.jpg)
  ![Pic 21](LAB%20PICS/21.jpg)
  ![Pic 22-](LAB%20PICS/22-.jpg)
  ![Pic 23](LAB%20PICS/23.jpg)
</details>
<details>
  <summary><strong>Results (click to expand)</strong></summary>


  ![Pic 24](LAB%20PICS/24.jpg)
  ![Pic 25](LAB%20PICS/25.jpg)
  ![Pic 26](LAB%20PICS/26.jpg)
</details>

---

## PART 3: PCM ENCODING AND DECODING

---

This section explores Pulse Code Modulation (PCM), the industry standard for turning analog waves into a digital language. While sampling "slices" the signal in time, PCM goes a step further by converting those slices into a precise numerical code through Quantization and Encoding. This transformation is what allows your voice or music to be stored, compressed, and transmitted across the globe with zero loss in quality—the backbone of everything from high-def audio to 5G telephony.

### **Encoding**

Sampling (The "Time" Slice)The encoder first captures the instantaneous value of the analog input. This is controlled by the System Clock. To ensure no information is lost, the clock must run at a frequency at least twice that of the input signal (The Nyquist Rate).

 Quantization (The "Value" Grid)Since a computer cannot understand "1.2345... volts," we map the sample to the nearest "rung" on a digital ladder. In this 4-bit system, the vertical range of the signal is divided into $2^4 = 16$ distinct levels.The Trade-off: With 16 levels, the "rounding" is relatively coarse. This leads to Quantization Noise, which is the audible difference between the smooth original wave and the "staircase" approximation.
 
  Encoding (The "Digital" Translation)Once a sample is assigned to one of the 16 levels, the encoder translates that level into a specific binary code (e.g., Level 5 becomes 0101). These bits are then sent out as a high-speed serial bitstream—a string of 1s and 0s that represents the original sound or data.
  <details>
  <summary><strong>Wiring Diagram (click to expand)</strong></summary>


  ![Pic 27](LAB%20PICS/27.jpg)
  ![Pic 28](LAB%20PICS/28.jpg)
  ![Pic 29](LAB%20PICS/29.jpg)
  ![Pic 30](LAB%20PICS/30.jpg)

  ![Pic 31](LAB%20PICS/31.jpg)
  ![Pic 32](LAB%20PICS/32.jpg)
  ![Pic 33-](LAB%20PICS/33-.jpg)
  ![Pic 34](LAB%20PICS/34.jpg)
</details>
<details>
  <summary><strong>Results (click to expand)</strong></summary>


  ![Pic 36](LAB%20PICS/36.png)
  ![Pic 37](LAB%20PICS/37.png)
  ![Pic 38](LAB%20PICS/38.png)
  ![Pic 39](LAB%20PICS/39.png)
  ![Pic 40](LAB%20PICS/40.png)
  ![Pic 41](LAB%20PICS/41.png)
</details>

### **DECODING**

Digital Reception & Frame SyncBefore the decoder can translate the bits, it must know where one sample ends and the next begins. Since the data arrives as a continuous string of 1s and 0s, the Frame Synchronization signal acts as a digital "comma."It groups the incoming stream into 4-bit words.Without this timing, the decoder might read the end of one sample and the start of the next as a single, garbled value.

D/A Conversion (The "Staircase" Phase)The Digital-to-Analog (D/A) Converter translates each 4-bit binary word back into a specific voltage level.For example, a 0111 might be converted to $0\text{V}$, while 1111 becomes $+5\text{V}$.At this stage, the signal looks like a "staircase" approximation (technically a Zero-Order Hold). While the general shape of the original wave is visible, it is jagged and filled with high-frequency "edges."Note: This staircase is essentially a raw Pulse Amplitude Modulated (PAM) signal waiting to be polished.

 Smoothing (Final Reconstruction)The final step uses a Low-Pass Filter (LPF) to act as a "sonic sander."The sharp corners of the staircase represent high-frequency noise that wasn't in the original message.The LPF blocks these rapid jumps and "connects the dots," smoothing the transitions to restore the original, continuous analog waveform.
 <details>
 <summary><strong>Wiring Diagram (click to expand)</strong></summary>


  ![Pic 42](LAB%20PICS/42.jpg)
  ![Pic 43](LAB%20PICS/43.jpg)
  ![Pic 44-](LAB%20PICS/44-.jpg)
  ![Pic 45](LAB%20PICS/45.jpg)
</details>
<details>
<summary><strong>Results (click to expand)</strong></summary>
  ![Pic 46](LAB%20PICS/46.png)
  ![Pic 47](LAB%20PICS/47.png)
  
</details>

## PART 4: BANDWIDTH LIMITING AND RESTORING DIGITAL SIGNAL

In a perfect world, a digital signal is a sharp, crisp square wave. In the real world, physics gets in the way. Bandwidth Limiting is the natural (or intentional) "rounding off" of these sharp edges as a signal travels through a medium, while Restoring is the process of cleaning up that messy data so a computer can read it again.
### **Simulating the Channel (Bandwidth Limiting)**

Loss of High-Frequency Components (Rounding)A perfect digital pulse is a square wave, which mathematically consists of a fundamental frequency plus an infinite series of odd harmonics. These harmonics are what create the "sharp" vertical edges.

The Filter's        Action: As you lowered the cut-off frequency , you stripped away these higher harmonics.

The Result: Without the high frequencies, the edges can no longer be vertical. The pulses begin to look like rounded "humps" or "sines" rather than blocks.

Pulse Spreading and ISI Intersymbol Interference (ISI) is the "nightmare" of digital communications. As the bandwidth narrows further, the time it takes for a pulse to rise and fall increases.

The "Smear": The energy of a single bit starts to leak into the time slot reserved for the next bit.The Receiver's Dilemma: If a '1' is still "falling" while the next '0' is supposed to be starting, the receiver sees a messy middle-voltage. It can no longer confidently decide if it's seeing a high or low signal, leading to bit errors.
<details>
<summary><strong>Wiring Diagram (click to expand)</strong></summary>

  ![Pic 48](LAB%20PICS/48.jpg)
  ![Pic 49](LAB%20PICS/49.jpg)
</details>
<details>
<summary><strong>Results (click to expand)</strong></summary>

 ![Pic 50](LAB%20PICS/50.png)

 
</details>

### **Signal Restoration (The Decision Circuit)**

Signal Thresholding
The rounded, bandwidth-limited signal was compared against a precise, adjustable voltage level. This threshold acts as a decision boundary: any voltage measured above this point is interpreted as a logical 1, while anything below is treated as a logical 0. By adjusting the variable DC threshold, the receiver can be "tuned" to the midpoint of the incoming pulses, maximizing its ability to distinguish between high and low states even when the signal is weak or rounded.

Digital Regeneration
Once the decision is made, the circuit performs a "snap" action. If the input exceeds the threshold, the output instantly jumps to a clean, full-scale high voltage. Conversely, if the input falls below, the output drops to a clean ground or negative voltage. This process "squares up" the waveform, eliminating the gradual slopes and noise introduced by the low-pass filter. The final output is a brand-new, sharp-edged version of the original bitstream, ready for processing by a computer or decoder.
<details>
<summary><strong>Wiring Diagram (click to expand)</strong></summary>

  ![Pic 51](LAB%20PICS/51.jpg)

  ![Pic 52](LAB%20PICS/52.jpg)
</details>
<details>
<summary><strong>Results (click to expand)</strong></summary>

 ![Pic 53](LAB%20PICS/53.png)

 
</details>

## Result and Data analysis

<details>
<summary><strong>Results (click to expand)</strong></summary>

 ![Pic s1](LAB%20PICS/s1.png)
  ![Pic s2](LAB%20PICS/s2.png)

 
</details>

