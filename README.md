# PID Control

The combination of the three terms (P, I, and D) leads to the PID controller whose output variable y(t) is equal to the addition of the P, I, and D controllers which is described by the following equation:

y(t) = Kp * e(t) + Ki * Int(e(t) * dt) + Kd * de(t)/dt 

## Propotional Term
The propotional term makes the current error signal multiplied with a gain (Kp) to get the controllers output. 
A small propotional gain Kp leads to the setpoint, but the controller performance will be slow. If Kp is increased, the controllers output overshoots. 

## Integral Term
The integral term makes the current error signal value and duration multiplied with a Gain (Ki).
In addition, when the integral term is added to the propotional term, it accelerates the movement of the process towards setpoint and eliminates the residual steady-state error that occurs with a propotional only controller. 

## Derivative Term
The derivative term makes the rate of change of the error signal multiplied with a Gain (Kd).
Further, it slows the rate of change of the controller output and this effect is most noticeable close to the controller setpoint. 

## Tuning PID Hyperparameters

The PID hyperparameters were tuned experimental with the following algorithm[1]:

- Set all gains to 0.
- Increase Kd until the system oscillates.
- Reduce Kd by a factor of 2-4.
- Set Kp to about 1% of Kd.
- Increase Kp until oscillations start.
- Decrease Kp by a factor of 2-4.
- Set Ki to about 1% of Kp.
- Increase Ki until oscillations start.
- Decrease Ki by a factor of 2-4.

# References 
[1] https://robotics.stackexchange.com/questions/167/what-are-good-strategies-for-tuning-pid-loops
