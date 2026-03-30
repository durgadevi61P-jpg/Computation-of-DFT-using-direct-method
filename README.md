# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD
```
clc;
clear;
xn=[1 2 3 4 4 3 2 1];
n1=0:1:length(xn)-1;
subplot(3,1,1);
plot2d3(n1,xn);
xlabel('Time n');
ylabel('Amplitude xn');
title('Input Sequence');
j=sqrt(-1);
N=length(xn);
Xk=zeros(1,N);
for k=0:N-1
for n=0:N-1
Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
end
end
disp(Xk)
K1=0:1:length(Xk)-1;
magnitude=abs(Xk)
subplot(3,1,2);
plot2d3(K1,magnitude);
xlabel('frequency(Hz)');
ylabel('magnitude(gain)');
title('magnitude spectrum');
angle = atan(imag(Xk),real(Xk))
subplot(3,1,3);
plot2d3(K1,angle);
xlabel('frequency(Hz)');
ylabel('Phase');
title('Phase spectrum');
```
### CALCULATIONS:
<img width="725" height="1280" alt="image" src="https://github.com/user-attachments/assets/e75babbd-0166-4b8a-a27a-bb05f69e79e5" />

<img width="812" height="1280" alt="image" src="https://github.com/user-attachments/assets/3c480cfc-ad6f-4576-aba1-6d6e88ec0e8c" />


### SAMPLE OUTPUT:
<img width="1913" height="1105" alt="Screenshot 2026-03-23 215329" src="https://github.com/user-attachments/assets/db29a97b-b9dc-45a8-a91c-6e0513021222" />

## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

