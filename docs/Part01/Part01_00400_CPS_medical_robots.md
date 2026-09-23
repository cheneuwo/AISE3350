(medical-robotics)=
# Medical Robotics

Medical robotics provides another example of how computation, sensing, and control can be integrated to perform precise physical tasks. In surgery, robots can assist clinicians by positioning instruments, guiding movements, or executing selected tasks under human supervision. However, **robotic surgery does not necessarily mean autonomous surgery**: a robot may follow a surgeon's movements directly, execute a predefined plan, or adapt its actions using sensor measurements.

Recent advances in artificial intelligence—including **vision–language models (VLMs)**, which combine visual information with language—are creating new possibilities for surgical automation. For example, the research system [SRT-H](https://arxiv.org/abs/2505.10251) combines visual observations with language-conditioned task planning and robotic control to perform surgical tasks in an experimental setting. Such demonstrations should not be confused with establishing that a system can safely perform an entire operation autonomously on a human patient.

## Historical Example: ROBODOC

Medical robotics predates these recent developments in AI. An important early example is **ROBODOC**, developed through collaboration involving orthopaedic surgeon **William Bargar**, veterinarian **Howard “Hap” Paul**, and researchers and engineers at the University of California, Davis, and IBM.

On **November 7, 1992**, a surgical team led by Bargar used ROBODOC in a human hip replacement at Sutter General Hospital in Sacramento, California. This procedure was part of an FDA-authorized investigation into the device's safety and feasibility. The [Smithsonian's history of ROBODOC](https://americanhistory.si.edu/collections/object/nmah_1842522) documents this milestone and the collaboration behind the system.

:::{note} Clinical investigation versus marketing clearance

Authorization to investigate a medical device in human patients is not the same as clearance to market it for clinical use. ROBODOC's early human procedures took place in 1992; the DigiMatch ROBODOC Surgical System subsequently received **FDA 510(k) clearance in 2008** for its specified application in primary total hip arthroplasty. See the [FDA clearance documentation](https://www.accessdata.fda.gov/cdrh_docs/pdf7/k072629.pdf).

:::

## The Clinical Problem: Preparing Bone for an Implant

In **total hip arthroplasty**, or total hip replacement, an artificial implant replaces damaged joint components. Although implants can be manufactured in standardized sizes, each patient's anatomy is different. The surgeon must therefore select an appropriate implant and prepare the bone so that it accommodates the implant in the planned position.

For the femoral component—the part inserted into the thigh bone—this involves creating a cavity with an appropriate shape, size, and orientation. Traditionally, surgeons prepare this cavity using manually operated instruments, including broaches and reamers. ROBODOC was developed to improve the accuracy and consistency of this preparation, particularly for cementless hip implants. Its design and early clinical evaluation are described by [Bargar and colleagues (1998)](https://doi.org/10.1097/00003086-199809000-00011).

The system combined computer-based planning with robotic execution. Using patient-specific medical images, the surgeon could select the implant and plan its position. The robot then used a milling tool to prepare the femoral cavity according to that plan, under the surgeon's direction. The [FDA system description](https://www.accessdata.fda.gov/cdrh_docs/pdf7/k072629.pdf) explains the roles of the ORTHODOC planning workstation and the ROBODOC robotic surgical tool.

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/yEO4dMWmYro?si=VPLYRACgegU5AAdN"
    title="ROBODOC"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

## From Robotic Assistance to Autonomy

From a CPS perspective, ROBODOC illustrates how a computational representation of a patient's anatomy can guide a physical action. Medical images and planning software form part of the **cyber component**, while the robotic mechanism, cutting tool, and interaction with bone constitute the **physical component**. Control connects the planned action to the motion of the physical mechanism.

This example also illustrates an important distinction: **automating a specific surgical task is not the same as automating an entire surgical procedure**. Executing a planned bone-milling task does not mean that the robot independently selects the treatment or manages every stage of the operation.

As with driving automation, discussing autonomy therefore requires us to identify the division of work between the human and the machine. For medical robots, the central questions are: Which decisions and actions belong to the clinician? Which belong to the robot? How much supervision is required, and what happens if the system encounters an unexpected situation? These questions provide the starting point for examining levels of autonomy in medical robotics.

:::{note} Discussion

Consider a robot that automatically mills bone according to a surgeon-approved plan:

- Which parts of the task involve computation, sensing, and physical action?
- Which decisions remain with the surgeon?
- Why does successful execution of this task not establish that the robot can perform the entire operation autonomously?

:::