(medical-robotics-level-1)=
# Level 1: Robot Assistance

At **Level 1**, the robot provides mechanical guidance or assistance during a task while the human operator maintains **continuous control**. The clinician directs the procedure, while the robotic system helps guide or constrain the execution of movements.

In the framework proposed by [Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638), **virtual fixtures**, also called active constraints, are an example of this level of assistance.

## The Human Operator’s Role

The clinician continues to:

- Decide which clinical action to perform.
- Direct the instrument’s movement throughout the task.
- Monitor the patient and the progress of the procedure.
- Decide when to stop or change the intended action.

The robot assists with execution; it does not independently undertake a complete surgical task.

## Virtual Fixtures and Active Constraints

A **virtual fixture** is a software-defined guide or constraint that influences how a robotic instrument can move. It can help guide the instrument along a desired path or restrict movement towards a region that should be avoided.

Unlike a physical cutting guide, a virtual fixture is implemented through computation and robotic control. The system uses measurements of instrument position and, where applicable, registered anatomical information to determine how assistance should be applied.

For example, [Park, Howe, and Torchiana (2001)](https://doi.org/10.1007/3-540-45468-3_252) investigated virtual fixtures for robotic cardiac surgery. Their work explored constraining surgeon-commanded instrument movements near an artery and demonstrated a virtual wall in a preliminary dissection task.

This illustrates **shared control**: the surgeon supplies the intended movement, while the robot helps keep its execution within defined constraints.

## Tremor Filtering and Compensation

**Physiological tremor** consists of small, involuntary movements that can interfere with delicate manipulation. Tremor-filtering algorithms seek to distinguish these movements from the operator’s intended motion, allowing the robotic system to reduce their effect on the instrument.

[Veluvolu and Ang (2010)](https://doi.org/10.1002/rcs.340) investigated methods for estimating and filtering physiological tremor in real time for surgical robotics applications.

:::{note} Assistance does not automatically establish an autonomy level

Tremor compensation can improve movement quality, but its presence alone does not establish Level 1. A system that only filters user commands may still function as a Level-0 teleoperated system.

Yang and colleagues explicitly identify virtual fixtures and active constraints as Level-1 examples. Classification should therefore consider the system’s overall behaviour and the division of control, rather than the presence of a single feature.

:::

## Connection to Cyber-Physical Systems

Virtual fixtures demonstrate how a digital constraint can influence physical movement. Sensors measure instrument motion, software evaluates that motion relative to a defined boundary, and actuators provide corrective guidance or resistance.

The clinician remains continuously involved in directing the task. The robot contributes assistance to its execution rather than independently choosing and completing the task.

:::{note} Discussion

A surgeon moves a robotic instrument towards a protected anatomical region. The robot resists further movement at a predefined virtual boundary.

- Which decisions remain with the surgeon?
- What measurements does the robot need to enforce the boundary?
- How could an error in registering the patient’s anatomy affect this assistance?

:::