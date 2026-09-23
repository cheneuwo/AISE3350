# Level 1: Driver Assistance

At **Level 1**, a driving automation feature provides sustained assistance with **either steering or acceleration and braking**, but not both simultaneously. The human driver remains actively involved, continuously monitors the driving environment, supervises the system, and intervenes whenever necessary.

In the terminology emphasized by SAE J3016_202609, this is driver support for **steering OR speed**, with continual driver supervision.

```{figure} ./../../imgs/autonomous_vehicle_level_1.png
:label: fig-driving-level-1
:alt: Vehicle Autonomy, level 1.
:width: 600px
:align: center
```

## The Human's Role

The driver performs the driving tasks that the system does not undertake and remains responsible for monitoring and responding to the road environment.

- When the system controls acceleration and braking, the driver controls steering.
- When the system provides sustained steering assistance, the driver controls acceleration and braking.
- In either case, the driver must supervise the assistance feature and be ready to override it.

The driver is therefore not merely waiting for a request to take over: they remain continuously engaged in driving.

## The System's Role

The system uses sensor measurements and feedback control to assist with one aspect of vehicle motion:

- **Longitudinal control:** Adjusting acceleration and braking to regulate speed and following distance.
- **Lateral control:** Adjusting steering to help maintain the vehicle's position within its lane.

This assistance operates within the feature's specified conditions and limitations.

## Representative Features

### Adaptive Cruise Control

[Adaptive cruise control (ACC)](https://tc.canada.ca/en/road-transportation/driver-assistance-technologies/driving-control-assistance/adaptive-cruise-control) uses sensors to monitor a vehicle ahead and adjusts speed to maintain a driver-selected following gap. When the road ahead is clear, it regulates speed toward the driver's selected setting.

Unlike conventional cruise control, ACC responds to changes in the traffic ahead. However, the driver must continue steering, monitoring traffic, and intervening when required. For example, braking beyond the system's capability may be necessary.

### Lane Centring Assistance

**Lane centring assistance** provides sustained steering adjustments to help keep the vehicle near the centre of its lane. When used independently as a Level 1 feature, the driver continues to control speed and braking while supervising the steering assistance.

:::{important}
**Lane keeping and lane centring are not necessarily the same.**

A lane-keeping feature that intervenes briefly when the vehicle approaches a lane boundary does not, by itself, qualify as Level 1 driving automation.

A lane-centring feature that provides sustained steering assistance can qualify as Level 1 when operating without simultaneous automated longitudinal control.
:::

## Key Takeaway

**The system assists with one aspect of vehicle motion; the human continues driving and supervising.**

A vehicle may contain both ACC and lane-centring features. Classification depends on how they operate: an engaged feature providing sustained control of both steering and acceleration/braking under driver supervision falls within Level 2.

## Discussion

A vehicle uses ACC to maintain its following distance while the driver steers through a curve.

- Which tasks are performed by the system?
- Which responsibilities remain with the driver?
- Why must the driver continue monitoring traffic even though the system measures the vehicle ahead?