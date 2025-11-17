# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:

   <img width="290" height="915" alt="image" src="https://github.com/user-attachments/assets/45652135-561e-4fed-a204-7a4a12c5e308" />

 <img width="513" height="924" alt="image" src="https://github.com/user-attachments/assets/42db8d5c-5ab6-4c6c-b2df-c31662019de2" />


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
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
<img width="1625" height="913" alt="image" src="https://github.com/user-attachments/assets/0a0ef4c7-3e75-47a3-8306-302a33fb7580" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12

Phase Margin = 60.42

Gain crossover frequency = 0.90 rad/s

Phase crossover frequency = 4.47 rad/s

The system is STABLE
