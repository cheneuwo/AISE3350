# Vehicle-to-Everything (V2X)

[Vehicle-to-everything (V2X)](wiki:Vehicle-to-everything) is an umbrella term that describes wireless communication between a vehicle and any entity that **may affect**, or **may be affected by**, the vehicle.

V2X standards have been established and continue to evolve. However, standardization does not necessarily imply widespread adoption: deployment varies by region and application.

Two major technologies supporting V2X communication are:

- [Dedicated short-range communications (DSRC)](wiki:Dedicated_short-range_communications): A technology for the **direct** wireless exchange of V2X and other [intelligent transportation systems (ITS)](wiki:Intelligent_transportation_system) data between vehicles, other road users, and roadside infrastructure.
  - DSRC is based on [IEEE 802.11p](wiki:IEEE_802.11p) and was developed for operation in the **5.9 GHz band**. Spectrum allocations and permitted technologies vary by jurisdiction.

- [Cellular V2X (C-V2X)](wiki:Cellular_V2X): A family of standardized technologies supporting V2X communication, initially based on [Long-Term Evolution (LTE)](wiki:LTE_(telecommunication)) and subsequently extended to include 5G New Radio (NR).
  - C-V2X supports **direct communication**, such as vehicle-to-vehicle and vehicle-to-infrastructure communication, without requiring a cellular network connection.
  - It also supports **wide-area communication** through a cellular network, such as vehicle-to-network communication.

The following figure and table illustrate different vehicle communication relationships.

```{image} https://thumb.wikimedia.org/wikipedia/commons/thumb/7/7a/Types_V2X_.png/1920px-Types_V2X_.png
:alt: Types of vehicle-to-everything communication, showing connections between vehicles and other entities.
:width: 500px
:align: center
```

| Relationship | Participants | Examples |
| :--- | :--- | :--- |
| V2V: Vehicle-to-vehicle | A vehicle and nearby vehicles | Exchange of position, speed, and braking information |
| V2P: Vehicle-to-pedestrian | A vehicle and equipped pedestrians or other vulnerable road users | Warnings involving pedestrians, cyclists, and wheelchair users |
| V2N: Vehicle-to-network | A vehicle and a wider communication network | Telematics and fleet management |
| V2I: Vehicle-to-infrastructure | A vehicle and roadside infrastructure | Traffic signal information and road hazard warnings |
| V2D: Vehicle-to-device | A vehicle and personal devices | Bluetooth or Wi-Fi connectivity, including connections used by wireless Android Auto and Apple CarPlay |
| V2G: Vehicle-to-grid | A vehicle and the electricity grid | Communication and bidirectional energy exchange to support grid operation and balance electricity supply and demand |
| V2C: Vehicle-to-cloud | A vehicle and cloud services | Over-the-air (OTA) updates and remote diagnostics |

:::{note}
These labels describe relationships rather than individual communication protocols, and the categories can overlap. For example, vehicle-to-cloud communication typically uses a vehicle-to-network connection.

In this broader classification, not every connection is necessarily wireless. Vehicle-to-grid systems, for example, commonly use a wired charging connection and involve both information exchange and electrical power transfer.
:::
