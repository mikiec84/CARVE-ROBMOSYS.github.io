---
layout: page
title: Work Package 5
subtitle: Tool for Behavior Tree Integration and Verification
use-site-title: true
---

This work package is implemented by three tasks:


- Task 5.1 Semantic preservation proof of the correctness of BT to DFSM transformation: this task ensures that the high-level design of behaviors with BTs fits the Rob-
MoSys framework and that the corresponding encoding implements correctly the semantics of
BTs. To meet both requirements, this task seeks to provide a formal assurance that the compiler
correctly implements the BT, yielding a representation which can be plugged in the RobMoSys
framework flawlessly.
[Deliverable 5.1](https://github.com/CARVE-ROBMOSYS/Coordination/blob/master/deliverables/D5.1%20Model%20transformation%20and%20correctness%20proof.pdf) presents the reults obstained within this task.

- Task 5.2 Design time verification of behavior invariants: this task
implements verification tools, either in the form of DFSM verification against requirements when
the latter can be expressed in some logical, yet tractable way, or in the form of automated-test
pattern generation to cover requirements and/or elements of the DFSMs (states, transitions,
subsets of specific behaviors).
[Deliverable 5.2](https://github.com/CARVE-ROBMOSYS/Coordination/blob/master/deliverables/D5.2%20Tools%20for%20verification%20of%20Behavior%20Trees.pdf) presents the reults obstained within this task.

- Task 5.3 Runtime verification of behavior invariants: this task
extends and complements the tool developed in Task 5.2, so that runtime monitors can be generated
to cover cases in which design-time assumptions fail to be satisfied during operations.
[Deliverable 5.3](https://github.com/CARVE-ROBMOSYS/Coordination/blob/master/deliverables/D5.3%20Combining%20Statis%20and%20Runtime%20Verification%20of%20Behavior%20Trees.pdf) presents the reults obstained within this task.
