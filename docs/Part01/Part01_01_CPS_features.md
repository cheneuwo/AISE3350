# Key Features of Cyber-Physical Systems

Cyber-physical systems is ubiquitous in modern society, exemplary includes autonomous vehicles, industrial robots, smart buildings and cities, and large-scale electrical networks. Although these systems operate in different physical environments, they share several important characteristics. Alur identifies five distinguishing characteristics of cyber-physical systems [@Alur2015]:

1. **Reactive computation**
2. **Concurrency**
3. **Feedback control of the physical world**
4. **Real-time computation**
5. **Safety-critical applications**

A timely example (as of 2026-08-31) that illustrates all five characteristics is a **humanoid robot**.

## Humanoid Robots as Cyber-Physical Systems

Humanoid robots has advanced in recent years, [capable of performing household and industrial tasks such as folding laundry and welding](https://www.bbc.com/news/articles/c62m4zn1q6mo). The following BBC video shows humanoid robots participating in running competitions:

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

At first glance, the most impressive feature of the robot is its speed. From a cyber-physical systems perspective, however, how to maintain bipedalism and stability, e.g. without tipping over, is a harder task to achieve. Towards the end of the race, you will notice that the more difficult task for the humanoid robot to achieve is how to stop gracefully: **hint** many humanoid robots simply fall or run into a wall once the race is completed. [Bipedalism](wiki:Bipedalism) robotics is inherently difficult due to control design challenges includeing, but not limited to, the following [@LCP+2021,MMA+2022]:

- Bipedal robots have unstable structures due to the passive joints located at the unilateral contact between the foot and the ground,
- One-sided contact of the foot with the ground and a complex configuration of the gait cycle bring about the highly non-linear trajectory of the bipedal robot,
- Bipedal robots have multiple degrees of freedom. Most researchers uses simplified models to reach a trade-off between simplicity and the dexterity,
- Bipedal robots are most often designed to interact with unknown environment and are expected to achieve a high level of autonomy, and
- Simulation is required as a part of many control strategies for bipedal walking.

A controller designed primarily to maximize forward speed may not automatically produce a safe or stable stop.

```{admonition} Speed is not the complete objective
:class: important

A successful humanoid robot must do more than reach a high speed. It must maintain dynamic balance, reject disturbances, coordinate many actuators, and transition safely between standing, accelerating, running, decelerating, and stopping.
```

The humanoid robot provides a particularly useful example because the interaction between cyber and physical components is easy to observe.

## Reactive Computation

In the classical model of computation, a computing device produces an output based on the given input. For example, a [sorting algorithm](wiki:Sorting_algorithm) takes, as the input, a list of numbers and returs, as the output, a list of the same set of number but in a sorted manner. Based on the [algorithm](wiki:algorithm) used, the manner of how computating was performed and its complexity are generally well-understood. Mathematical expressions and algorithms are often abstracted as functions and procedures, allowing one to build an increasingly complex computational methods by decomposing simpler functions. The notion of correctness of such a program is often captured mathematically as a *function* from input values to output values.

A *reactive* system, in contrast, interacts with its environment in an **ongoing manner** via inputs and outputs [@Alur2015]. A typical example of reactive computation is the cruise controller of a car. Such a system receives high-level input commands such as turning on or off the cruise controller and for changing the desired crusing speed. The control program needs to respond to such inputs by changing its output, which corresponds to the force that is applied to the engine throttle. The behaviour of such a system is natually described by a *sequence* of observed inputs and outputs, and the notion of correcness specifies which input/out sequences corresponds to acceptable behaviour.

## Concurrency

In a traditional *sequential* model of computation, the computation consists of a sequence of sequence of instructions executed one at a time. A humanoid robot does not perform only one task at a time. Many physical and computational processes occur simultaneously. This simultaneous activity is called **concurrency**, where multiples threads of computation (i.e. components or processes), are executed concurrently, communicating with one another with information to achieve the desired outcome of the computation. Using the humanoid robot as an example, visual perception may update more slowly than joint-position measurements. A high-level motion planner may update more slowly than the low-level balance controller. Nevertheless, their results must remain sufficiently consistent for the complete robot to operate safely.

```{admonition} Concurrency
:class: important

Understanding models and design principles for *distributed* and *concurrent* computation is critical for CPSs. Categorically, these models can be divided into:

1. *synchronous* models, where components are executed in lock-steps, and the computation progresses in a logical sequence of synchronized rounds; and
2. *asynchronous* models, where components are executed at independent speeds, exchanging information by sending and receiving messages.
```

The detail for concurrency is not a focus for this course.

## Feedback Control of the Physical World

Feedback control provides the central connection between computation and physical behaviour.

A humanoid robot may use inertial sensors, joint encoders, force sensors, cameras, and other instruments to estimate its physical state. The controller compares the estimated state with the desired motion and calculates corrective commands. Electric motors then apply torque at the joints.

A simplified feedback loop is

\[
\text{Desired motion}
\longrightarrow
\text{Controller}
\longrightarrow
\text{Motors}
\longrightarrow
\text{Robot dynamics}
\longrightarrow
\text{Sensors}
\longrightarrow
\text{Controller}.
\]

Let

- \(r(t)\) denote the desired motion;
- \(y(t)\) denote the measured motion;
- \(e(t)=r(t)-y(t)\) denote the tracking error; and
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

Stopping provides a particularly useful illustration. When the desired speed changes from a positive value to zero, the robot cannot simply switch off its motors. It must generate a coordinated sequence of actions that reduces forward momentum while maintaining balance.

The stopping manoeuvre may require the robot to:

1. modify its desired foot-placement locations;
2. reduce its forward acceleration;
3. apply braking torques at several joints;
4. control the motion of its torso and arms;
5. maintain sufficient ground contact; and
6. transition from a running gait to a stable standing posture.

The success of the manoeuvre depends on the complete feedback loop rather than on a single motor command.

## Real-Time Computation

A computation is **real-time** when the time at which its result is produced forms part of its correctness.

For a humanoid robot, a balance correction must be calculated and applied before the robot moves too far from a recoverable state. A motor command that would have been correct several milliseconds earlier may no longer be appropriate for the robot's current posture.

The total response delay may include

\[
T_{\mathrm{loop}}
=
T_{\mathrm{sensing}}
+
T_{\mathrm{communication}}
+
T_{\mathrm{computation}}
+
T_{\mathrm{actuation}}.
\]

Each term contributes to the time between a physical event and the resulting physical response.

Real-time computation does not simply mean that a computer is fast. A processor can perform millions of operations per second and still fail to meet the deadline imposed by the physical process.

The relevant question is therefore not

> Is the computer fast?

but rather

> Does the complete sensing–computation–actuation loop respond before the physical deadline?

The deadline is determined by the dynamics of the physical system. A building-temperature controller may tolerate delays of several seconds. A balancing robot requires responses on a much shorter timescale.

```{admonition} Temporal correctness
:class: important

For a real-time CPS, correctness has two components:

1. the computed result must be logically correct; and
2. the result must be produced and applied at the correct time.
```

Timing behaviour may be affected by:

- sensor sampling rates;
- processor scheduling;
- communication delays;
- variation in execution time;
- contention for shared resources;
- packet loss and retransmission; and
- actuator response time.

Therefore, the timing of the complete system must be considered rather than only the execution time of one algorithm.

## Safety-Critical Applications

Many cyber-physical systems interact directly with people, equipment, infrastructure, or the environment. A failure may therefore cause physical harm rather than only producing incorrect information.

A humanoid robot may:

- fall onto a nearby person;
- collide with an obstacle;
- apply excessive joint torque;
- lose control while carrying an object;
- continue moving after receiving a stop command;
- damage nearby equipment; or
- behave unpredictably after a sensor or communication failure.

Safety must therefore be considered at the level of the complete system. It is not sufficient to verify that each software function produces the expected numerical result.

A safe humanoid-robot system may require:

- limits on speed, force, and joint torque;
- emergency-stop mechanisms;
- collision detection;
- fault detection and isolation;
- redundant sensing;
- safe operating regions;
- controlled degradation after a failure; and
- a stable stopping strategy.

Not every CPS has the same level of safety criticality. A smart thermostat and a cardiac pacemaker are both cyber-physical systems, but the immediate consequences of failure are very different. Safety requirements must therefore be derived from the application and its physical environment.

```{admonition} Safety and performance are different requirements
:class: warning

A robot may satisfy a performance objective, such as completing a race quickly, while failing a safety objective, such as stopping without a collision.

A successful CPS design must satisfy both types of requirements.
```

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

List five physical or computational activities that must occur concurrently while the robot is running.

Identify one pair of concurrent activities that must exchange information.

### Exercise 4: Feedback-loop delay

Suppose the robot has the following delays:

| Operation | Delay |
|---|---:|
| Sensor acquisition | \(2.0\text{ ms}\) |
| State estimation | \(1.5\text{ ms}\) |
| Control calculation | \(0.8\text{ ms}\) |
| Communication | \(0.7\text{ ms}\) |
| Actuator response | \(4.0\text{ ms}\) |

1. Calculate the total feedback-loop delay.
2. If the robot is moving at \(8\text{ m/s}\), how far does it travel during this delay?
3. Explain why this distance alone is not sufficient to determine whether the robot remains stable.

### Exercise 5: Safety and performance

A robot completes a race in record time but cannot stop without colliding with a padded barrier.

Discuss whether its control system has succeeded. Consider:

- performance requirements;
- control objectives;
- stability;
- safety; and
- the definition of successful system operation.

### Exercise 6: Feature identification

Select one of the following systems:

- autonomous vehicle;
- cardiac pacemaker;
- smart electrical grid;
- industrial robot; or
- autonomous drone.

For each of Alur's five CPS characteristics, provide one application-specific example.

### Exercise 7: Short reflection

In no more than three sentences, explain why a humanoid robot is a cyber-physical system rather than simply a computer-controlled machine.