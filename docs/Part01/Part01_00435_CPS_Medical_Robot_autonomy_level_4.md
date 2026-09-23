(medical-robotics-level-4)=
# Level 4: High Autonomy

At **Level 4**, the robot can make medical decisions while operating under the supervision of a qualified clinician.

[Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638) describe this relationship using the analogy of a **robotic resident** performing surgery under an attending surgeon’s supervision. The robot has substantial independence in decision-making and execution, but human clinical oversight remains part of the arrangement.

## How Does This Differ from Level 3?

At Level 3, the system develops task strategies but relies on the human to select or approve a strategy. At Level 4, the robot has greater authority to make medical decisions within the supervised activity.

The distinction therefore concerns **decision-making authority**, not simply whether the robot can complete a long sequence of movements.

## The Human Supervisor’s Role

The supervising clinician is not required to direct every instrument movement. However, supervision should not be interpreted as merely having access to an emergency-stop button.

Yang and colleagues do not prescribe a particular intervention interface or limit the clinician’s involvement to stopping the robot. The appropriate interaction between clinician and machine depends on the application and its safety requirements.

:::{important} High autonomy does not guarantee task completion

The framework does not state that a Level-4 medical robot must complete its task if a human fails to respond to an intervention request.

As an engineering consideration, continuing is not always the safest response. A system may need to pause, maintain a controlled state, or request assistance when it encounters conditions outside its capabilities.

:::

## Connection to Cyber-Physical Systems

Consider a hypothetical robot that encounters unexpected tissue movement while performing a supervised procedure. Correcting the instrument’s position is a control problem; deciding whether to continue, change the approach, or stop introduces a higher-level decision problem.

This illustrates the coupling between **perception**, **decision-making**, and **physical action**. A reliable controller cannot compensate for an inappropriate clinical decision, just as a sound decision cannot guarantee safety if the physical action is executed incorrectly.

:::{note} Discussion

A supervised surgical robot detects an unexpected condition and requests assistance, but the clinician does not immediately respond.

- What information would help determine whether the robot should continue or pause?
- Why might an immediate stop also create difficulties during some surgical tasks?
- What should the robot communicate to support the clinician’s intervention?

:::