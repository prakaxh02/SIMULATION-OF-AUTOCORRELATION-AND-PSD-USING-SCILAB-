# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-
## AIM
Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB

## THEORY
The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.
<img width="582" height="91" alt="image" src="https://github.com/user-attachments/assets/dacf7cfd-96c5-45a6-aa31-321978d15f97" />

## ALGORITHM
1.	Load or Define the Signal: Input your time-domain signal.
2.	Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3.	Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.
4.	Plot Results: Visualize the autocorrelation function and PSD.

## PROCEDURE

•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

## PROGRAM
~~~
clear; clc;
xdel(winsid());  
gray = [0.8 0.8 0.8];  
f = gcf();
f.background = color(gray);
clf;
subplot(3,2,1);
t = 0:0.01:14;
plot(t, sin(t), 'b-.');
xgrid();
title("");

subplot(3,2,2);
t = 0:0.01:14;
y = cos(t) + 0.5*cos(2*t) + 0.2*cos(3*t);
plot(t, y, 'b-.');
xgrid();
title("");
subplot(3,2,3);
n = 0:1000;
u = ones(n);
plot(n, u, 'b');
axis([0 1000 0 2]);
xgrid();
title("");
subplot(3,2,4);
t = 0:0.1:2;
plot(t, t, 'b-.');
plot(t, -t, 'b-.');
axis([0 2 -2 2]);
xgrid();
title("");

subplot(3,2,5);
n = 0:1000;
d1 = zeros(n);
d1($) = 1;
plot(n, d1, 'b');
axis([0 1000 0 2]);
xgrid();
title("");
subplot(3,2,6);
d2 = zeros(n);
d2(1) = 1;
plot(n, d2, 'b');
axis([0 1000 0 2]);
xgrid();
title("");
~~~
## OUTPUT
<img width="754" height="569" alt="image" src="https://github.com/user-attachments/assets/bdfdf454-eb57-43ec-9ca6-ec7b721f4240" />

## RESULT
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.

