# Foundations of Cyber-Physical Systems

:::{important} Original Definition
:class: simple

Cyber-physical systems, or **CPSs**, are physical, biological, and engineered systems whose operations are integrated, monitored, and/or controlled by a computational core. Components of a CPS are networked at every scale. The computational core is an embedded system, usually demands real-time response, and is most often distributed. The behaviour of a cyber-physical system is a fully-integrated hybridization of computational (logical) and physical actions.

The above definition is paraphrased by [one of the earliest presentations given by Helen Gill of the US National Science Foundation in 2008](https://labs.ece.uw.edu/nsl/aar-cps/Gill_HCSS_Transportation_Cyber-Physical_Systems_2008.pdf).
:::

A cyber-physical system, or **CPS**, is an orchestration of computing and physical systems, coordinated via a communication mechanism. Embedded computers monitor and control physical processes, usually with feedback loops, where physical processes affect computations and *vice versa* [@Lee2015].

Applications of CPS includes autonomous vehicles, industrial robots, medical devices, smart building/city, power grids, and transportation networks. While theye systems operate in different environments, they share a common structure: computation cores communicating with one another and interacting with the physical world via sensors and actuators in a feedback loop. More concretely:
- Computation core receives information about a physical process (via sensors),
- Makes a decision,
- Produces an action (via actuators) that affect the subsequent behaviour of that physical process.

This continuous interaction between information and physical behaviour is the central idea of CPSs.

## Historical Context

The term *cyber-physical systems* emerged around 2006 and is generally credited to **Helen Gill**, who was a program director at the United States National Science Foundation (NSF) [@Lee2015]. Gill's contribution was not the invention of feedback control, embedded computing, or networked systems. These technologies and research areas had existed for decades.

Instead, the CPS terminology gave a name to a growing engineering problem: computation and physical dynamics could no longer be designed as independent components and connected only near the end of the development process. They had to be understood and engineered as parts of one integrated system.

The [NSF subsequently described CPS](https://www.nsf.gov/funding/opportunities/cps-cyberphysical-systems/503286/nsf08-611/solicitation) as involving the tight conjoining and coordination of computational and physical resources. This framing helped establish CPS as a multidisciplinary area connecting computer science, control engineering, communications, electronics, mechanical systems, and application-specific physical sciences.

The foundations of CPS are considerably older than the terminology. Feedback control, for example, predates digital computers. Early control systems used mechanical, pneumatic, hydraulic, and analog electronic components to measure and regulate physical processes. Embedded and real-time computing later made it possible to implement increasingly sophisticated control and decision-making algorithms in software.

The CPS perspective brings these established ideas together and places particular emphasis on their interaction.

```{admonition} Historical perspective
:class: note

The underlying engineering ideas are older than the term *cyber-physical systems*. Helen Gill's contribution was to make the integration of computation and physical dynamics a distinct research and engineering problem.