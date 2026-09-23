# Communication

While AISE 3350 focuses on control theory, it is worthwhile to introduce the communication aspect of CPSs and the security risks associated with it.

Communication enables the cyber (computational) and physical components of a CPS to exchange information. It occurs at multiple scales:

- Within an individual system, sensors communicate measurements to controllers, and controllers send commands to actuators.
- Between systems, communication supports coordination, information sharing, and access to remote services.

Perhaps a timely example, as of this writing, is the coordination of nearly 3,000 drones:

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
- What communication and coordination must take place **within** a single drone?
- What communication and coordination must take place **among** drones in a swarm?
:::

## Communication Within and Between CPSs

Communication occurs at different levels and scales. When we consider a modern vehicle as a CPS, its embedded controllers exchange information with sensors and actuators through an in-vehicle network. For example, when a [hybrid vehicle](wiki:Hybrid_vehicle) or [electric vehicle (EV)](wiki:Electric_vehicle) operating under cruise control travels downhill, regenerative braking will be activated to maintain the cruising speed, charging the battery in the process. Conversely, when a hybrid vehicle operating under cruise control travels uphill, the [engine](wiki:Internal_combustion_engine) may be engaged. Such exchanges of information typically occur through wired connections without involving the Internet.

:::{important}
A CPS can be considered a collection of embedded systems interconnected **vertically**, that is, through the top-down integration of embedded systems.
:::

Beyond the vehicle, wireless communication enables information exchange with nearby vehicles, roadside infrastructure, and remote services. These connections can extend a system's awareness beyond its own sensors. Information from other vehicles along a route, for example, could provide details about a hazard or local traffic conditions that are not yet visible to the driver or onboard sensors.

:::{important}
CPSs can also communicate **horizontally** with each other to form a larger-scale CPS.
:::