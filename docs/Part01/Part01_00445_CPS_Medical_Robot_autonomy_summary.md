(medical-robotics-summary)=
# Medical Robotics: Summary and Future Directions

Medical robotics illustrates how computation, sensing, and control can support increasingly capable interaction with the physical world. However, **precision, automation, and autonomy are different properties**. A robot may execute movements precisely while depending entirely on a clinician to decide what those movements should be.

The autonomy framework proposed by [Yang and colleagues (2017)](https://doi.org/10.1126/scirobotics.aam8638) describes how decisions and actions can be divided between humans and robotic systems.

## Summary of the Six Levels

| Level | Classification | Central distinction |
| :---: | :--- | :--- |
| 0 | No autonomy | The robot follows human commands. |
| 1 | Robot assistance | The robot assists while the human maintains continuous control. |
| 2 | Task autonomy | The robot executes a specific human-initiated task under supervision. |
| 3 | Conditional autonomy | The robot develops strategies that the human selects or approves. |
| 4 | High autonomy | The robot makes medical decisions under qualified clinical supervision. |
| 5 | Full autonomy | The robot performs the surgical activity without requiring human participation in its decision-and-control loop. |


```{figure} https://www.science.org/cms/10.1126/scirobotics.aam8638/asset/3b604d9a-6231-4d2a-96cd-b2a109755ecf/assets/graphic/aam8638-f1.jpeg
:label: fig-driving-level-3
:alt: Vehicle Autonomy, level 3.
:width: 600px
:align: center
```

These levels describe the **allocation of control and decision-making**, not a ranking of clinical quality. The appropriate level depends on the task, operating conditions, and evidence of safety and effectiveness.

## Beyond Precise Movement: Sensorimotor Intelligence

Higher autonomy requires more sophisticated interpretation of sensory information. A surgical robot must do more than identify an instrument or anatomical structure: it must relate what it observes to the physical consequences of its actions.

Relevant information may include images, instrument position, interaction forces, and tissue motion. These measurements can be incomplete, noisy, or contradictory.

Yang and colleagues emphasize the importance of reproducing an expert surgeon’s **sensorimotor capabilities**: the close coordination of perception and skilled physical action. This extends the familiar **sense–think–act** cycle:

- **Sense:** Estimate the state of the instruments, tissues, and surrounding environment.
- **Think:** Determine an appropriate action and assess uncertainty.
- **Act:** Execute the movement within relevant constraints.
- **Observe again:** Evaluate the result and update the next action.

The cycle is continuous. Physical actions change the environment, which changes the measurements available for subsequent decisions.

## Towards Embodied and Physical AI

An important research and industry direction is **embodied AI**, often discussed alongside **physical AI**. These terms emphasize AI systems that interact with the physical world through sensing and action, rather than producing only digital outputs. See this [introduction to physical AI](https://docs.nvidia.com/learning/physical-ai/).

For medical robotics, the objective is to connect perception and task understanding with controlled physical behaviour. **Vision–language–action (VLA) models**, for example, connect visual observations and language instructions to robot actions.

This does not remove the need for control theory. A learned model may propose an action, but the robot must still execute it with appropriate timing, stability, accuracy, and constraint enforcement.

## Research Example: Open-H-Embodiment

[Open-H-Embodiment](https://open-h.github.io/open-h-embodiment/) is a collaborative dataset initiative supporting foundation models for medical robotics. Its project page reports **780 hours of synchronized video and robot kinematics**, covering **20 robotic platforms** and contributions from **50 institutions**.

The project demonstrates two research directions:

- **GR00T-H:** A vision–language–action model for medical robotic tasks.
- **Cosmos-H-Surgical-Simulator:** An action-conditioned model for generating surgical scene sequences, supporting simulation and research evaluation.

Combining observations with recorded robot movements can help researchers investigate how actions affect surgical scenes and how learned behaviours transfer across robotic platforms.

:::{important} Research performance is not clinical readiness

The project reports a **25% end-to-end completion rate on one structured suturing benchmark**. This result illustrates both progress and the difficulty of reliably completing a sequence of dependent actions.

A successful demonstration, dataset release, or benchmark improvement does not establish Level-5 autonomy or readiness for clinical use.

:::

## Safety, Cybersecurity, and Privacy

Reducing human oversight changes how failures must be detected and managed. Errors in perception, planning, or control may propagate into physical actions before a clinician can intervene.

However, greater autonomy does not inevitably increase overall risk: automation may reduce some human errors while introducing different failure modes. Safety must be evaluated for the complete human–robot system and its intended use.

Connectivity introduces additional concerns. Unauthorized changes to software, commands, or data can affect device behaviour, while disclosure of medical information can compromise privacy. The [FDA’s medical-device cybersecurity resources](https://www.fda.gov/medical-devices/digital-health-center-excellence/cybersecurity) emphasize cybersecurity as part of protecting device safety and effectiveness.

## Future Engineering Priorities

From a CPS perspective, several priorities follow:

- **Robust sensing:** Combine measurements and recognize when observations are unreliable.
- **Uncertainty-aware decisions:** Detect unfamiliar conditions and identify when assistance is needed.
- **Safe control:** Enforce physical constraints even when a proposed action is inappropriate.
- **Generalization:** Evaluate performance across anatomy, tissue conditions, equipment, and clinical settings.
- **Human–robot coordination:** Make system intentions, limitations, and intervention needs understandable.
- **Responsible data use:** Address data quality, representativeness, privacy, access, and provenance.

:::{note} Discussion

A robot performs well on data from one hospital but is deployed with different instruments and imaging conditions.

- Which parts of the sense–think–act cycle might be affected?
- How could the system recognize that its predictions are becoming unreliable?
- What evidence would be needed before reducing human oversight?

:::

## Takeaway

The future of medical robotics is not simply about removing the human operator. It is about determining which decisions and actions can be delegated safely, under what conditions, and with what evidence.

**More capable AI expands what a robot may attempt; dependable CPS engineering determines whether it can do so reliably.**