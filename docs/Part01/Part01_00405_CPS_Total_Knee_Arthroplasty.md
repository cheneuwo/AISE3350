(robotic-assisted-tka)=
# Robotic-Assisted Total Knee Arthroplasty

**Total knee arthroplasty (TKA)**, commonly called total knee replacement, provides an example of how robotic assistance can improve the accuracy and repeatability of a physical task. The objective is not simply to replace the surgeon’s movements, but to help translate a surgical plan into precisely controlled bone preparation.

## The Challenge: Translating a Plan into Physical Cuts

Conventional TKA relies on the surgeon’s skill and judgement to perform surgical manoeuvres, including drilling and sawing. Some instruments used in orthopaedic surgery resemble tools used in carpentry: saws remove material, drills create holes, and guides help establish the position and direction of a cut. However, surgery involves living tissue, patient-specific anatomy, and the need to protect nearby structures.

During TKA, the surgeon prepares surfaces on the femur and tibia to accommodate the implant components. The position, orientation, and depth of these cuts must be consistent with the selected implant and the surgical plan.

**Cutting guides** help constrain the saw, but they do not eliminate all sources of error. The resulting surface may deviate from the intended plane, and the angles between prepared surfaces may differ from those required for the planned implant placement. Research on surgical saws has examined how blade behaviour affects cutting accuracy. See the [study of saw-blade accuracy and excursion](https://pubmed.ncbi.nlm.nih.gov/23523505/).

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/cRioLC4cY2E?si=t-UcDjpZcUMDumD"
    title="Total Knee Arthroplasty"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

## How Robotic Assistance Can Help

Robotic-assisted TKA combines a digital surgical plan, measurements of the patient’s anatomy, and controlled instrument positioning. Depending on the platform, a robot may position a cutting guide, constrain a surgeon-operated tool, or perform a planned bone-preparation task under supervision.

For example, the **Mako** system uses patient-specific planning and **haptic boundaries** to constrain the saw within a planned cutting region. This provides a form of shared control: the surgeon operates the instrument while the robotic system limits its permitted movement. See the [Mako Total Knee system description](https://www.stryker.com/us/en/joint-replacement/systems/mako-total-knee.html).

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe
    src="https://www.youtube.com/embed/KfqfS5sSqfo?si=wHygiPdvZPJbB7fa"
    title="MAKO Robotic Assisted Total Knee Replacement"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

An **active cutting zone** can therefore be understood as a digitally defined region in which cutting is permitted. Depending on the system, movement or cutting action may be constrained or interrupted when the instrument reaches a boundary. This is different from **tremor filtering**, which suppresses unintended oscillatory movements; the two mechanisms should not be treated as interchangeable or assumed to exist in every TKA platform.

Comparative cadaveric research has demonstrated that particular robotic systems can produce bone resections that are more accurate and reproducible than those achieved with conventional instruments. These findings support the engineering value of robotic assistance, while remaining specific to the systems and conditions studied. See this [comparative study of robotic and conventional TKA](https://pubmed.ncbi.nlm.nih.gov/32448945/).

:::{note} Accuracy, precision, and clinical outcomes

**Accuracy** describes how closely a cut matches its intended position, angle, or depth. **Precision** describes how consistently the task can be repeated.

Improving these engineering measures does not automatically guarantee better patient outcomes. Pain, function, complications, and implant longevity require separate clinical evaluation. For example, a [long-term randomized trial](https://pubmed.ncbi.nlm.nih.gov/31389889/) did not demonstrate superior long-term functional outcomes or implant survivorship for the robotic system it investigated.

:::


:::{note} Discussion

As you watch these videos, consider:

- Who directs the instrument’s movement: the surgeon, the robot, or both?
- How does the system constrain the cutting tool?
- What measurements would the controller need to compare the actual tool position with the surgical plan?
- Which decisions still require the surgeon’s judgement?

:::

## Learning from Surgical Data

Digital surgical systems can record selected information, such as the surgical plan, anatomical measurements, implant alignment, and intraoperative assessments. When combined with postoperative outcomes, these records can support performance review, research, and improvements to future planning.

For example, **ROSA Knee** can connect intraoperative information with mobility and outcome measurements through an associated analytics platform. This allows clinicians to investigate relationships between surgical decisions and recovery. See [ROSA Knee and its data-analysis capabilities](https://www.zimmerbiomet.com/en/products-and-solutions/specialties/knee/rosa--knee-system.html).

However, recording data does not mean that the robot automatically learns from each operation or changes its behaviour for the next patient. Any proposed improvement must be evaluated, and the use of patient data requires appropriate privacy, security, and governance safeguards.

## Connection to Cyber-Physical Systems

Robotic-assisted TKA brings the main elements of a CPS together: a **computational plan** specifies the desired action, **sensors** provide measurements, and **actuators and control algorithms** guide physical interaction with bone.

The central engineering challenge is to make the physical result match the digital plan while respecting safety constraints. This also illustrates why **greater precision does not necessarily imply greater autonomy**: a robot may accurately constrain a tool while the surgeon continues to direct the procedure.