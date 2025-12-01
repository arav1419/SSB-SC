# SSB

# EXP NO: 3	SSB-SC-AM MODULATION using SCILAB

# AIM:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

# EQUIPMENTS REQUIRED

•	Computer with i3 Processor

•	SCI LAB

Note: Keep all the switch faults in off position


# ALGORITHM
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: The baseband signal that will be modulated.
•	Carrier Signal: A high-frequency signal used for modulation.
•	Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
3.	SSBSC Modulation:
•	Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
4.	SSBSC Demodulation:
•	Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
•	Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
5.	Visualization:
•	Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.


# PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

# MODEL WAVEFORM

<img width="704" height="178" alt="image" src="https://github.com/user-attachments/assets/32ee29b3-0d95-4192-9762-972d50c05c90" />
<img width="706" height="167" alt="image" src="https://github.com/user-attachments/assets/bff0d8fd-d679-444e-af37-0b34585853c1" />

# Program
```
ac=57.2; 
Am=28.6; 
fc=9100;
fm=910;
fs=25000; 
t=0:1/fs:2/fm; 
wc=2*3.14*fc;
wm=2*3.14*fm;
e1=(Am*sin(wm*t));
subplot(4,1,1);
plot(t,e1); 
xlabel("Time(s)");
ylabel("Amplitude");
title("Message Signal m(t)");
e2=(ac*sin(wc*t)); 
subplot(4,1,2); 
plot(t,e2);
xlabel("Time(s)");
ylabel("Amplitude");
title("Carrier Signal c(t)");
sbsc1=(Am/2.*cos(wc*t-wm*t))-(Am/2.*cos(wc*t+wm*t));
sbsc2=(Am/2.*cos(wc*t-wm*t))+(Am/2.*cos(wc*t+wm*t)); 
e3=(sbsc2)+(sbsc1); 
subplot(4,1,3);
plot(t,e3);
xlabel("Time(s)");
ylabel("Amplitude");
title("SSB-SC Modulated Signal (LSB)");
e4=(sbsc2)-(sbsc1); 
subplot(4,1,4); 
plot(t,e4);
xlabel("Time(s)");
ylabel("Amplitude");
title("SSB-SC Modulated Signal (USB)");
xgrid;
```


# OUTPUT WAVEFORM
![WhatsApp Image 2025-11-04 at 18 25 39_7b4b77a8](https://github.com/user-attachments/assets/64b1c0db-38ad-4003-9105-1446ac1174b4)

# TABULATION
![WhatsApp Image 2025-11-04 at 20 47 05_71dd0021](https://github.com/user-attachments/assets/69df7ddc-9de6-46ef-800f-4fc45be58118)

# CALCULATION
![WhatsApp Image 2025-11-04 at 20 47 22_0106ef8a](https://github.com/user-attachments/assets/6846acea-7be0-4d43-8bee-4dc39131dae7)

# RESULT
![WhatsApp Image 2025-11-16 at 21 24 10_d1fad215](https://github.com/user-attachments/assets/d53245a6-2007-4b47-b3fc-4f9fe490e18f)






