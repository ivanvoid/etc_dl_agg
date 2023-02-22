# Event trigger control Deep learning in RL setting
This repository is reflection on how to approch ETC with DL in RL setting.

## Event trigger control
Event-triggered control (ETC) is a control strategy that is used to reduce the communication and computational requirements of a control system, the controller sends control signals when a certain event or condition is met.


## Application of Deep learning
- ETC problem: Reacher environment with an ETC algorithm, where control signals are triggered based on the system state and the triggering condition to minimize the number of communications while achieving good reward.
- Expert model: DDPG 
- State and action spaces: state space as the end-effector position and velocity of the Reacher environment, and the action space as the joint angles of the robotic arm. Scale and normalize the state and action spaces.
- Reward function: Negative Euclidean distance between the goal position `g` and the end-effector position `e`  penalized by the number of control signals sent `n`: R = -||g - e||^2 - alpha * n  where g is the goal position, e is the end-effector position, ||.|| is the Euclidean distance, n is the number of control signals sent, and alpha is a hyperparameter that controls the penalty for sending control signals.
