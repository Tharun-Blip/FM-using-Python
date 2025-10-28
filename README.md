# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program:
```
import numpy as np
import matplotlib.pyplot as plt

Am = 4.8
Ac = 9.6
fm = 374
fc = 3740
beta = 5

t = np.linspace(0, 0.005, 10000)

message = Am * np.sin(2 * np.pi * fm * t)
carrier = Ac * np.sin(2 * np.pi * fc * t)
fm_signal = Ac * np.sin(2 * np.pi * fc * t + beta * np.sin(2 * np.pi * fm * t))

plt.figure(figsize=(10, 7))
plt.subplot(3, 1, 1)
plt.plot(t, message)
plt.subplot(3, 1, 2)
plt.plot(t, carrier)
plt.subplot(3, 1, 3)
plt.plot(t, fm_signal)
plt.tight_layout()
plt.show()
```



Output Waveform:
<img width="994" height="589" alt="image" src="https://github.com/user-attachments/assets/ccc486b2-6056-4651-aa71-c4e9160d7e7e" />



Tabular Column:
![WhatsApp Image 2025-10-28 at 22 17 28_b3a6f7dd](https://github.com/user-attachments/assets/7891e2da-01cd-435d-b1d0-e951fd370828)




Calculation:
![WhatsApp Image 2025-10-28 at 22 18 24_4d46de45](https://github.com/user-attachments/assets/ea222f81-c5c0-4a35-9ef5-9f264eb7885a)





Result:


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
