# Level 4: High Driving Automation

At **Level 4**, an automated driving system performs the **entire dynamic driving task** under defined operating conditions, without requiring a human to supervise or take over to mitigate risk.

**When engaged within its operating conditions, the system drives and the occupants ride.**

Unlike Level 3, Level 4 does not depend on a fallback-ready human. If continued driving becomes inappropriate, the system must handle the fallback response rather than rely on a passenger to resume driving.

```{figure} ./../../imgs/autonomous_vehicle_level_4.png
:label: fig-driving-level-4
:alt: Vehicle Autonomy, level 4.
:width: 600px
:align: center
```

## The Human's Role

Occupants are passengers rather than supervising drivers. They do not need to continuously observe the road, operate the controls, or remain ready to take over.

Passengers may still interact with the service, for example by selecting a destination or requesting that the vehicle stop. These interactions are different from performing the driving task.

Some vehicles retain manual controls and permit human driving in a separate operating mode. Others omit these controls entirely. The availability of manual override is therefore a design choice, not a defining requirement of Level 4.

## The System's Role

Within its operational design domain, the system:

- Controls steering, acceleration, and braking.
- Monitors and responds to the driving environment.
- Handles situations requiring a fallback response without relying on human takeover.
- Brings the vehicle to a minimal-risk condition when continued operation is not appropriate.

A **minimal-risk condition** generally involves bringing the vehicle to a stop in a manner intended to reduce risk. This does not imply that the system can eliminate every hazard or continue a journey despite any failure.

## Defined Operating Conditions

Level 4 operation is restricted to an **operational design domain (ODD)**. Its limits may concern geographical area, road type, speed, weather, or other environmental conditions.

**Geofencing** establishes a geographical operating boundary, but geography is only one part of an ODD. A vehicle might be inside its permitted service area while weather conditions are outside its operating limits.

These boundaries reflect the conditions for which the system is designed and validated. They are not simply restrictions that disappear when legislation or infrastructure changes.

## Examples and Case Studies

### Waymo: Driverless Ride-Hailing

Waymo's rider-only service, including operations in Phoenix, Arizona, provides an example of Level 4 driving automation. The Waymo Driver performs the driving task without an onboard human driver in its supported operating conditions.

Its ability to provide driverless trips within a service area does not mean that it can operate on every road or in every environment.

### Tesla Cybercab: Deployment and Certification

Tesla Cybercab provides a related case study of a vehicle designed without conventional human driving controls.

In September 2026, NHTSA announced an investigation into Tesla's self-certification of Cybercab following its commercial driverless deployment in Austin, Texas. The investigation concerns compliance with federal vehicle safety standards.

The absence of a steering wheel and pedals does not, by itself, establish an SAE automation level. Classification requires examining the system's driving capabilities, operating conditions, and responsibility for fallback. Regulatory compliance is a separate question.

## Interpreting the Illustration

An illustration without a driver-attention cone, steering wheel, or pedals can emphasize that the occupant is not expected to perform the driving task.

However, these are visual cues rather than classification criteria. Level 4 vehicles may retain conventional controls, and the automated system still needs to perceive and respond to its surroundings.

## Key Takeaway

**The system performs both the driving task and the fallback response within defined operating conditions; human driving is not needed to mitigate risk.**

The distinction from Level 3 is the absence of reliance on human takeover. The distinction from Level 5 is the restriction to a defined operating domain.

## Discussion

A driverless taxi encounters conditions outside those supported by its automated driving system.

- Why is asking a passenger to take over insufficient for Level 4 operation?
- What could an appropriate fallback response involve?
- Why does having no steering wheel not automatically make the vehicle Level 5?