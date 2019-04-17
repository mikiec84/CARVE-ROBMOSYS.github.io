---
layout: page
title: Work Package 3
subtitle: Component-based Formal Development Approach
use-site-title: true
---

This work package is implemented by three tasks:

- Task 3.1 Extension of RobMoSys framework for formal behavioral modeling and composition through BT
approach: this task extends the RobMoSys framework through
a formal and systematic approach to robotic behaviors design and reuse. In particular, it leverages
previous work on formalizing Behavior Trees and on defining a requirements-to-design methodology
based on this formal notation. The objective is to enrich RobMoSys with a refinement-based
methodology for (hierarchical, modular, readable) definition of robotic behaviors.

- Task 3.2 Extension of Behavior Trees notation for robotic application:
this task assesses the gaps in the BT notation for an effective application in the field of robotic
applications. It incorporates feedbacks from the definition of the scenarios and provides
modifications to allow the expression of invariants and assumptions for correct execution of
the defined robotic behavior, compliant with the SMT-LIB standard for the integration of
industrial-strength SMT solvers in Work Package 5.

- Task 3.3 Semantic integration of the YARP platform concepts into RobMoSys framework: The first objective of this task is to map the R1 middleware (YARP) core
communication concepts onto the RobMoSys meta-model concepts. This will enable developers
to build YARP applications with the RobMoSys tools. The second objective is to formalize the
Model-Of-Computation provided by YARP, which is critical (1) for the adoption of BT to specify
robot behaviors in terms of orche
