# PID Control

The combination of the three terms (P, I, and D) leads to the PID controller whose output variable y(t) is equal to the addition of the P, I, and D controllers which is described by the following equation:

y(t) = Kp*e(t) + Int(e(t)*dt) + Kd*de(t)/dt 

## Propotional Term
The propotional term makes the current error signal multiplied with a Gain (Kp) to get the controllers output. 
A small Kp leads to the setpoint, but your controller performance will be slow. If Kp is increased, the output overshoots. 

## Integral Term
The integral term makes the current error signal value and duration multiplied with a Gain (Ki).
In addition, when the integral term is added to the propotional term, it accelerates the movement of the process towards setpoint and eliminates the residual steady-state error that occurs with a propotional only controller. 

## Derivative Term
The derivative term makes the rate of change of the error signal multiplied with a Gain (Kd).
Further, it slows the rate of change of the controller output and this effect is most noticeable close to the controller setpoint. 
