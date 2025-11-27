# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

![WhatsApp Image 2025-11-27 at 22 09 01_c828fe9c](https://github.com/user-attachments/assets/60c3fea1-5872-4fde-8920-faa05667016f)

![WhatsApp Image 2025-11-27 at 22 09 01_4c570256](https://github.com/user-attachments/assets/98bc5966-f7e9-496e-9725-588ac04c8cf7)



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=[10]
den=[0.1 0.7 1 0]
sys=tf(num,den)
[mag,phase,W]=bode(sys)
mag=squeeze(mag)
phase=squeeze(phase)
phase1=deg2rad(phase)
polarplot(phase1,mag,'linewidth',1.5)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```
## Output:
<img width="690" height="607" alt="image" src="https://github.com/user-attachments/assets/cf3791e2-ba81-4f8a-9106-f71a98fafa8a" />

## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin =   0.7<br>
Phase Margin = -8.8865<br>
Gain crossover frequency = 3.7565<br>
Phase crossover frequency = 3.1623<br>
The system is unstable


