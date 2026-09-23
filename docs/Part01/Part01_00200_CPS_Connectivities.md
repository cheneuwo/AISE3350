# Connectivity, Autonomy, and Security

The preceding examples illustrate how communication connects vehicles to other vehicles, road users, infrastructure, devices, and remote services. These connections provide access to information beyond what an individual vehicle can obtain from its onboard sensors. Together with advances in computing resources and algorithms, this information can support more informed decisions and increasingly capable automated functions.

However, connectivity also introduces potential security risks. The communication pathways that provide useful information and services may also expose a system to unauthorized access, data manipulation, or disruption.

## Connectivity: Extending Awareness

**Connectivity** concerns the exchange of information within a system and between systems. For a vehicle, this includes communication among onboard sensors and controllers, as well as connections to other vehicles, roadside infrastructure, and cloud services.

Information exchange can extend a vehicle's awareness beyond its onboard sensors. For example, a vehicle might receive a warning about sudden braking farther along a road, even when the braking vehicle is hidden from view.

Connectivity is useful even when a human performs all driving tasks. A human-driven vehicle can use connected services for navigation, traffic warnings, remote diagnostics, and software updates without being autonomous.

## Autonomy: From Information to Action

**Automation** concerns which tasks a system performs without direct human control. Increasing autonomy involves giving the system greater responsibility for sensing its environment, making decisions, and taking appropriate actions within its intended operating conditions.

Advances in computing resources and algorithms allow vehicles to process sensor measurements, estimate their surroundings, predict possible events, and select actions. Connectivity can complement these capabilities by supplying additional information or access to remote services.

However, connectivity and autonomy are distinct. Some automated functions rely primarily on onboard sensing and computation, while others also use information from connected systems. For example, adaptive cruise control can regulate a vehicle's speed using onboard measurements without requiring information from a cloud service.

:::{important}
Connectivity can **support and enhance autonomy**, but connectivity alone does not make a system autonomous.

Likewise, more information does not automatically produce better decisions: the information must be relevant, sufficiently accurate, and timely.
:::

## Security: Protecting Information and Physical Behaviour

Communication introduces potential security concerns both **within a CPS**, such as an onboard vehicle network, and **between CPSs and external systems**, such as other vehicles or cloud services.

Consider vehicle-to-cloud communication. A vehicle collects selected data from its onboard sensors and networks and sends these data to a cloud service provider. The provider processes the data to support services such as fleet management, traffic warnings, and remote diagnostics. Information and software updates may also flow back to the vehicle.

These exchanges raise several security questions:

- **Confidentiality:** Could an unauthorized party obtain sensitive information, such as vehicle location or travel history?
- **Integrity and authenticity:** Could information be altered, or could a message come from an attacker impersonating a trusted source?
- **Availability:** Could communication or a connected service be disrupted when it is needed?
- **Access control:** Could an unauthorized party change software, settings, or system behaviour?

In a CPS, the consequences of a security failure may extend beyond data loss. If compromised information influences a controller's decisions, it may also affect the system's physical behaviour. For example, a false traffic warning could influence route selection, while a compromised control message could have more direct consequences for vehicle operation.

Connectivity therefore creates both opportunities and responsibilities: it can improve awareness and support automation, but the resulting information exchanges must be protected.

This leads to the next question: **How can we obtain the benefits of connected CPSs while maintaining secure and safe operation?**