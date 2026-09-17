# Dependability

**[Dependability](wiki:Dependability)** is a holistic concept describing the extent to which a system can be trusted to deliver its required service. It encompasses several related attributes, including availability, reliability, durability, safety, security, integrity, and maintainability.

In the interdisciplinary field of systems engineering, dependability is evaluated by considering these attributes together rather than examining each one in isolation.

| Attribute | Guiding question |
|---|---|
| **Availability** | Is the system ready to provide its service when required? |
| **Reliability** | Can the system continue operating correctly over the required period? |
| **Durability** | Can the system withstand degradation over its intended lifetime? |
| **Safety** | Can the system operate without creating unacceptable physical risks? |
| **Security** | Can the system resist unauthorized access, interference, or attack? |
| **Integrity** | Can the system prevent improper alteration of its data and operation? |
| **Maintainability** | Can the system be repaired, updated, or restored efficiently? |

These attributes are closely related and may sometimes conflict. For example, a security mechanism may improve protection against unauthorized access but increase computational delay or make emergency maintenance more difficult. Similarly, adding redundant components may improve reliability while increasing cost, energy consumption, and system complexity.

The CPS perspective requires engineers to consider how failures and attacks in the cyber domain can affect the physical domain, and how physical failures can affect computation and communication. Dependability must therefore be evaluated across the complete cyber-physical system.

```{admonition} Reliability and dependability are not synonymous
:class: important

Reliability is one attribute of dependability. A system may operate reliably under normal conditions but still be considered undependable if it is unsafe, insecure, unavailable when needed, or difficult to repair.