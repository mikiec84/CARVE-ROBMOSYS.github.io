---
layout: page
title: Results
subtitle: Dissemination and Deployment
use-site-title: true
---





# Overview

The resulting approach is illustrated in the figure below. 


![](../img/approach.png)

The user designs a robot behavior using [Behavior Trees](https://en.wikipedia.org/wiki/Behavior_tree_(artificial_intelligence,_robotics_and_control) ) to orchestrate [Skills](https://robmosys.eu/wiki-sn-03/modeling:metamodels:skill-definition) 
(as defined in [SmartSoft metamodel](https://robmosys.eu/wiki-sn-01/modeling:metamodels:start)).
Using an automatic tool, such Behavior Tree is compiled into executable code
using an execution engine. 
 
This engine is generated using the [Coq proof assistant](https://coq.inria.fr/) starting from the Behavior Tree description 
and a well-defined operational semantic. This engine is then loaded and executed 
as a SmartSoft component to orchestrate SmartSoft or YARP components.  

We use contracts and [contract-based design](https://it.wikipedia.org/wiki/Design_by_contract) as a methodology to describe 
skills and the use of off-the-shelf verification tools [NuSMV](http://nusmv.fbk.eu/) to statically verify 
correct execution of the Behavior Tree. To this end the Behavior Tree is translated to a 
Hierarchical Finite State Machine using an automatic tool. 

From the description of the Behavior Tree in terms of Hierarchical Finite State Machine 
another automatic tool can also generate runtime monitors. Monitors ensure 
that the properties assumed during the static verification of the Behavior Tree are still 
valid at runtime, and generate an exception otherwise.

We defined the three scenarios for the experimental validation of the CARVE 
methodology and tools. In summary they involve the implementation of 
a “fetch” behavior, in which the robot has to navigate to a given room, s
earch for an object, pick it up and bring it back to the user (Scenario 1).
 In Scenario 2 the robot may ask the user to show the location of the room and follow him, 
 if the room is not in the map (adding a human following behavior). 
 In Scenario 3 the task involves picking up a bottle, a glass, and pouring a drink to
  add a safety constraint to the task. These scenarios have been defined in terms of Behavior Trees.
  
  
  

# Contract-based design

The contract-based design methodology for has been used to validate the three reference scenarios.
We defined syntax and operational semantics for Behavior Trees. This allowed us to 
implement an automatic tool that can generate an execution engine which conforms
to the given semantics and that has guaranteed termination.

To support static verification of Behavior Trees we propose contract based design and verification
methodology for robotics. This  allowed us to verify desirable properties
 of the overall system model. The system model includes Behavior Tree, the skills it 
 coordinates and the environment. Properties are expressed in temporal logic and verified offline
  using the [NuSMV](http://nusmv.fbk.eu/)   model checker. 
The procedure is depicted in the figure below.


![](../img/contracts.png)


Videos showing the execution of the static analysis are in the [Media](../media#static) page.

# Runtime Monitoring
Runtime monitoring is used to carry out runtime verification, i.e., ensure that during deployment on the real robot
everything other than the BT behaves as expected. 

Given the abstract models for the skills and the environment, we can verify that at runtime, the skill and the evironment behave as expected.
Videos showing the execution of runtime monitors are in the [Media](../media#monitors) page.



# Integration with SmartSoft

For the integration of the Behavior Tree execution engine in SmartSoft we developed a 
dedicated component that can execute the engine. We also implemented the code to achieve
 interoperability between the SmartSoft toolchain and YARP (the middleware used 
 on the R1 robot).
 
To achieve better interoperability we also mapped the RobMoSys communication 
patterns into their YARP equivalent. We are currently working to support 
automatic generation of SmartSoft-YARP bridges in the form of mixed port 
components in tight collaboration with ULM.
A video showing this integration is available in the [Media](../media#yarpss) page.



# Integration with the Mood2Be ITP 

We also integrated the Behavior Tree graphical editor developed by the Mood2Be ITP (Groot) 
so that it can be used to design a Behavior Tree compatible with the CARVE toolchain and 
visualize the status of the execution engine. The Groot GUI has been used for 
the development and execution of the three Scenario [1](../scenario1), [2](../scenario2), and [3](../scenario3).






