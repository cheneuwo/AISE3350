# Level 2: Driver Support for Steering and Speed

At **Level 2**, a driving assistance feature provides sustained control of **both steering and acceleration/braking** under specified operating conditions. The human driver must continuously supervise the system, monitor the driving environment, and intervene whenever necessary.

This level is commonly known as **partial driving automation**. The defining distinction from Level 1 is simultaneous assistance with both aspects of vehicle motion—not a transfer of responsibility for supervising the driving environment.

```{figure} ./../../imgs/autonomous_vehicle_level_2.png
:label: fig-driving-level-2
:alt: Vehicle Autonomy, level 2.
:width: 600px
:align: center
```

## The Human's Role

Although the system controls steering and speed, the human remains actively engaged in driving. The driver must:

- Continuously observe traffic, road conditions, and potential hazards.
- Supervise the system and recognize when its behaviour is inappropriate.
- Intervene when necessary, including by steering or braking.
- Follow the feature's operating instructions and limitations.

The driver must not wait for a warning before responding to a situation that requires intervention.

## The System's Role

The system combines:

- **Lateral control:** Steering to help maintain the vehicle's path.
- **Longitudinal control:** Adjusting acceleration and braking to regulate speed and following distance, or to perform a low-speed manoeuvre.

For example, a highway assistance feature may combine adaptive cruise control with lane centring. A supervised parking feature may coordinate steering, acceleration, and braking while moving into a parking space.

These capabilities operate within specified conditions; they do not mean that the system can handle every situation it encounters.

## Representative Features

### Highway Driving Assist

**Highway Driving Assist** combines steering assistance with speed and following-distance control on supported roads. It can help keep the vehicle centred in its lane while adjusting speed in response to traffic ahead.

The driver must continue monitoring the road and supervising the feature. Its capabilities depend on the particular implementation and operating conditions.

### Supervised Automatic Parking Assist

**Supervised automatic parking assistance** can qualify as Level 2 when it provides sustained control of both steering and acceleration/braking during a parking manoeuvre.

The human supervises the manoeuvre, checks for obstacles and other road users, and intervenes when needed. Some implementations require the user to hold a control button throughout the manoeuvre.

:::{important}
Not every feature marketed as “automatic parking” is Level 2.

- **Steering assistance only**, with the human controlling acceleration and braking, can qualify as Level 1.
- **Combined steering and speed control**, with continuous human supervision, can qualify as Level 2.

Classification depends on the feature's capabilities and required human involvement—not its name.
:::

## Key Takeaway

**The system controls both vehicle-motion axes, but the human continuously monitors the driving environment and remains responsible for intervening when needed.**

Hands-free operation, where permitted by a particular feature, does not mean attention-free operation.

## Discussion

A vehicle maintains its lane and following distance while approaching roadworks with temporary lane markings.

- Which tasks are being performed by the system?
- What must the driver continue to monitor?
- Why does controlling both steering and speed not make the feature driverless?