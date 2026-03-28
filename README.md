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
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows

% INPUT SIGNAL-1
a=-3;
x=[2.3,1.2,-3.5,4.6,8.1];
n=a:1:length(x)+a-1;

figure(1)
stem(n,x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')

% INPUT SIGNAL 2
b=-1;
y=[3,2.5,-1.6,2.8,4.5,6];
m=4;
n1=b:1:length(y)+b-1;

figure(2)
stem(n1,y)
xlabel('Time')
ylabel('Amplitude')
title('Input signal-2')

% DISCRETE AUTO CORRELATED SIGNAL
out1=xcorr(x,x);
n2=a-m:1:length(out1)+a-m-1;

figure(3)
stem(n2,out1)
xlabel('Time')
ylabel('Amplitude')
title('Discrete auto correlated waveform')

% DISCRETE CROSS CORRELATED SIGNAL
out2=xcorr(x,y);
n3=a-m:1:length(out2)+a-m-1;

figure(4)
stem(n3,out2)
xlabel('Time')
ylabel('Amplitude')
title('Discrete cross correlated waveform')
```

## OUTPUT:
<img width="1918" height="1018" alt="image" src="https://github.com/user-attachments/assets/c5f17be5-0074-4881-8955-535648db1fb7" />
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/20694586-dc0d-42e6-90fe-e5c98920e2bb" />
<img width="1919" height="1016" alt="image" src="https://github.com/user-attachments/assets/a667c072-ed4c-4889-8d88-e54d7be66f73" />
<img width="1919" height="1019" alt="image" src="https://github.com/user-attachments/assets/0c795ea8-690b-4b3a-8a45-863ad117b88a" />


## RESULT:
The Cross correlation of X1[n] and X2[n] is y1[n] = {18.63,20.3,-30.88,19.72,105.75,19.72,-30.88,20.3,18.63}
The Auto correlation of X1[n] and X2[n] is y1[n] = {13.8,17.55,-9.16,11.53,63.33,64.83,10.17,-11.96,34.05,24.3}

