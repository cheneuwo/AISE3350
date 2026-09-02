# CPS Example: Self-Balancing Personal Transporter

At an airport, you may have seen security officers or other personnel travelling on a **self-balancing personal transporter**. Unlike an ordinary vehicle, this device must continuously maintain its balance while responding to the rider's commands.

A self-balancing personal transporter is a single-person electric vehicle comprising a one- or two-wheeled platform on which the rider stands. Unlike other vehicles, it uses a self-balancing gyroscopic system for steering, changing directions depending on which way the rider leans. [This new and increasingly popular means of urban mobility operates using digital sensors and one or two electric motors](https://www.planete-energies.com/en/media/article/how-do-segways-hoverboards-and-other-self-balancing-personal-transporters-work).

The following video demonstrates the Ninebot by Segway miniPRO:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/nu4V_XDQKrk?si=MRhvS3nfkWLsNqms"
    title="The Ninebot by Segway miniPRO"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

## Why Is It a Cyber-Physical System?

A self-balancing transporter can be approximated as an [inverted pendulum](wiki:Inverted_pendulum) mounted on two wheels. An inverted pendulum is inherently unstable: without continuous corrective action, it will fall.

Sensors measure the motion and orientation of the transporter. An embedded computer estimates its physical state and calculates corrective commands. Electric motors apply torque to the wheels, changing the physical motion of the transporter. The resulting motion is measured again, completing the feedback loop.

Because this process connects real-time computation directly to physical
motion, the transporter is a cyber-physical system.

## Principal Components

A self-balancing transporter may include the following components:

- **[Electric motors](wiki:Electric_motor):** Act as the system's actuators. They apply torque to the wheels for both propulsion and balance control.

- **[Wheel encoders](wiki:Rotary_encoder):** Measure the angular position and rotational speed of the wheels.

- **[Accelerometers](wiki:Accelerometer):** Measure acceleration and  provide information related to the direction of gravity.

- **[Gyroscopes](wiki:Vibrating_structure_gyroscope):** Measure angular velocity, indicating how quickly the transporter is rotating or tilting.

- **[Inertial measurement unit (IMU)](wiki:Inertial_measurement_unit):** Combines measurements from accelerometers and gyroscopes. The controller uses these measurements to estimate the transporter's orientation and motion.

- **Embedded control board:** Processes sensor measurements, estimates the state of the transporter, and calculates motor commands.

```{admonition} Components of CPSs
:class: important

When studying the components of a CPS, ask the following questions
- What is the physics (physical process),
- What are the sensors required to measure the properties of this physical process, and
- What actuator(s) is needed to alter the state of this physical process.
```