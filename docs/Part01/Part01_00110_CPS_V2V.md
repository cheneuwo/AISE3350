# Vehicle-to-Vehicle (V2V)

[Vehicle-to-vehicle (V2V)](https://www.nhtsa.gov/sites/nhtsa.gov/files/documents/v2v_fact_sheet_101414_v2a.pdf) communication supports crash avoidance by enabling nearby vehicles to exchange information and potentially warn drivers about dangerous situations that could lead to a collision. For example, V2V could warn a driver that a vehicle ahead is braking and that they need to slow down. It could also alert a driver that it is unsafe to proceed through an intersection because another vehicle, not yet visible to the driver, is approaching quickly.

## Dedicated Short-Range Communications (DSRC)

[Dedicated short-range communications (DSRC)](wiki:Dedicated_short-range_communications) support **two-way, wireless communication**, enabling the rapid exchange of safety-related messages. The 2014 NHTSA fact sheet describes an approximate communication range of **300 metres**, depending on the surrounding environment. This is an indicative range rather than a guaranteed limit.

Historically, the United States allocated **75 MHz of spectrum in the 5.9 GHz band** to intelligent transportation systems, including DSRC. This allocation has since changed: the upper **30 MHz (5.895–5.925 GHz)** is retained for ITS, with a transition from DSRC to C-V2X.

:::{note}
V2V describes communication **between vehicles**, whereas DSRC and C-V2X describe technologies that can enable this communication. V2V is therefore not limited to DSRC.
:::

## Safety Applications Enabled by V2V

V2V can extend a driver's awareness beyond their direct line of sight and supplement information from onboard sensors. Potential safety applications include:

- **Intersection Movement Assist (IMA):** Warns the driver when entering an intersection could lead to a collision with one or more vehicles.

- **Left Turn Assist (LTA):** Warns the driver when there is a high risk of colliding with an oncoming vehicle while making a left turn. This is especially important when the driver's line of sight is blocked by a vehicle turning left from the opposite direction.

- **Emergency Electronic Brake Light (EEBL):** Warns the driver when a V2V-equipped vehicle travelling in the same direction brakes sharply, even if that vehicle is outside the driver's line of sight. This can provide advance warning of an abrupt stop in traffic ahead, including situations in which other vehicles or poor visibility obscure the driver's view.

- **Forward Collision Warning (FCW):** Warns the driver of an impending rear-end collision with a vehicle ahead in the same lane and travelling in the same direction.

- **Blind Spot Warning (BSW) and Lane Change Warning (LCW):** BSW notifies the driver that a vehicle in an adjacent lane is occupying their blind spot. LCW warns the driver during an intended lane change that another vehicle is present in, or approaching, the relevant blind-spot area.

- **Do-Not-Pass Warning (DNPW):** Warns the driver when it is unsafe to pass a slower-moving vehicle because of approaching traffic in the opposite direction.

:::{note}
These applications are not all exclusive to V2V. For example, forward collision and blind spot warnings can also be implemented using onboard sensors. V2V can supplement these systems by providing information directly from other equipped vehicles, including vehicles that are not directly visible.
:::