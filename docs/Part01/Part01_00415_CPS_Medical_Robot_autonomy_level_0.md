(medical-robotics-level-0)=
# Level 0: No Autonomy

At **Level 0**, the human operator directs the task, while the robot responds to the operator’s commands. The robot does not independently select clinical actions or determine how the procedure should proceed.

Examples include **teleoperated surgical robots** and **prosthetic devices operating directly in response to user commands**. A surgical robot with **motion scaling** also belongs to this category because its movements represent the surgeon’s intended actions, even when the magnitude of those movements is modified. These examples follow the framework proposed by [Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638).

## The Human Operator’s Role

The human operator remains responsible for:

- **Monitoring** the patient, instruments, and progress of the task.
- **Generating possible actions**, such as deciding where an instrument could move.
- **Selecting an action** based on clinical judgement.
- **Directing its execution** through commands to the robotic system.

The distinction is between deciding and directing the clinical action, which remain human functions, and physically producing the commanded movement, which may be performed by the robot.

## What Does the Robot Do?

The robot translates the operator’s commands into physical movement. Its sensors, actuators, and feedback controllers may regulate instrument position or velocity without giving it decision-making autonomy.

For example, suppose a motion-scaling system converts a **10 mm movement of the surgeon’s control handle into a 2 mm movement of the surgical instrument**. The robot implements the scaling, but the surgeon still determines the movement’s direction, timing, and purpose.

:::{important} No autonomy does not mean no robot

A Level-0 system can contain powered actuators, embedded computers, sensors, and sophisticated feedback control.

It is therefore not identical to non-robotic surgery. The defining characteristic is that the robot follows human-directed actions rather than independently choosing clinical actions.

:::

## Connection to Cyber-Physical Systems

A teleoperated robot remains a CPS: it senses operator inputs and instrument motion, processes those measurements, and controls physical actuators. The human supplies the task-level decisions, while the machine controls the execution of commanded movements.

This illustrates a key distinction: **automatic feedback control is not the same as autonomous decision-making**.

:::{note} Discussion

A surgical robot automatically corrects its motor commands to maintain the instrument position requested by the surgeon.

Does this feedback correction make the robot autonomous? Explain the difference between controlling a commanded movement and deciding which surgical action to perform.

:::