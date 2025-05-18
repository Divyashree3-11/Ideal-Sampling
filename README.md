# Ideal-Sampling
# Aim
Write a Python program for the Construction and Reconctruction of Samples. (Ideal Method)
# Tools required:
Python with Numpy and Scipy
# Program
```
#Impulse Sampling
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
# Output Waveform:

![image](https://github.com/user-attachments/assets/4f4508c3-c328-4c1b-87e7-c1e29738f6a5)

![image](https://github.com/user-attachments/assets/2e472552-07f9-4381-8e92-4584c70cff47)

![image](https://github.com/user-attachments/assets/da506598-ea9e-4e8d-9d0b-a99b584fcfe2)

# Results:

 Thus, Construction and Re-construction of Ideal or Impulse Sampling has been
 verified using python.
# Hardware experiment output waveform.
![WhatsApp Image 2025-04-26 at 21 07 04_2a470b09](https://github.com/user-attachments/assets/d22ad424-2033-4fb1-a5a3-e4f45ecaa34f)
