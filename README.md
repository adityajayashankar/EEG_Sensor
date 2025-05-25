
# DESIGN AND IMPLEMENTATION OF ANALOF EEG SENSOR. <br>
### PROJECT AIM <br>
Design and implement a cost-effective, high-sensitivity, low-noise analog EEG sensor with a complete layout ready for tape-out.<br> 
This sensor will support accurate brain signal acquisition and seamless integration into brain-computer interface (BCI) systems, fostering wider accessibility and innovation in neurotechnology.<br>

### Instrumentation Amplifier Design Parameters

| **Parameter**     | **Designed Value** |
|-------------------|--------------------|
| Gain              | 52 dB              |
| Gain Bandwidth    | 1 – 100 Hz         |
| Phase Margin      | 45°                |
| Gain Resistor     | 500 Ω              |
| R1                | 10 KΩ              |
| Input Impedance (Zin)  | 10 MΩ        |
| Output Impedance (Zout) | 100 Ω       |


### Bandpass Filter Design Parameters

| **Parameter**           | **Designed Value**        |
|-------------------------|---------------------------|
| Lower Cutoff Frequency  | 1 Hz                      |
| Upper Cutoff Frequency  | 100 Hz                    |
| Bandwidth               | 1 – 100 Hz                |
| Quality Factor          | 100                       |
| Gain                    | 37 dB                     |
| Filter Order            | 2                         |
| Type                    | Active Bandpass Filter     |


### Notch Filter Design Parameters

| **Parameter**         | **Designed Value**            |
|-----------------------|-------------------------------|
| Center Frequency (fc) | 50 Hz                         |
| Gain Bandwidth        | 1 – 100 Hz                    |
| Quality Factor (Q)    | 100                           |
| Capacitance (C)       | 500 pF                        |
| Filter Type           | Two op-amp notch filter design |

## WORKING OF EACH COMPONENT : <br>

**1. INSTRUMENTAION AMPLIFIER** <br>
**Stage 1** : Buffering and Gain Setting <br>
Consists of 2 OpAmps and gain is controlled by single resistor (Rgain) between the 2 OpAmp. <br>
&nbsp;&nbsp;&nbsp;&nbsp;                      ``` GAIN = 1 + 2*R1 / Rgain  ``` <br>

**Stage 2** : Differential Amplifier<br>
The output of the first stage feed into the third op-amp, which acts as a differential amplifier.<br>
This stage amplifies the difference between the two input voltages and rejects common-mode signals.<br>
&nbsp;&nbsp;&nbsp;&nbsp;                          ```  Vout = GAIN * (R3/R2) * (V2 - V1) ``` <br>
<br>

**2. BANDPASS FILTER** <br>
A bandpass filter is created by combining a low-pass filter and a high-pass filter in series.<br>
The high-pass filter removes low-frequency signals below a certain cutoff frequency (f_low).<br>
The low-pass filter removes high-frequency signals above a certain cutoff frequency (f_high).<br>
The resulting filter only passes signals between f_low and f_high, which is the bandwidth of the filter.<br>
<br>
<br>
**3. NOTCH FILTER (2nd ORDER BANDSTOP)** <br>
The specific frequency that the filter is designed to eliminate.<br>
In this region, the signal’s amplitude is significantly reduced, creating the "notch".<br>

