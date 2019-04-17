---
layout: page
title: Scenario 1
use-site-title: true
---



In this scenario, the robot is asked to fetch a bottle in the kitchen. 
If an action fails, the robot asks for help to a human operator. 
The position of the kitchen is available in the blackboard. 
The map available to the robot contains all the obstacles that the robot will encounter
 (i.e. we do not consider dynamic obstacles).
 
 
# Behavior Tree for Scenario 1
The figure below shows the BT that encodes the task for Scenario 1. The BT encodes the following logic:
 
![scenario1BT](https://user-images.githubusercontent.com/8132627/56294629-a4548000-612b-11e9-82f0-7bbae290c2f4.png)
- The robot first checks if it is in the kitchen. If not, it performs the action _Goto Kitchen_.
- If the robot is in the kitchen, then it checks if the bottle is found. If not, it performs the action _Find Bottle_.
- If the robot is in the kitchen and it found the bottle, then it checks if the bottle is grasped. If not, it does the following:
  - It checks if the Inverse Pose (i.e. a pose of the robot such that the robot can locate and grasp the bottle) is computed and valid. If not, it performs the action _Compute Inverse Pose_.
  - If the Inverse Pose is computed and valid, the robot checks if it is at the Inverse Pose. If not, it performs the action _Goto Inverse Pose_.
  - If the Inverse Pose is computed and valid, and the robot is at it inverse pose, it checks if the bottle is located with a predefined confidence. If not, it performs the action _Locate Bottle_.
  - If the Inverse Pose is computed and valid, the robot is at the inverse pose, and the bottle is located with a given confidence. The robot performs the action _Grasp Bottle_.
  - If any of the action above fails, the robot sets the Inverse Pose as invalid and retries to grasp the bottle from a different inverse pose.
- If the robot cannot reach the kitchen or it cannot find the bottle, the robot asks for help to a human operator.

# Execution of Scenario 1

The video below show the execution of Scenario 1

<iframe width="580" height="315" src="http://www.youtube.com/embed/-b7TeRX1uzoc" frameborder="0" allowfullscreen></iframe>



