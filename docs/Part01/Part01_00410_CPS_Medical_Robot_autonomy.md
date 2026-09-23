(medical-robotics-autonomy-levels)=
# Levels of Autonomy in Medical Robotics

The previous example showed how robotic assistance can improve the execution of a surgical task. However, precise movement alone does not establish autonomy. We must also consider **who determines what to do**, **who performs the task**, and **what supervision is required**.

[Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638) proposed six levels of autonomy for medical robots, ranging from systems that follow human commands to systems that can operate without human involvement.

## The Six Levels

| Level | Classification | Human–robot relationship |
| :---: | :--- | :--- |
| 0 | **No autonomy** | The robot follows the operator’s commands without independently deciding what to do. |
| 1 | **Robot assistance** | The robot provides guidance or assistance while the operator maintains continuous control. |
| 2 | **Task autonomy** | The robot executes a human-initiated task; the operator monitors and can intervene. |
| 3 | **Conditional autonomy** | The robot develops task strategies, while the human selects or approves the strategy to execute. |
| 4 | **High autonomy** | The robot makes medical decisions under the supervision of a qualified clinician. |
| 5 | **Full autonomy** | The robot can undertake an entire surgical procedure without requiring a human in the control loop. |

## How Are These Levels Distinguished?

For each medical robotic application, consider four questions:

1. **Planning:** Who develops and selects the strategy?
2. **Execution:** Who controls the physical actions?
3. **Supervision:** Does the clinician guide movements continuously, monitor individual tasks, or oversee broader decisions?
4. **Intervention:** When must the clinician approve an action or take control?

These questions connect autonomy to the CPS cycle of sensing, computation, and physical action.

:::{important} A framework, not a clinical standard

These categories were proposed to support discussion of medical robotics and its regulatory, ethical, and legal implications. A level of autonomy is not evidence of safety or authorization for clinical use.

:::

## Why Context Matters

The same autonomy level can present different challenges in a surgical robot, a prosthetic limb, or a home-assistance robot. The task, operating environment, and consequences of failure must therefore accompany any level designation.

The following pages examine each level, focusing on the division of decisions and actions between the clinician and the robot.