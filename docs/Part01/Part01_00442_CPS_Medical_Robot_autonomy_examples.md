(advanced-medical-robots)=
# Examples of Advanced Medical Robots

Medical robots demonstrate how sensing, computation, and control can be integrated to perform precise physical actions. Their applications range from preparing bone for joint replacement and assisting surgeons with instrument manipulation to inserting needles and delivering radiation.

The following four examples illustrate different approaches to robotic assistance and task automation. They include established commercial systems, a historically important platform, and a research prototype.

## ROBODOC: Image-Guided Bone Preparation

ROBODOC is a historically important example of robotic automation in orthopaedic surgery. Its development is associated with the technology lineage of [THINK Surgical](https://thinksurgical.com/), based in Fremont, California.

In the original hip-replacement application, the surgeon used computed tomography (CT) images to select and position an implant digitally. The robot then machined a corresponding cavity in the femur according to the surgical plan.

Important technical features included:

- **Image-to-robot registration:** The system established the spatial relationship between the CT-based model and the physical bone. Early implementations combined manual guidance with autonomous tactile searches for implanted reference pins; registration was therefore not an entirely autonomous process.
- **Planned cutting with force monitoring:** The robot followed a planned machining path while a force sensor monitored its interaction with the bone. Excessive forces could trigger a pause or shutdown.
- **Spatial safety constraints:** Early designs included independent monitoring of whether the cutter remained within a predefined permitted volume. This illustrates the principle of using software-defined boundaries to constrain physical actions.
- **Surgeon supervision:** The surgeon could pause the robot, assess its status, initiate recovery actions, or discontinue robotic operation.

These mechanisms are described in [*Taming the Bull: Safety in a Precise Surgical Robot*](https://www.cs.jhu.edu/~rht/RHT%20Papers/1991/Taming%20the%20Bull.pdf) and [*An Image-Directed Robotic System for Precise Orthopaedic Surgery*](https://doi.org/10.1109/70.294202).

:::{note}
**Historical and current platforms**

ROBODOC should not be treated as interchangeable with every current THINK Surgical product. For example, the commercially marketed [TMINI system](https://thinksurgical.com/tmini/) is a handheld robotic platform that uses a CT-based plan to help position bone pins for attaching knee-replacement cutting guides. This differs from ROBODOC's robotic bone-milling approach.
:::

## da Vinci: Surgeon-Controlled Robotic Assistance

The [da Vinci surgical systems](https://www.intuitive.com/en-us/products-and-services/da-vinci), developed by [Intuitive](https://www.intuitive.com/en-us), assist surgeons in minimally invasive procedures.

The surgeon operates from a console, using hand controls to direct robotic instruments while viewing the surgical site through an endoscopic camera. The robot translates the surgeon's commands into instrument movements; it does not independently decide which surgical procedure to perform.

Depending on the system and configuration, capabilities include:

- **Motion scaling:** Larger movements of the surgeon's hands can be translated into smaller instrument movements, supporting fine manipulation.
- **Hand-tremor filtering:** Unintended tremor is filtered from the commanded instrument motion.
- **Instrument positioning:** Surgeon-controlled robotic instruments provide articulated movement within the surgical workspace.
- **Camera positioning:** The surgeon can control the endoscope to adjust the view of the operative field.
- **Setup assistance:** Features such as guided setup and targeting help the operating-room team position and dock the system. These should not be described as fully autonomous docking.

Intuitive describes these setup capabilities on its [system software page](https://www.intuitive.com/en-us/products-and-services/da-vinci/software).

This example illustrates an important distinction: **a robot can provide sophisticated motion control without independently making surgical decisions**.

Demonstrations are available on [Intuitive's video channel](https://www.youtube.com/@Intuitive).

## Veebot: Image-Guided Needle Insertion

[Veebot](https://www.veebot.com/) illustrates how medical imaging and robotic manipulation can be combined to automate intravenous needle insertion.

The approach described in [Veebot's patent](https://patents.google.com/patent/US9913605B2/en) combines complementary sensing methods:

- **Infrared imaging:** Helps identify candidate veins beneath the skin.
- **Ultrasound imaging:** Provides additional information about the target vessel, including its position and depth.
- **Computer-based planning:** Processes the imaging information to determine an insertion site and needle trajectory.
- **Robotic actuation:** Positions and advances the needle towards the selected target.

Ultrasound does not physically insert the needle. It provides measurements that inform the robot's positioning and insertion actions.

This is a useful CPS example because the success of the physical action depends on interpreting sensor measurements and translating them into controlled motion.


<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/IpdTeGPruFA?si=WL-0c38CkwgUH3cj"
    title="Veebot"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>


:::{important}
**Prototype, not a commercially available product**

As checked in September 2026, the [manufacturer's website](https://www.veebot.com/solutions.html) describes Veebot as a prototype that is not available for sale. It should therefore be presented as a development example rather than an established commercial clinical system.
:::


## CyberKnife: Image-Guided Robotic Radiation Delivery

[CyberKnife](https://www.accuray.com/cyberknife/), developed by [Accuray](https://www.accuray.com/), is a commercially available robotic radiation-treatment system.

Despite its name, CyberKnife does not use a physical knife. A linear accelerator mounted on a robotic manipulator directs radiation towards a treatment target from multiple orientations. Applications include stereotactic radiosurgery and stereotactic body radiation therapy, with treatment sites extending beyond the brain and spine.

Its capabilities include:

- **Image-guided targeting:** X-ray imaging helps determine the target's position using anatomical structures or implanted markers, depending on the treatment.
- **Robotic positioning:** The manipulator positions the radiation source to deliver the prescribed treatment.
- **Motion compensation:** For respiratory-motion tracking, the Synchrony system combines internal target information from X-ray images with external breathing-motion measurements. A computational model relates these measurements so that delivery can adapt to target movement.
- **Clinician-directed treatment:** The clinical team establishes and approves the treatment plan; automated delivery does not mean that the robot independently chooses the patient's treatment.

Further details are available in the [CyberKnife technical specifications](https://www.accuray.com/wp-content/uploads/cyberknife-treatment-delivery-system_-technical-specifications.pdf).

Demonstrations are available on [Accuray's video channel](https://www.youtube.com/@AccurayIncorporated).

## Connecting These Examples to CPS Theory

These systems use different combinations of sensors, computational models, actuators, and human supervision. However, each connects digital information to physical action: preparing bone, manipulating instruments, inserting a needle, or directing radiation.

:::{important}
**Advanced robotics does not necessarily imply high autonomy.**

Precision, motion compensation, and sophisticated feedback control are not the same as independent clinical decision-making. An autonomy classification must consider the particular task and operating mode, rather than the product name alone.
:::

:::{note} Discussion

Choose one of the four examples:

1. What physical quantities does the system measure?
2. What actions does it control?
3. Which decisions remain with the human operator?
4. How should the system respond if its sensor measurements become unreliable?
:::