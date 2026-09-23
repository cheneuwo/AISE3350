(medical-robotics-level-3)=
# Level 3: Conditional Autonomy

At **Level 3**, the robotic system generates strategies for performing a task but relies on a human to **select a strategy** or **approve a strategy chosen by the system**.

In the framework proposed by [Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638), the robot can then execute the task without close human oversight. Human involvement shifts from directing individual movements towards selecting or authorizing how the task should be performed.

## How Does This Differ from Level 2?

At Level 2, the emphasis is on autonomously executing a human-initiated task. At Level 3, the system also contributes to **generating the task strategy**, while the human retains a selection or approval role.

The distinction is therefore not simply that the robot moves more accurately or performs a longer sequence of movements. It concerns the division of **planning, decision-making, and execution** between the human and the system.

## Example: Active Lower-Limb Prostheses

Yang and colleagues identify an active lower-limb prosthesis that infers the wearer’s intention to move and adjusts its behaviour without requiring direct attention to each adjustment as an example of conditional autonomy.

The wearer supplies the movement intention, while the prosthesis manages aspects of its physical execution. Unlike approving a surgical plan through a user interface, this interaction may occur through the wearer’s physical signals and movement.

For background on the technology, [Tomovic and colleagues (2026)](https://doi.org/10.1016/j.robot.2026.105487) review developments in active lower-limb prostheses, including actuation mechanisms and control approaches for supporting locomotion.

:::{important} Powered does not necessarily mean Level 3

An actuator makes a prosthesis active, but does not by itself establish conditional autonomy. Classification depends on how the device interprets user intent, determines its response, and shares control with the wearer.

Similarly, automatic adjustment does not imply unrestricted operation or an absence of safety limitations.

:::

## Connection to Cyber-Physical Systems

An intention-responsive prosthesis illustrates a tightly coupled human–machine CPS. Sensors provide measurements, computational models estimate the user’s movement state or intention, and actuators produce physical assistance. The resulting movement changes subsequent sensor measurements.

The engineering challenge is not merely to generate movement, but to generate movement that is consistent with the user’s intention. An incorrect estimate could produce assistance at the wrong time or in an inappropriate direction.

:::{note} Discussion

Consider a powered prosthesis intended to adjust its assistance as the wearer changes walking speed:

- What measurements might help distinguish an intended speed change from a stumble?
- How could uncertainty in that estimate affect the control response?
- Why is the presence of a motor insufficient to determine the device’s autonomy level?

:::