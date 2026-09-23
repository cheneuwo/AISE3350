(medical-robotics-level-2)=
# Level 2: Task Autonomy

At **Level 2**, the robot autonomously performs a **specific task initiated by a human**. The clinician defines or authorizes the task, monitors its execution, and intervenes when necessary.

The important distinction from Level 1 is that the operator exercises **discrete rather than continuous control**. Instead of directing each instrument movement, the clinician delegates a bounded task to the robot. This distinction follows the framework proposed by [Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638).

## The Human Operator’s Role

The clinician remains responsible for:

- Selecting the task and specifying its intended result.
- Initiating the robot’s execution of the task.
- Monitoring progress and intervening when necessary.
- Assessessing the result and deciding what should happen next.

Here, *discrete control* refers to task-level commands and interventions, rather than continuous manual guidance. It does not mean that supervision is unnecessary.

## Example: Surgical Suturing

In a task-autonomous suturing workflow, the surgeon specifies where a running suture should be placed. The robot then performs the suturing task without the surgeon manually directing every needle movement, while the surgeon monitors and intervenes as needed.

[Shademan and colleagues (2016)](https://doi.org/10.1126/scitranslmed.aad9398) demonstrated supervised autonomous suturing using robotic control and visual tracking of soft tissue. Their experiments included intestinal anastomosis—the joining of intestinal segments—in porcine tissue and living pigs.

This is particularly challenging because soft tissue can move and deform. The robot must therefore use sensory information during execution rather than simply replay a fixed sequence of movements.

:::{note} Task autonomy is not complete surgical autonomy

The cited study demonstrated supervised autonomous tasks in preclinical experiments. It did not establish that a robot could independently manage an entire operation on a human patient.

:::

## Example: Bone Drilling

Bone drilling can illustrate task autonomy when the clinician specifies the drilling objective and initiates execution, while the robot controls the drilling process.

For example, an experimental robotic drilling system investigated by [Kastelov and colleagues (2017)](https://doi.org/10.5430/jbei.v3n2p62) could drill to a predefined depth or detect the far bone cortex and stop automatically. The researchers evaluated the system using animal and human bone specimens outside the living body.

This illustrates the distinction between **guiding a tool** and **delegating a task**. A robot that holds a guide while the surgeon manually advances the drill does not exhibit the same task autonomy as one that controls the drilling progression and stopping condition.

For broader background, see [Fan and colleagues’ review of image-guided orthopaedic surgery](https://doi.org/10.1088/1361-6560/acaae9).

## Connection to Cyber-Physical Systems

At Level 2, the clinician supplies a task-level objective, while the robot uses sensing, computation, and feedback control to execute it. Depending on the application, relevant measurements may include tissue position, tool position, drilling depth, or interaction force.

The robot must also distinguish successful completion from conditions that require stopping or requesting human intervention.

:::{important} The key distinction

**Level 1:** The human continuously directs the task while the robot assists.

**Level 2:** The human initiates a specific task that the robot then executes autonomously under supervision.

:::

:::{note} Discussion

Compare two drilling systems:

1. A robot positions a guide, but the surgeon manually advances the drill.
2. A robot advances the drill to a clinician-specified depth and stops automatically.

Which system demonstrates task autonomy? What measurements and stopping conditions would the second system require?

:::