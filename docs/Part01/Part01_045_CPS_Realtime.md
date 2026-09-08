# Real-Time Systems

A **[Real-Time Systems](wiki:Real-time_computing)** is one that must respond to external events within specified timing constraints. Its correctness depends not only on the logical value of its output, but also on **when that output is produced**.

Many, but not all, real-time systems are embedded systems. For example, an automated trading agent would not normally be considered an embedded system. However, it may have strict timing constraints if its useful operation depends on responding to rapidly changing market conditions within specified deadlines.

Traditionally, research on real-time systems has focused on topics such as:

- scheduling real-time tasks;
- periodic and aperiodic task-arrival patterns;
- allocating tasks among multiple computational resources;
- managing tasks with different priorities;
- real-time communication; and
- analysing worst-case execution times.

Worst-case execution time is particularly important because average performance does not guarantee that a critical deadline will always be met.

```{admonition} Real time does not simply mean fast
:class: important

A system may perform computations very quickly without being a real-time system. A real-time system must provide a predictable response within a specified deadline.