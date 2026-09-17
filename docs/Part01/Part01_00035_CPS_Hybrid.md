# Hybrid Systems

A **[Hybrid Systems](wiki:Hybrid_system)** combines continuous physical dynamics with discrete computational behaviour. Physical quantities -- such as position, velocity, temperature, voltage, and pressure -- typically evolve continuously over time. In contrast, a digital controller operates through discrete computations, events, decisions, and modes.

For example, the velocity of an autonomous vehicle changes continuously, while its controller may switch among discrete operating modes such as *lane keeping*, *lane changing*, *emergency braking*, and *stopped*. Similarly, a pacemaker observes continuously evolving physiological processes but responds through discrete sensing events, timing decisions, and pacing actions.

Hybrid-system models provide a mathematical framework for studying the interaction between these two kinds of behaviour:

**Continuous physical evolution** ↔ **Discrete computational decisions**

This interaction is fundamental to CPS because the physical process influences the controller's decisions, while the controller's decisions alter the subsequent evolution of the physical process.

## Mathematical Models of Systems

A **mathematical model** is used to represent and explain the observed behaviour of a system. A model is not the physical system itself; instead, it is an abstraction that captures the properties considered important for a particular purpose.

When new observations cannot be explained adequately by an existing model, the assumptions underlying the model must be reconsidered. The model may need to be refined, revised, or, in some cases, replaced by a different model.

We often associate physical systems with **continuous models** and computational systems with **discrete models**. This distinction is useful, but it is not absolute. Whether a model is continuous, discrete, or hybrid depends on the behaviour being represented and the questions the model is intended to answer.

### Physical Systems Can Exhibit Discrete Behaviour

[**Quantum mechanics**](https://en.wikipedia.org/wiki/Quantum_mechanics) demonstrates that a physical system need not always be described as purely continuous. Certain physical quantities can take only particular quantized values. For example, a bound electron in an atom can occupy only certain permitted energy levels.

In simplified atomic models, these energy levels are sometimes depicted as discrete electron orbits around the nucleus. Modern quantum mechanics instead describes an electron using a wavefunction and atomic orbitals. Therefore, quantum mechanics contains both continuous mathematical descriptions and discrete measurement outcomes.

Other physical systems also exhibit discrete events, such as:

- contact or separation between mechanical components;
- collisions;
- the opening or closing of a switch; and
- transitions between operating modes.

### Computational Systems Are Physically Continuous

Conversely, a computational system cannot always be viewed as purely discrete. A digital computer is generally implemented using electronic circuits in which physical quantities such as voltage and current vary continuously.

The circuits are designed so that ranges of continuous voltages can be interpreted reliably as discrete logical values, such as **0** and **1**. Thus, a digital computer can be understood at two different levels:

- at the **physical level**, it is a continuous electronic system; and
- at the **logical level**, it is modelled as a discrete computational system.

[**Analog computers**](https://en.wikipedia.org/wiki/Analog_computer) provide another example. They perform computations using continuously varying physical quantities, such as voltage, current, or mechanical position. Computation itself is therefore not necessarily discrete.

```{admonition} Continuous and discrete are properties of models
:class: important

The labels *physical* and *continuous* are not interchangeable. Similarly, the labels *computational* and *discrete* are not interchangeable. Continuous and discrete descriptions are modelling choices made at particular levels of abstraction.