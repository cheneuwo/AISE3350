# Level 0: No Driving Automation

At **Level 0**, the human driver remains responsible for the entire driving task, including observing the road, steering, controlling speed, and responding to hazards. The vehicle may provide warnings, convenience features, or momentary safety interventions, but these do not replace the driver's responsibility for driving.


```{figure} ./../../imgs/autonomous_vehicle_level_0.png
:label: fig-driving-level-0
:alt: Vehicle Autonomy, level 0.
:width: 600px
:align: center

**Level 0: No driving automation.** The human driver remains responsible for observing the driving environment, steering, and controlling speed. [Image Courtesy](https://www.niehs.nih.gov/sites/default/files/2025-05/wtp_f23_autonomous_vehicles.pdf)
```

## The Human's Role

The illustration highlights three aspects of the driver's involvement:

- **Eyes on the driving environment:** The driver must continuously observe and interpret road conditions, traffic, and potential hazards.
- **Hands controlling the steering wheel:** The driver is responsible for steering and maintaining the vehicle's path.
- **Feet operating the pedals as needed:** The driver is responsible for acceleration and braking.

These visual cues represent responsibility for the driving task. They should not be interpreted as requiring continuous pressure on a pedal or looking only straight ahead.

## The System's Role

A Level 0 vehicle can still contain sophisticated sensors, computers, and actuators. These may detect hazards, issue warnings, or intervene briefly to help maintain stability or avoid a collision.

The important distinction is that these functions do not take over the driving task on a sustained basis in the sense used by SAE's driving-automation taxonomy.

## Representative Features

The following features may be present during Level 0 driving:

- **[Anti-lock braking system (ABS)](wiki:Anti-lock_braking_system):** Modulates braking pressure to help prevent wheel lock during braking.

- **[Electronic stability control (ESC)](wiki:Electronic_stability_control):** Helps counter a loss of vehicle stability, for example by selectively applying individual wheel brakes.

- **[Conventional cruise control](wiki:Cruise_control):** Maintains a driver-selected speed but does not automatically adjust that speed in response to a slower vehicle ahead. The driver remains responsible for assessing traffic and intervening.

- **[Blind spot warning](wiki:Blind_spot_monitor):** Alerts the driver to a detected vehicle in a blind spot.

- **[Automatic emergency braking (AEB)](wiki:Automated_emergency_braking_system):** Applies or supplements braking to help avoid an imminent collision or reduce its severity.

- **[Forward collision warning (FCW)](wiki:Collision_avoidance_system):** Warns the driver of a potential collision ahead but does not itself apply the brakes.

- **[Lane departure warning (LDW)](wiki:Lane_departure_warning_system):** Alerts the driver when the vehicle unintentionally approaches or crosses a lane boundary, without providing steering control.

:::{important}
**Conventional cruise control is different from adaptive cruise control.**

Conventional cruise control maintains a selected speed. Adaptive cruise control also responds to a vehicle ahead by adjusting speed to maintain a following gap. When operating independently as a sustained longitudinal-control feature, adaptive cruise control is associated with Level 1.
:::

These safety and convenience features are not exclusive to Level 0 vehicles; they may also be present in vehicles with higher-level automation.

## Key Takeaway

**No driving automation does not mean no computation, feedback control, or automatic intervention.** Level 0 vehicles can contain many CPS components while leaving the driving task with the human.