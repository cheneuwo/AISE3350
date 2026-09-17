# Key Features of Cyber-Physical Systems

Cyber-physical systems are ubiquitous in modern society. Examples include autonomous vehicles, industrial robots, smart buildings and cities, and large-scale electrical networks. Although these systems operate in different physical environments, they share several important characteristics. Alur identifies five distinguishing characteristics of cyber-physical systems [@Alur2015]:

1. **Reactive computation**
1. **Concurrency**
1. **Feedback control of the physical world**
1. **Real-time computation**
1. **Safety-critical applications**

A timely example (as of 2026-08-31) that illustrates all five characteristics is a **humanoid robot**.

## Humanoid Robots as Cyber-Physical Systems

Humanoid robots have advanced considerably in recent years and are now [capable of performing household and industrial tasks such as folding laundry and welding](https://www.bbc.com/news/articles/c62m4zn1q6mo). The following BBC video shows humanoid robots participating in running competitions:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/FGBLzMESBAo?si=ZbzM7T8L79XOc1gB"
    title="BBC report on humanoid robots"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

At first glance, the robot's most impressive feature may be its speed. From a cyber-physical systems perspective, however, maintaining balance and dynamic stability without falling is an even more demanding task. Toward the end of the race, notice the challenge of stopping gracefully: many humanoid robots simply fall or run into a padded barrier after crossing the finish line. Bipedal robotics is inherently difficult because of control-design challenges that include, but are not limited to, the following [@LCP+2021,MMA+2022]:

- Bipedal robots have unstable structures due to the passive joints located at the unilateral contact between the foot and the ground;
- One-sided contact of the foot with the ground and a complex configuration of the gait cycle bring about the highly non-linear trajectory of the bipedal robot;
- Bipedal robots have many degrees of freedom. Researchers often use simplified models to balance computational tractability and model fidelity;
- Bipedal robots are often designed to interact with unknown environments and are expected to achieve a high level of autonomy;
- Simulation is an important component of many control strategies for bipedal locomotion.

The humanoid robot provides a particularly useful example because the interaction between its cyber and physical components is easy to observe.

## Reactive Computation

In the classical model of computation, a computing device produces an output from a given input. For example, a [sorting algorithm](wiki:Sorting_algorithm) takes a list of numbers as input and returns those numbers in sorted order as output. Depending on the [algorithm](wiki:Algorithm) used, the way in which the computation is performed and its computational complexity are generally well understood. Mathematical expressions and algorithms are often abstracted as functions and procedures, allowing increasingly complex computational methods to be built by composing simpler functions. The correctness of such a program is often characterized mathematically by a *function* that maps input values to output values.

A *reactive* system, in contrast, interacts with its environment in an **ongoing manner** through inputs and outputs [@Alur2015]. A bipedal robot programmed to traverse a given environment may encounter, for example, uneven ground or obstacles along its path. These conditions may not -- and often cannot -- be fully accounted for during path planning. The robot must therefore react to conditions that were not included in its original plan. The behaviour of a reactive system is naturally described by a *sequence* of observed inputs and outputs, and its correctness specifies which input–output sequences correspond to acceptable behaviour.

## Concurrency

In a traditional *sequential* model of computation, a sequence of instructions is executed one instruction at a time. A humanoid robot, however, does not perform only one task at a time. Many physical and computational processes occur simultaneously. This simultaneous activity is called **concurrency**. Multiple threads of computation -- that is, multiple components or processes -- execute concurrently and exchange information to achieve the desired system behaviour. At any given time, the humanoid robot may be required to:

- perceive its dynamic environment using cameras and algorithms such as [SLAM](wiki:Simultaneous_localization_and_mapping) for three-dimensional reconstruction, [image segmentation](wiki:Image_segmentation), and [object detection](wiki:Object_detection);
- compute the poses (positions and orientations) of its end effectors using [joint kinematics](wiki:Kinematic_chain);
- estimate its centre of mass; and
- determine how to move while maintaining stability.

Both the acquisition rates of the sensor data streams and the subsequent processing, communication, and actuation times may differ among sensors and actuators

```{admonition} Concurrency
:class: important

Understanding models and design principles for *distributed* and *concurrent* computation is critical for CPSs. Broadly, these models can be divided into:

1. *synchronous* models, in which components execute in lock-step and computation progresses through a logical sequence of synchronized rounds; and
2. *asynchronous* models, in which components execute at independent rates and exchange information by sending and receiving messages.
```

A detailed treatment of concurrency is beyond the scope of this course.

## Feedback Control of the Physical World

The majority of this course instead focuses on [control theory](wiki:Control_theory). The aim is to develop models and algorithms that govern the application of system inputs to drive a system toward a **desired state**, while minimizing undesirable effects such as *delay*, *overshoot*, and *steady-state error* and ensuring an appropriate level of [stability](wiki:Stability_theory).

A *control system* interacts with the physical world in a feedback loop by measuring the environment through *sensors* and influencing it through *actuators*. A common example is a car's cruise-control system: given a desired cruising speed, the controller adjusts inputs such as engine throttle and braking so that the measured speed remains close to the desired speed. A humanoid robot may use inertial sensors, joint encoders, force sensors, cameras, and other instruments to estimate its physical state. The controller compares this estimated state with the desired motion and calculates corrective commands. 

Let

- \(x(t)\) denote the desired motion;
- \(y(t)\) denote the measured motion;
- \(e(t)=x(t)-y(t)\) denote the tracking error; and
- \(u(t)\) denote the motor command.

The controller uses the error and other estimated quantities to calculate \(u(t)\). The motor command changes the robot's physical motion, producing new sensor measurements.

Feedback allows the robot to correct deviations caused by:

- uneven ground;
- modelling errors;
- inaccurate foot placement;
- external pushes;
- actuator variation;
- sensor uncertainty; and
- unexpected changes in momentum.

Without feedback, even a small error could grow until the robot loses its balance.

The design of controllers for the physical world requires models of the dynamics of physical quantities. The theory of dynamical control systems is a well-developed discipline with a rich set of mathematical tools for design and analysis, and a sound understanding of these principles is valuable to CPS engineers. Traditional [control theory](wiki:Control_theory) focuses primarily on *continuous-time* systems. In a CPS, however, a controller may consist of discrete software components operating concurrently and in multiple modes while interacting with a continuously evolving physical environment. Systems that combine *discrete* and *continuous* dynamics are called **hybrid systems**. The principles used to design and analyse controllers for such systems will be studied later in this course.

## Real-Time Computation

[Real-time computing](wiki:Real-time_computing) refers to hardware and software systems that are subject to timing constraints: they must produce responses within specified time limits, often called **deadlines**. For a CPS with real-time requirements, the design must account for the time required by its subcomponents to perform computations, communicate results, and actuate the physical system. Consequently, the design and implementation of real-time CPSs require an understanding of timing delays, their effects on correctness and system performance, timing-dependent coordination protocols, and resource-allocation strategies that ensure predictable execution.

## Safety-Critical Applications

Cyber-physical systems interact directly with people, equipment, infrastructure, or the environment. A failure may therefore cause physical harm rather than merely produce incorrect information. Applications in which *safety* takes priority over other design objectives, such as performance and development cost, are called *safety-critical*. Computing devices that control aircraft, automobiles, and medical devices are examples of CPS components used in safety-critical applications. In this context, establishing at design time that the system operates correctly is of paramount importance and may be mandatory under government regulations and certification requirements.

A traditional approach to system development is to design and implement a system and then conduct extensive testing and validation to detect errors. A more principled approach begins by writing mathematically precise requirements for the desired system, developing models of the system components and their operating environment, and using analysis tools to determine whether the system model satisfies those requirements. This methodology can detect design errors at earlier stages and help achieve greater reliability. Approaches based on [formal models](wiki:Formal_methods) and verification are particularly valuable in safety-critical applications and are increasingly being adopted in industry.


## Connecting the Five Features

The five characteristics are strongly related rather than independent.

| CPS characteristic | Humanoid-robot example | Possible failure |
|---|---|---|
| Reactive computation | Responding to changes in posture and ground contact | The robot fails to react to a disturbance |
| Concurrency | Coordinating perception, planning, balance, and motor control | Tasks produce inconsistent or conflicting actions |
| Feedback control | Adjusting joint torques using sensor measurements | Errors grow and the robot loses balance |
| Real-time computation | Applying corrections before the posture becomes unrecoverable | A correct correction arrives too late |
| Safety-critical operation | Limiting motion near people and obstacles | A fall or collision causes physical harm |

The humanoid robot is not cyber-physical merely because it contains processors or uses artificial-intelligence software. It is cyber-physical because its computation continuously interacts with its physical dynamics through sensors, actuators, communication, and feedback.

The five features provide a useful framework for examining other CPS applications. When studying a new system, we can ask:

1. To which physical events must the system react?
2. Which computations and physical processes occur concurrently?
3. What feedback loops connect computation to physical behaviour?
4. Which results must be produced within a deadline?
5. What physical consequences may result from failure?

## Exercises

### Exercise 1: Reactive computation

Explain why a program that calculates the robot's complete running trajectory before the race begins would be insufficient by itself.

Identify at least three events that would require the robot to modify its previously planned motion.

### Exercise 2: System decomposition

For the humanoid robot, identify:

- the physical plant;
- at least four sensors;
- the computational components;
- the actuators;
- the control objectives;
- three external disturbances; and
- three safety requirements.

### Exercise 3: Concurrency

List three physical or computational activities that must occur concurrently while the robot is running.

Identify one pair of concurrent activities that must exchange information.

### Exercise 4: Safety and performance

A robot completes a race in record time but cannot stop without colliding with a padded barrier.

Discuss whether its control system has succeeded. Consider:

- performance requirements;
- control objectives;
- stability;
- safety; and
- the definition of successful system operation.

### Exercise 5: Feature identification

Select one of the following systems:

- autonomous vehicle;
- cardiac pacemaker;
- smart electrical grid;
- industrial robot; or
- autonomous drone.

For each of Alur's five CPS characteristics, provide one application-specific example.

### Exercise 7: Short reflection

Explain why a humanoid robot is a cyber-physical system rather than simply a computer-controlled machine.