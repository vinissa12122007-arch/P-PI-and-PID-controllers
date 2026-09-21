# Analysis of P, PI and PID Controllers using MATLAB
## Aim:
To analyse the effect of P, PI and PID controllers for the system having open loop transfer function, G(S)=1/(S^2+10S+20) using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
	A controller is a device introduced in the system to modify the error signal and to produce a control signal. 
	The way the controller produces the control signal is called the control action.

Consider the following unity feedback system,
 <img width="823" height="281" alt="image" src="https://github.com/user-attachments/assets/36e49512-cf47-4fec-b00c-f79dc0af1c5f" />

### Proportional (P) Controller:
The proportional controller produces an output, which is proportional to error signal.<br>
u(t)∝e(t) <br>
⇒u(t)=Kpe(t) <br>
Apply Laplace transform on both the sides - <br>
U(s)=KpE(s) <br>
U(s)/E(s)=Kp <br>
Therefore, the transfer function of the proportional controller is Kp.

### Proportional Integral (PI) Controller:
The proportional integral controller produces an output, which is the combination of outputs of the proportional and integral controllers. <br>
u(t)=Kp e(t)+Ki ∫e(t)dt <br>
Apply Laplace transform on both sides - <br>
U(s)=(Kp+Ki/s)E(s) <br>
U(s)/E(s)=Kp+Ki/s <br>
Therefore, the transfer function of proportional integral controller is Kp+Kis. <br>

### Proportional Integral Derivative (PID) Controller:
The proportional integral derivative controller produces an output, which is the combination of the outputs of proportional, integral and derivative controllers. <br>
u(t)=Kp e(t)+Ki ∫e(t)dt+ Kd (de(t)/dt) <br>
Apply Laplace transform on both sides - <br>
U(s)=(Kp+Ki/s+Kds)E(s) <br>
U(s)/E(s)=Kp+Ki/s+Kd s <br>
Therefore, the transfer function of the proportional integral derivative controller is Kp+Ki/s+Kd s

### Characteristics of Kp, Ki and Kd terms:

Increasing the proportional gain ( ) has the effect of proportionally increasing the control signal for the same level of error. The fact that the controller will "push" harder for a given level of error tends to cause the closed-loop system to react more quickly, but also to overshoot more. Another effect of increasing   is that it tends to reduce, but not eliminate, the steady-state error.
The addition of a derivative term to the controller ( ) adds the ability of the controller to "anticipate" error. With derivative control, the control signal can become large if the error begins sloping upward, even while the magnitude of the error is still relatively small. This anticipation tends to add damping to the system, thereby decreasing overshoot. The addition of a derivative term, however, has no effect on the steady-state error.
The addition of an integral term to the controller ( ) tends to help reduce steady-state error. If there is a persistent, steady error, the integrator builds and builds, thereby increasing the control signal and driving the error down. 
 


## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the steady state error and analyse the controllers.
## Program: 
### Without Controller (Open loop System)
<img width="636" height="243" alt="image" src="https://github.com/user-attachments/assets/2fe70f8a-94f8-43fd-bc29-0a16e8201235" />



### With P-Controller
<img width="565" height="209" alt="image" src="https://github.com/user-attachments/assets/a2d35a0b-a940-41fe-a45f-29b3a55d109d" />


### With PI Controller
<img width="565" height="209" alt="image" src="https://github.com/user-attachments/assets/0f7d929b-7bf1-44b6-bfd9-5c96c0e86bc9" />

### With PID Controller
<img width="565" height="209" alt="image" src="https://github.com/user-attachments/assets/2cfe9d96-a366-40ba-99c2-b21f6bb1c0a6" />


## Output: 
### Without Controller (Open loop System)
<img width="840" height="634" alt="image" src="https://github.com/user-attachments/assets/b53cc6af-9133-4523-b39b-58bab9daf406" />



### With P-Controller
<img width="832" height="627" alt="image" src="https://github.com/user-attachments/assets/e4947c29-c28b-4b57-be74-d884f00935a9" />


### With PI Controller
<img width="843" height="640" alt="image" src="https://github.com/user-attachments/assets/b33276af-762b-4f8a-83cf-67dee2a5f6b9" />


### With PID Controller
<img width="839" height="631" alt="image" src="https://github.com/user-attachments/assets/ca4abcda-fea2-45e5-8a58-b87f4a61eedb" />


## Result:
Thus the P, PI and PID controllers for the given system was analysed and the following conclusions were arrived using MATLAB. <br>
### With-out controller 
Delay time =         <0.5s>
Rise time =             <1s>
Peak time =           <2s>
Settling time =            <2s>
Steady State Error =        <0.95>
### With P Controller 
Delay time =         <0.1s>
Rise time =             <0.2s>
Peak time =           <0.3s>
Settling time =            <1s>
Steady State Error =        <0.12>
### With PI Controller 
Delay time =         <0.1s>
Rise time =             <0.175s>
Peak time =           <0.25s>
Settling time =            <3s>
Steady State Error =        <0>
### With PID Controller 
Delay time =         <0.01s>
Rise time =             <0.05s>
Peak time =           <1s>
Settling time =            <2.6s>
Steady State Error =        <0>




