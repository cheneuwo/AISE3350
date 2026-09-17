# Reliability

**[Reliability](wiki:Reliability_engineering)** is the ability of a system to perform its required function without failure for a specified period and under specified operating conditions.

Reliability should be distinguished from **fault tolerance**. A fault-tolerant system can continue to provide an acceptable level of service despite the failure of one or more components. Fault tolerance, redundancy, fault detection, and recovery mechanisms are among the methods used to improve system reliability.

Probabilistic methods are commonly used to model and quantify reliability. For example, engineers may estimate:

- the probability that a component will fail within a given period;
- the expected time between failures;
- the likelihood that multiple components will fail together; and
- the probability that the complete system will perform successfully.

These analyses allow engineers to compare reliability improvements with their associated costs, complexity, energy consumption, and maintenance requirements.

Different CPSs have different reliability requirements. A failure in a domestic cleaning robot may cause inconvenience, whereas a failure in a pacemaker, aircraft controller, or autonomous-vehicle braking system may have severe physical consequences. Reliability will therefore receive different levels of attention depending on the system and its intended application.

As connectivity among CPSs increases, reliability must also be examined at the **system level**. A subsystem may operate reliably in isolation but still contribute to a larger failure when it depends on delayed, missing, or incorrect information from another subsystem.

```{admonition} Component reliability does not guarantee system reliability
:class: important

System reliability depends not only on the reliability of individual components, but also on their architecture, interactions, dependencies, and possible modes of failure.