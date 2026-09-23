(privacy-personal-autonomy)=
# Privacy and Personal Autonomy

Throughout this chapter, *autonomy* has described a machine's ability to perform tasks without continuous human control. However, another form of autonomy deserves equal attention: **personal autonomy**, or a person's ability to make informed choices about their own life, body, and interactions with technology.

```{figure} https://wp.technologyreview.com/wp-content/uploads/2022/12/A_3-crop.jpg?fit=1920,1280
:alt: Vehicle Autonomy, level 0.
:width: 600px
:align: center
```
Greater robotic autonomy should support human independence, rather than diminish people's control over their surroundings and personal information.

## When a Robot Observes More Than Its Task Requires

Consider a robot vacuum cleaner. Its sensors help it navigate, identify obstacles, and clean effectively. However, a camera operating inside a home may also capture people, possessions, and private activities that are unrelated to cleaning.

A December 2022 [MIT Technology Review investigation](https://www.technologyreview.com/2022/12/19/1065306/roomba-irobot-robot-vacuums-artificial-intelligence-training-data-privacy/) reported that sensitive household images captured by development versions of iRobot's Roomba robots had appeared in private social-media groups. The images had been supplied to Scale AI for annotation as part of an AI-training process, and some workers shared them outside that process.

According to iRobot, the images came from specially modified development robots used by participating employees and paid data collectors, rather than ordinary consumer products. The company stated that participants had agreed to data collection.

:::{important}
**Agreement to collect data is not permission to distribute it without restriction.**

This case illustrates why privacy protections must extend beyond the robot itself to the organisations, contractors, and people who subsequently handle its data.
:::

## Privacy Is More Than Cybersecurity

Cybersecurity helps protect systems and data against unauthorised access or manipulation. Privacy also concerns **whether information should be collected in the first place**, what purposes justify its use, and who should be allowed to see it.

A system could securely transmit information to an authorised recipient while still creating a privacy concern—for example, if users did not meaningfully understand that people outside the manufacturer would review images recorded inside their homes.

For CPS design, we should therefore ask:

- **Necessity:** What information is actually needed to perform the task?
- **Purpose:** Is the information used only to operate the device, or also to train models and develop other services?
- **Access:** Who can view the information, including contractors and subcontractors?
- **Retention:** How long is it stored, and how is it deleted?
- **Choice:** Can users decline optional data collection without losing essential functionality?

## Preserving Personal Autonomy

Meaningful consent requires more than an agreement presented during setup. People need understandable explanations and practical choices about what a system observes, records, and shares.

The person purchasing or operating a robot may not be the only person affected. Household members, visitors, children, patients, and healthcare workers may also enter its sensing environment. Their interests cannot simply be assumed to match those of the device owner.

In medical robotics, this distinction is particularly important. Agreeing to a robot-assisted procedure and agreeing to have recordings reused for AI training are different decisions. A responsible design should distinguish these purposes and make the relevant choices clear.

Possible engineering measures include processing data locally where feasible, collecting only necessary information, limiting storage, restricting and auditing access, and providing clear recording indicators. These measures should accompany—not replace—meaningful consent and organisational accountability.

:::{note} Discussion

A household robot needs camera images to avoid obstacles, while its manufacturer would also like to use those images to improve future models.

1. Which data are necessary for immediate operation, and which serve a separate purpose?
2. How could the robot remain useful if the user declines to contribute training data?
3. How should the system protect visitors who never agreed to its terms?
:::

## Concluding Perspective

A successful CPS must do more than perform its physical task accurately. It should also respect the people it observes and affects.

**The objective is not simply to make machines more autonomous, but to ensure that their growing capabilities preserve human privacy, choice, and control.**