# PID Controller

The objective of this project was to implement a PID controller in C++ to maneuver a vehicle around a track. 
The simulator provides the cross track error (CTE) and the velocity in order to compute the appropriate steering angle. 

## Propotional Term
The propotional term makes the current error signal multiplied with a gain (Kp) to get the controllers output. 
A small propotional gain Kp leads to the setpoint, but the controller performance will be slow. If Kp is increased, the controllers output overshoots. 

## Integral Term
The integral term makes the current error signal value and duration multiplied with a gain (Ki).
In addition, when the integral term is added to the propotional term, it accelerates the movement of the process towards setpoint and eliminates the residual steady-state error that occurs with a propotional only controller. 

## Derivative Term
The derivative term makes the rate of change of the error signal multiplied with a gain (Kd).
Further, it slows the rate of change of the controller output and this effect is most noticeable close to the controller setpoint. 

## Tuning PID Hyperparameters

The PID hyperparameters were tuned experimentally with the algorithm shown below[1] in order to control the steering angle based on the CTE while watching the effect on the behaviour of the car driving around the track.:

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
