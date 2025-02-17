# Forward-Kinematics-for-a-Two-Link-Robotic-Arm

(Introduction):

This document presents the mathematical equations for the Forward Kinematics (FK) of a two-link robotic arm. Forward Kinematics is used to determine the position of the end effector (the tip of the robotic arm) based on the given joint angles.

--------------------------------------------------------------------------------------------------

 (System Overview)
The robotic arm consists of:

Two links connected by two rotational joints.
Each joint has a rotation angle (( heta_1) and ( heta_2)).
The goal is to compute the (X, Y) position of the end effector.

-----------------------------------------------------------------------------------------------

 (Given Parameters):
 
( L_1 = 10 ) cm → Length of the first link
( L_2 = 15 ) cm → Length of the second link
( heta_1 ) → Rotation angle of the first joint
( heta_2 ) → Rotation angle of the second joint

---------------------------------------------------------------------------------------------

 Forward Kinematics Equations
To calculate the end effector's (X, Y) coordinates, we use trigonometric functions:
![image](https://github.com/user-attachments/assets/0d82d966-7fc5-40b5-b428-1d2467d5061c)

Understanding the Motion:

**The first term ( L_1 \cos(\theta_1), L_1 \sin(\theta_1) ) gives the position of the first joint.

**The second term ( L_2 \cos(\theta_1 + \theta_2), L_2 \sin(\theta_1 + \theta_2) ) adds the position of the second link relative to the first.


------------------------------------------------------------------------------------------------

(Example Calculation):
Assume:

( \theta_1 = 30^\circ )

( \theta_2 = 45^\circ )

Convert angles to radians and apply:

![image](https://github.com/user-attachments/assets/750edde5-2561-4962-ae50-a706d9557f73)

Using trigonometric values:

( \cos(30^\circ) \approx 0.866 ), ( \sin(30^\circ) \approx 0.5 )

( \cos(75^\circ) \approx 0.258 ), ( \sin(75^\circ) \approx 0.966 )

(Final results):

X \approx 12.53 cm

Y \approx 19.49 cm

---------------------------------------------------------------------------------------------


(For Future Work):

Implement Inverse Kinematics to calculate joint angles from a given (X, Y) position.

Develop an Arduino program to control a real robotic arm.
