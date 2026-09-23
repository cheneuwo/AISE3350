# Communication

While AISE 3350 is focused on control theory, it is worth while to introduct the communication aspect of CPSs and security risks associated with it.

Communication enables the cyber (computational) and physical component of a CPS to exchange information. It is multi-scale:
- Within an individual system, sensors communicate measurements to controllers, and controllers send commands to actuators, and
- Between systems, communication support coordination, shared information, and access to remote services.

Perhaps a timely example (as of this writing) is the coordination of nearly 3000 drones:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/tRdMuFvHrzY?si=JZtTIylvb7ZCDzZo"
    title="NYC Twin Tower Drone Show for 9/11 25th Anniversary Tribute"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

Together with computation and control, communication forms the **3C foundation** (Computation, Communication, and Control) introduced earlier in the course. Its importance lies not simply in connecting devices, but in enabling information to inform decisions and physical actions.

:::{note}
Discuss:
- What sensors and actuators may be integrated into a single drone?
- What communication (coordination) must take place *within* a single drone?
- What communication (coordination) must take place *among* a swarm of drones?
::::

## Communication Within and Between CPSs

Communication occurs at different level/scales. Treating modern  vehicle as a CPS, embedded controllers exchange information with sensors and actuators through in-vehicle network. For example, when a [hybrid vehicle](wiki:Hybrid_vehicle) or [EV](Electric_vehicle) on cruise control is travelling downhill, regenerative braking will be activated to maintain the cruising speed and the battery will be charged accordingly. Converse, when a hybrid vehicle on cruise control is convelling uphill, the [engine](wiki:Internal_combustion_engine) may be engaged. Such exchanges of information typically occur through wired connections, and without involving the Internet.

:::{important}
A CPS can be considered as a collection of embedded systems, each internnected *vertically*, i.e. top-down integration of embedded systems.
:::

Beyond the vehicle, wireless communication enable information exchange with nearby vehicle, roadside infrastructure, and remote services. These connections can extend a system's awareness beyond its own sensors. Information from other vehicles along a route, for example, could provide a harzard or local traffic that is not yet visible to the driver or onboard sensors.

:::{important}
CPSs can also communicate *horizontally* with each other to form a CPS of a larger scale.
:::