---
layout: page
title: Scenario 3
use-site-title: true
---



This scenario is an extension of the [Scenario 2](scenario2). After the robot fetched the bottle, it has to pour its
content into a glass on the table. We assume that the glass is in a pose such that, after grasping the bottle, the
robot can pour the content of the bottle into the glass without moving the base. 
 
 
# Behavior Tree for Scenario 3
The figure below shows the BT that encodes the task for Scenario 3. The BT encodes the following logic:
 
![scenario1BT](https://user-images.githubusercontent.com/8132627/56294629-a4548000-612b-11e9-82f0-7bbae290c2f4.png)

 - If the robot is in the destination room with the bottle grasped (i.e. the logic described by the BT for
[Scenario 2](scenario2)), it checks if the content of the bottle is poured. If not it does the following.
  - It first checks if the glass is located with a predened condence. If not, it performs the action Locate Glass.
  - If the Glass is located with a predened condence, it performs the action Pour.


# Execution of Scenario 3

The video below show the execution of Scenario 3, focused on the pouring execution.

<iframe width="580" height="315" src="http://www.youtube.com/embed/-wE457T0718" frameborder="0" allowfullscreen></iframe>



