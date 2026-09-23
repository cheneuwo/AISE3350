# Autonomy in Cyber-Physical Systems

Advances in sensors, actuators, computing resources, and communication technologies enable CPSs to perform increasingly complex tasks with less direct human intervention. Sensors provide information about the physical environment, computation supports interpretation and decision-making, and actuators translate decisions into physical actions. Connectivity can extend these capabilities by providing information from other systems and access to remote services.

Together, these capabilities support **automation** and **autonomy**. However, the presence of sophisticated hardware, powerful computers, or network connections does not, by itself, make a system autonomous.

## From Automation to Autonomy

**Automation** concerns the tasks that a system performs without direct human control. **Autonomy** concerns the extent to which a system can make and execute decisions without human intervention, within defined operating conditions.

These concepts are closely related, and their precise definitions vary across application domains. A system may automate a specific task while still depending on a human to select its objectives, supervise its operation, or respond when something goes wrong.

For example, a system might assist a person in performing a task, carry out a selected task under supervision, or undertake a broader activity with limited human involvement. Rather than treating autonomy as an all-or-nothing property, it is useful to examine how responsibilities are divided between the human and the system.

## Understanding Levels of Autonomy

Taxonomies of automation or autonomy provide a structured way to describe this division of responsibility. Across different applications, we can ask:

- **Task execution:** Which tasks does the system perform, and which remain with the human?
- **Decision-making:** Does the system follow human-selected actions, propose actions for approval, or select and execute actions independently?
- **Supervision and intervention:** Must a human continuously supervise, remain available to intervene, or take over when the system encounters a problem?
- **Operating conditions:** Under what circumstances is the system designed to perform these tasks?

These questions are more informative than simply asking whether a system is “autonomous.”

## Two Examples: Vehicles and Medical Robotics

The following pages examine two application domains:

- **Autonomous vehicles:** How are driving tasks, environmental monitoring, and responses to system limitations divided between the human driver and the automated system?
- **Medical robotics:** How are clinical task execution, action selection, supervision, and intervention divided between the clinician and the robotic system?

We will examine a six-level classification in each domain. Although both use levels numbered from **0 to 5**, their definitions are domain-specific. A particular level in driving automation should not be assumed to represent the same capabilities or responsibilities as the corresponding level in medical robotics.

:::{important}
A level of autonomy describes the system's role and the human involvement it requires. It is **not, by itself, a measure of safety, reliability, or overall quality**.

The appropriate level depends on the task, operating environment, and consequences of failure.
:::

For CPS design, the central question is therefore not simply **“How autonomous can the system become?”**, but **“Which responsibilities should the system assume, and what human involvement is needed for safe and effective operation?”**