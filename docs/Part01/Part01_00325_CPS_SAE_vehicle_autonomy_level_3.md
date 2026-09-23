# Level 3: Conditional Driving Automation

At **Level 3**, an automated driving system performs the **entire dynamic driving task** under defined operating conditions. This includes steering, acceleration, braking, and monitoring and responding to the driving environment.

The human does not need to supervise the system continuously while the Level 3 feature is operating as intended. However, the human must remain available and capable of resuming driving following a takeover request or an evident vehicle malfunction.

```{figure} ./../../imgs/autonomous_vehicle_level_3.png
:label: fig-driving-level-3
:alt: Vehicle Autonomy, level 3.
:width: 600px
:align: center

## The Human's Role

The human acts as a **fallback-ready user** rather than a continuously supervising driver.

While the feature is engaged, the user may undertake permitted non-driving activities, provided these do not prevent them from receiving an alert and responding appropriately. They must remain awake, available, and able to resume driving in a timely manner.

This does not permit sleeping, leaving the driving position, or becoming unable to respond. Permitted activities depend on the system's instructions and applicable rules.

:::{important}
**Level 2:** The human continuously monitors the driving environment and supervises the system.

**Level 3:** The system monitors and responds to the driving environment, but the human must remain ready to resume driving when required.
:::

## The System's Role

Within its **operational design domain (ODD)**, the system:

- Controls steering, acceleration, and braking.
- Detects and responds to relevant objects and events.
- Makes the decisions needed to perform the driving task.
- Requests human intervention when continued automated operation is no longer supported.

For example, a feature designed for congested highway traffic may request a takeover when traffic conditions move outside its operating limits.

Sensors, computation, and control enable these capabilities. AI may contribute to their implementation, but using AI is not itself a criterion for Level 3 classification.

## Representative Features

### Honda Legend: Traffic Jam Pilot

Honda introduced the Legend equipped with **Honda SENSING Elite** in Japan in March 2021. Its **Traffic Jam Pilot** feature was approved for Level 3 operation under specified traffic-jam conditions on expressways.

This is a historical deployment example: it does not mean that every Honda Legend, or every function of Honda SENSING Elite, operates at Level 3.

### Mercedes-Benz: DRIVE PILOT

Mercedes-Benz **DRIVE PILOT**, offered on suitably equipped S-Class and EQS sedans, is another example of Level 3 driving automation.

In the United States, approved operation includes designated freeways in **California and parts of Nevada**, subject to additional conditions. The manufacturer's U.S. description specifies traffic-jam operation at speeds up to approximately **40 mph (64 km/h)**, together with restrictions concerning weather, lighting, and road conditions.

These limits apply to the particular market and system version; they should not be treated as universal requirements for Level 3.

:::{note}
The classification applies to the **engaged feature**, not simply the vehicle model.

Outside the Level 3 feature's operating conditions, the vehicle may require manual driving or offer lower-level driver assistance.
:::

## Key Takeaway

**The system drives within defined conditions; the human remains available to resume driving when required.**

The transition from Level 2 to Level 3 is therefore a change in responsibility for monitoring and responding to the driving environment—not merely improved steering or speed control.

## Discussion

A Level 3 feature is operating in congested highway traffic. As traffic clears, it issues a takeover request.

- Why must the human resume driving?
- How does the human's role before the request differ from their role at Level 2?
- Why does the ability to perform the complete driving task not make this a Level 4 feature?