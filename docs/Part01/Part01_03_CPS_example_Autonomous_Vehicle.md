# CPS Example: Autonomous Vehicle

An [autonomous vehicle](wiki:Self-driving_car) is a car that is capable of operating with **reduced** or **no human input**. Autonomous vehicles rely on sensing, computation, communication, and physical actuation to perceive their environment and make driving decisions. Different levels of autonomy will be discussed later in the lecture materials.

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/HS1wV9NMLr8?si=3-GvXxwGKglwEJw2"
    title="How AI Helps Autonomous Vehicles See Outside the Box"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

## Why Is It a Cyber-Physical System?

An autonomous vehicle is a cyber-physical system because it tightly integrates computational decision-making with physical motion in the real world.

The **physical system** includes the vehicle body, wheels, brakes, steering system, engine or electric motors, and the surrounding road environment. The **cyber system** includes onboard computers, perception algorithms, control software, maps, localization systems, and communication modules. Sensors collect information from the physical world, software interprets that information, and actuators physically control the vehicle.

This creates a continuous feedback loop:

1. Sensors observe the environment.
2. Computers estimate the vehicle’s state and detect objects.
3. Planning algorithms decide what the vehicle should do.
4. Controllers send commands to steering, braking, and acceleration systems.
5. The vehicle moves, changing the physical environment and restarting the loop.

## Principal Components
An autonomous vehicle must be aware of its environment. This is achieved using an array of sensors, including but not limited to:

- **Cameras:** Multiple RGB cameras capture images and video, similar to human vision.
- **[LiDAR, or Light Detection and Ranging](wiki:Lidar):** A method for measuring distance by targeting an object or surface with a [laser](wiki:Laser) and measuring the time required for the reflected light to return to the optical receiver.
- **[GPS, or Global Positioning System](wiki:Global_Positioning_System):** Provides [geolocation](wiki:Geopositioning) and timing information.
- **[Radar](wiki:Radar):** Uses [radio waves](wiki:Radio_wave) to determine the distance, direction, and [radial velocity](wiki:Radial_velocity) of nearby objects.
- **[Ultrasound](wiki:Ultrasound):** Used for short-range object detection, such as parking assistance and low-speed maneuvering.

In addition to sensors, autonomous vehicles also require:

- **Perception software:** Detects lanes, vehicles, pedestrians, traffic signs, traffic lights, and other objects.
- **Localization and mapping:** Estimates where the vehicle is relative to roads, lanes, and obstacles.
- **Planning algorithms:** Decide the vehicle’s path and driving behavior.
- **Control systems:** Convert planned motion into steering, braking, and acceleration commands.
- **Actuators:** Physically control the vehicle’s movement.
- **Communication systems:** Allow vehicles to exchange information with infrastructure, cloud services, or other vehicles when needed.

## What Are Some Current Issues?

[Vehicle-to-everything (V2X)](wiki:Vehicle-to-everything)  describes wireless communication between a vehicle and other entities that may affect, or be affected by, the vehicle. In a broader vehicle-connectivity context, related categories
include:

- **[Vehicle-to-device (V2D)](wiki:Vehicle-to-device):** Communication with personal devices, such as smartphones, using technologies such as Bluetooth and Wi-Fi. Examples include wireless Apple CarPlay and Android Auto.

- **[Vehicle-to-grid](wiki:Vehicle-to-grid):** Communication supporting coordination between electric vehicles and the electrical grid, including energy management and bidirectional power transfer.

- **Vehicle-to-network (V2N):** Communication between a vehicle and a wider network, such as a cellular network.

- **Vehicle-to-cloud (V2C):** Communication with cloud-based services, for example, over-the-air (OTA) software updates and remote vehicle diagnostics.

- **[Vehicle-to-infrastructure (V2I)](wiki:Vehicle_infrastructure_integration):** Communication with equipped infrastructure, such as traffic signals, roadside units, and smart parking systems.

- **Vehicle-to-pedestrian (V2P):** Communication with devices used by pedestrians and other vulnerable road users, including cyclists and wheelchair users.

- **Vehicle-to-vehicle (V2V):** Exchange of time-sensitive information with nearby vehicles.

Standards for many of these communication functions already exist, while interoperability, industry adoption, and large-scale deployment continue to develop.

### Network Connectivity

If a fleet of autonomous vehicles relies on a network to communicate with each other or with a central hub, network reliability becomes critical. Poor connectivity, delayed commands, or software coordination failures can affect the behavior of many vehicles at once.

In 2023, [a fleet of robotaxis caused traffic congestion](https://www.cbc.ca/radio/asithappens/san-francisco-robotaxi-traffic-jam-1.6938440) after several vehicles stopped or became confused in the road network. This illustrates that autonomous vehicles are not only individual CPS devices, but can also become part of a larger connected transportation system.

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/LgyQa0xTzbE?si=h339rPjyWOJ4jLfb"
    title="Cruise Confusion: Driverless Cruise robotaxis create gridlock day after mass expansion approved"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>