# SAE Levels of Driving Automation

Road vehicles provide a familiar example of cyber-physical systems with varying degrees of automation. Some features assist a human driver with individual tasks, while others perform the complete driving task under specified conditions.

To distinguish these capabilities, **SAE International**, formerly the Society of Automotive Engineers, established a taxonomy in [**SAE J3016: Taxonomy and Definitions for Terms Related to Driving Automation Systems for On-Road Motor Vehicles**](https://www.sae.org/standards/j3016_202609-taxonomy-definitions-terms-related-driving-automation-systems-road-motor-vehicles).

SAE uses the term **driving automation**, rather than simply *autonomy*, to describe how driving responsibilities are divided between the human and the system.

## The Six Levels

The taxonomy defines six levels, numbered from **0 to 5**:

- **Level 0: No Driving Automation**
- **Level 1: Driver Assistance**
- **Level 2: Partial Driving Automation**
- **Level 3: Conditional Driving Automation**
- **Level 4: High Driving Automation**
- **Level 5: Full Driving Automation**

The levels distinguish what the system does, what the human must do, and the conditions under which the feature can operate. They do not simply reflect the number of sensors, the available computing power, or the extent of connectivity.

## How Are These Levels Distinguished?

In **the revised standard**[@SAE_vehicle], published in 2026, SAE distinguishes the levels by the **responsibilities assigned to the human and the system**, rather than by the sophistication of the technology.

Its framework considers three actors: the **human user**, the **driving automation system**, and **other vehicle systems and components**. Their intended roles determine who performs the driving task and who responds when normal operation cannot continue.

Four questions help explain the distinctions:

1. **What does the system control?** Does it provide sustained control of steering, speed, or both?

2. **Who monitors and responds to the driving environment?** Must the human continuously supervise, or does the system undertake this responsibility?

3. **When is human intervention required?** Must the human intervene as needed, resume driving following an alert or an evident malfunction, or is human driving unnecessary for risk mitigation?

4. **Where and under what conditions can it operate?** Is automated driving restricted to defined conditions, or can it operate under all on-road conditions in which humans can drive?

These responsibilities concern the **dynamic driving task (DDT)** and **DDT fallback**. The DDT includes controlling vehicle motion and responding to the driving environment. Fallback concerns the response when continued normal operation is no longer possible. The **operational design domain (ODD)** describes the conditions for which a feature is designed.

:::{important}
The classification concerns **intended responsibilities**, not whether a person actually fulfils them. A driver who stops supervising a driver-assistance feature does not thereby turn it into a higher-level automated system.
:::

The taxonomy addresses **sustained driving automation**. Warnings and brief safety interventions do not, by themselves, establish a higher automation level.

Finally, SAE J3016 is a classification framework—not a safety standard or certification that a system is safe.