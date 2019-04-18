---
layout: page
title: Scenario 2
use-site-title: true
---



In this scenario, the robot is tasked to fetch a bottle in the kitchen. 
If an action fails, the robot asks for help to a human operator. 
The position of the kitchen is available in the blackboard. 
The map available to the robot contains all the obstacles that the robot will encounter
 (i.e. we do not consider dynamic obstacles).
 
This scenario is an extension of the [Scenario 1](../scenario1). The robot has to fetch the bottle in a room in the map
called Destination Room. The room's location is available in the blackboard. However, the robot may initially
not know the Destination Room. In that case, it follows a human operator. The human eventually tells to the
robot the destination room.
 
 
# Behavior Tree for Scenario 2
The figure below shows the BT that encodes the task for Scenario 2. The BT encodes the following logic:
 
![scenario2BT](https://user-images.githubusercontent.com/8132627/56295437-1ed1cf80-612d-11e9-83f2-d1756920e13e.png)

 - The robot first checks if the destination room is known. If not, it performs the action Follow Human.
 - If the robot knows the destination room, it checks if it is in the room. If not, it performs the action Goto Destination Room.
 - If the robot knows the destination room and the robot is in that room, the logic is the same of [Scenario 1](../scenario1).

# Execution of Scenario 2

The video below show the execution of Scenario 2

<iframe width="580" height="315" src="http://www.youtube.com/embed/q25uvU443Tg" frameborder="0" allowfullscreen></iframe>



