# CPS Example: Pacemakers

A [pacemaker](wiki:Pacemaker), also known as an **artificial cardiac pacemaker**, is an implanted medical device that generates electrical pulses delivered by electrodes to one or more of the [chambers of the heart](https://en.wikipedia.org/wiki/Heart#Chambers). Each pulse causes the targeted chamber(s) to contract and pump blood, thus regulating the function of the [electrical conduction system of the heart](wiki:Cardiac_conduction_system).


*Traditional* pacemakers, also called *transvenous pacemakers*, have three components:

- **A pulse generator** creates the electrical pulses. It is   [hermetically sealed](wiki:Hermetic_seal) and contains a power source   (i.e., a battery).
- **Wires, also called leads,** are implanted inside the veins and carry the pulses to the heart.
- **Electrodes** sense the natural heartbeats. When the heartbeat is   slower than normal, the electrodes deliver electrical impulses to   the heart to make it beat normally.

```{image} https://www.nhlbi.nih.gov/sites/default/files/inline-images/images_279.jpg
:alt: Grapes on a vineyard
:width: 500px
:align: center
```

A modern alternative is a [leadless pacemaker](https://my.clevelandclinic.org/health/treatments/17166-pacemakers-leadless-pacemaker), which is smaller and is about the size of a large pill capsule. The pulse generator and electrodes are all contained in **one** device. This device is placed inside a chamber of the heart through a small tube inserted into one of the veins. It is typically implanted in the
right ventricle:

```{image} https://my.clevelandclinic.org/-/scassets/images/org/health/articles/17166-leadless-pacemaker-illustration
:alt: Grapes on a vineyard
:width: 500px
:align: center
```

The **advantages of a leadless pacemaker** over a traditional pacemaker include:

- No need for connecting leads (wires), a separate power source, or the   creation of a surgical pocket in the chest to hold the power source. These are the most common sources of traditional pacemaker complications, such as **infections** or **broken leads**.
- No lump under the skin on the chest or leads anchored to muscle, which can cause minor discomfort.
- No chest incision or scar from generator placement and replacement.
- Potentially a shorter procedure time than a traditional pacemaker implantation procedure.
- With no wires or generator, there is no need to limit upper-bodyactivity after implantation.
- It is safe for the patient to undergo imaging using an [MRI](wiki:Magnetic_resonance_imaging) machine.

```{admonition} Disadvantages of a leadless pacemaker
:class: important

Using the Cleveland Clinic page linked above, identify some disadvantages of a leadless pacemaker.
```

Refer to the following video comparing conventional lead-based pacemakers with leadless pacemakers:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/1M3vAqRLuy0?si=rCcC36GcGoiP-xJn"
    title="Conventional versus leadless pacemakers"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

## Why Is It a Cyber-Physical System?

A pacemaker is a CPS because its computational and physical components operate in a feedback loop. Sensors observe cardiac activity; digital processing interprets these measurements; and output circuitry delivers electrical stimulation that influences subsequent heart activity.

Bogdan and colleagues describe this interaction through observation, model identification, computation, communication, control, and actuation [@BJM2013]. Measurements therefore do more than record the patient's condition: they inform a model used to determine pacing actions. Communication also supports interaction with medical devices and experts.

The article emphasizes **heart-rate variability**, including the temporal relationships between successive heartbeat intervals. The authors propose fractional-order models and constrained optimal control to account for this behaviour. Their approach illustrates why choosing an appropriate physical model matters to controller design.

Implementation also matters. The authors investigate an FPGA realization to examine hardware requirements, connecting the mathematical controller to its computational implementation.

Thus, the pacemaker is not merely an electronic device attached to the heart. It participates in a coupled system in which **physical behaviour informs computation, and computation influences physical behaviour**.