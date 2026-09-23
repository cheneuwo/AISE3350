# Summary: Levels of Driving Automation

The six levels distinguish how the driving task is divided between the human and the system. The central questions are **who drives, who supervises, who handles fallback, and under what conditions the system operates**.

```{figure} ./../../imgs/autonomous_vehicle_summary.png
:label: fig-sae-automation-summary
:alt: SAE comparison of driving automation Levels 0 to 5, showing human responsibilities, system capabilities, and example features.
:width: 100%
:align: center

SAE levels of driving automation. Source: SAE International, 2021. Reproduced unchanged with attribution. 
```

## Three Important Boundaries

- **Level 1 → Level 2:** Assistance expands from steering **or** speed control to steering **and** speed control. Continuous human supervision remains necessary.

- **Level 2 → Level 3:** The system assumes the entire dynamic driving task, including monitoring and responding to the environment. The human no longer continuously supervises, but must remain available to resume driving when required.

- **Level 3 → Level 4:** The system also assumes fallback responsibility rather than depending on human takeover. Level 5 extends this capability beyond a particular operating domain to all on-road conditions in which humans can drive.

:::{important}
Two qualifications help interpret the simplified wording in this 2021 figure:

- At **Level 3**, human driving may be required following an alert **or an evident vehicle malfunction**.
- At **Level 5**, “all conditions” means conditions in which humans can drive—not physically impassable or inherently unsafe conditions.
:::

The levels describe **functional responsibilities**, not a safety ranking. More sensors, greater computing power, hands-free operation, or the absence of a steering wheel do not independently determine the automation level.