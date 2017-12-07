# PID Control

The combination of the three terms (P, I, and D) leads to the PID controller whose manipulated output variable is equal to the addition of the P, I, and D controllers and is described by the following equation:

yR(t) = Kp*e(t) + Int(e(t)*dt) + Kd*de(t)/dt 

## Propotional Term
The propotional term makes the current error signal multiplied with a Gain (Kp).

## Integral Term
The integral term makes the current error signal value and duration multiplied with a Gain (Ki).
When added to the propotional term, it accelerates the movement of the process towards setpoint and eliminates the residual steady-state error that occurs with a propotional only controller. 
