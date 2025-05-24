
# DESIGN AND IMPLEMENTATION OF ANALOF EEG SENSOR. <br>
PROJECT AIM : Design and implement a cost-effective, high-sensitivity, low-noise analog EEG sensor with a complete layout ready for tape-out.<br> 
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

