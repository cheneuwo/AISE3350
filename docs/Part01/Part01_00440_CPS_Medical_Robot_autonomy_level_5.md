(medical-robotics-level-5)=
# Level 5: Full Autonomy

At **Level 5**, the robotic system can perform an entire surgical procedure without requiring human direction or supervision during execution.

[Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638) describe this as a robotic surgeon. In their broad interpretation, such a system could undertake the range of procedures performed by a human specialist, such as a general surgeon.

## How Does This Differ from Level 4?

At Level 4, a qualified clinician supervises the robot’s medical decisions and actions. At Level 5, human participation is no longer required in the surgical decision-and-control loop.

The distinction is not simply whether the robot can complete a sequence of movements without assistance. Full autonomy encompasses the decisions needed to conduct the procedure, rather than only executing selected tasks.

:::{important} No human in the control loop does not mean no human involvement anywhere

Full surgical autonomy should not be interpreted as eliminating patients, consent, equipment maintenance, or institutional oversight.

The autonomy classification concerns the robot’s ability to make decisions and perform the surgical activity—not the removal of every human role in healthcare.

:::

## Current Status

**As of September 2026, no established clinical example of Level-5 surgical autonomy, in the broad sense described above, was identified for these notes.**

Research has demonstrated increasingly sophisticated autonomous surgical tasks. For example, [SRT-H](https://arxiv.org/abs/2505.10251) demonstrated autonomous execution of a substantial surgical phase in an experimental setting. Such results do not establish a generally capable robotic surgeon that can independently manage complete operations on human patients.

## Connection to Cyber-Physical Systems

Full autonomy would require more than precise motion control. The system would need to interpret changing anatomy, evaluate the effects of its actions, recognize unexpected conditions, and decide how to respond.

This makes surgical autonomy a useful illustration of a central CPS challenge: **reliable physical action depends on both sound decisions and accurate control**.

:::{note} Discussion

Suppose a robot completes a predefined surgical procedure successfully in a laboratory demonstration.

- What additional evidence would be needed before describing it as fully autonomous?
- How should it respond to a condition it cannot confidently interpret?
- Why is technical capability alone insufficient to establish readiness for clinical use?

:::