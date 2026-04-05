# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2012.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 
clc;
clear all;
close all;

% INPUT SIGNAL-1
a = input('enter the starting x(n)');
x = input('Enter the x(n) sequence');
n = a : 1 : length(x) + a - 1;
figure(1)
stem(n,x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')

% INPUT SIGNAL-2
b = input('enter the starting y(n)');
y = input('Enter the y(n) sequence');
m = input('enter the ending y(n)');
n1 = b : 1 : length(y) + b - 1;
figure(2)
stem(n1,y)
xlabel('Time')
ylabel('Amplitude')
title('Input signal-2')

% DISCRETE AUTO CORRELATED SIGNAL
Out1 = xcorr(x,x);
n2 = a - m : 1 : length(Out1) + a - m - 1;
figure(3)
stem(n2,Out1)
xlabel('Time')
ylabel('Amplitude')
title('Discrete auto correlated waveform')

% DISCRETE CROSS CORRELATED SIGNAL
Out2 = xcorr(x,y);
n3 = a - m : 1 : length(Out2) + a - m - 1;
figure(4)
stem(n3,Out2)
xlabel('Time')
ylabel('Amplitude')
title('Discrete cross correlated waveform')

## OUTPUT:
### INPUT SIGNAL-1:
<img width="1600" height="1298" alt="image" src="https://github.com/user-attachments/assets/bf5a5659-658b-4338-984d-e66ab1193fc1" />


### INPUT SIGNAL-2:
<img width="1600" height="1267" alt="image" src="https://github.com/user-attachments/assets/7f6fe691-fca5-4f4e-b4f1-1e10f0a56505" />


### DISCRETE AUTO CORRELATED :
<img width="1600" height="1306" alt="image" src="https://github.com/user-attachments/assets/f55700ac-3bc9-4111-9832-e0ecdee81b97" />

### DISCRETE CROSS CORRELATED :
<img width="1568" height="1304" alt="image" src="https://github.com/user-attachments/assets/60e01907-a601-450c-9c92-c24b07a02891" />

## RESULT:
![WhatsApp Image 2026-04-05 at 4 58 19 PM](https://github.com/user-attachments/assets/e2b8786f-f3b9-4be1-ad1f-e3a99380eb8b)



