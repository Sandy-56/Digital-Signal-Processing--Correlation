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

a=input('enter the starting x(n)');

x=input('Enter the x(n) sequence');

n=a:1:length(x)+a-1;

figure(1)

stem(n,x)

xlabel('Time')

ylabel('Amplitude')

title('Input Signal-1')

% INPUT SIGNAL 2

b=input('enter the starting y(n)');

y=input('Enter the y(n) sequence');

m=input('enter the ending y(n)');

nl=b: 1:length(y)+b-1;

figure(2)

stem(nl,y)

xlabel('Time')

ylabel('Amplitude')

title('Input signal-2')

% DISCRETE AUTO CORRELATED SIGNAL

out1=xcorr(x,x)

n2=a-m:1:length(out1)+a-m-1;

figure(3)

stem(n2,out1)

xlabel('Time')

ylabel('Amplitude')

title(' Discrete auto correlated waveform')

% DISCRETE CROSS CORRELATED SIGNAL

Out2=xcorr(x,y);

n3=a-m:1:length(Out2)+a-m-1;

figure(4)

stem(n3,Out2)

xlabel('Time')

ylabel('Amplitude')

title(' Discrete cross correlated waveform')
```


## OUTPUT:
<img width="521" height="394" alt="image" src="https://github.com/user-attachments/assets/2af35d65-c8a7-4cf3-8ae2-5c1ba5f8ff5d" />
<img width="478" height="390" alt="image" src="https://github.com/user-attachments/assets/c8888b48-ee35-4f77-891e-16a8947a8030" />
<img width="644" height="523" alt="image" src="https://github.com/user-attachments/assets/0cc73fcf-f5e5-4b37-9434-423fe7d4d2f6" />
<img width="658" height="428" alt="image" src="https://github.com/user-attachments/assets/5370b155-3ac0-40e7-9e2e-0ce9e320c25a" />



## RESULT:
The cross correlation of x1[n] and x2[n] is {6,14.1,-2.56,27.8,-12.4,51.24,-43.76,-18.8,32.2}

