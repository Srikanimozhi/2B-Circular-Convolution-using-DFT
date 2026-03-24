# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
## CIRCULAR CONVOLUTION
```asm
clc;
clear;
x = [3 -1 0 1 3 2 0 1 2 1];
n1 = 0:1:length(x)-1;
subplot(3,1,1);
plot2d3(n1,x);
xlabel('time');
ylabel('amplitude');
title('input sequence');
h = [1 1 1];  
n2 = 0:1:length(h)-1;
subplot(3,1,2);
plot2d3(n2,h);
xlabel('time');
ylabel('amplitude');
title('impulse sequence');
N1 = length(x);
N2 = length(h);
N  = max(N1,N2);
N3 = N1 - N2;
if (N3 > 0)
h = [h zeros(1,N3)];
else
x = [x zeros(1,abs(N3))];
end
disp(x)
disp(h)
for n = 1:N
y(n) = 0;
for i = 1:N
j = n - i + 1;
if (j <= 0)
j = N + j;
end
y(n) = y(n) + x(i) * h(j);   
end
end
disp(y)
n = 0:N-1;
subplot(3,1,3);
plot2d3(n,y);
xlabel('time');
ylabel('amplitude');
title('circular convolution');

```
### CALCULATIONS:
<img width="1600" height="938" alt="image" src="https://github.com/user-attachments/assets/b5ba395f-5cb4-46d8-a62a-af6b106c1f54" />

### SAMPLE OUTPUT:
![WhatsApp Image 2026-03-24 at 8 14 14 PM](https://github.com/user-attachments/assets/8f83f8db-b9db-4486-adb8-ff28c5e5e36e)


## RESULT:

Thus, the circular convolution of the two given sequences were performed and its result was verified.

