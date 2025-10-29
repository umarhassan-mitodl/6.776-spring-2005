---
content_type: page
description: The projects section provides information on final project assignment
  - RF power amplifier design.
learning_resource_types:
- Projects
ocw_type: CourseSection
title: Projects
uid: f37aa8c0-8f4e-902f-c366-474bab3f974f
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

Final Project Assignment - RF Power Amplifier Design
----------------------------------------------------

Work in a group of two. Only one report should be turned in per group.

### Project

The objective of this project is to design and simulate a 2 GHz power amplifier for narrowband communication systems. The power amplifier to be designed will output a constant-envelope signal suitable for phase modulation systems. The amplifier must meet the specifications listed below. It is recommended that you first select the overall circuit topology and do enough hand calculations to determine that the required specifications are approximately met. For hand calculations, use the device parameters published in the spec sheets.

Inductors should be first designed according to the reference paper from Thomas Lee's group (Mohan, et. al. "Simple, Accurate Expressions for Planar Spiral Inductances." _JSSC_ (Oct 1999): 1419-1424.) The inductor (or transformer) geometry should then be entered in ASITIC and its model extracted.

Spectre RF should be used to simulate and fine-tune the amplifier performance - be sure to include the full inductor models (i.e., including loss and parasitic capacitance) in your schematic.

{{< tableopen >}}
{{< theadopen >}}
{{< tropen >}}
{{< thopen >}}
SpecificationS
{{< thclose >}}
{{< thopen >}}
ValueS
{{< thclose >}}

{{< trclose >}}

{{< theadclose >}}
{{< tropen >}}
{{< tdopen >}}
Power Supply
{{< tdclose >}}
{{< tdopen >}}
Single \< 1.8 V
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Load
{{< tdclose >}}
{{< tdopen >}}
50Ω (resistive)
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
RF Output Power (at 50Ω load)
{{< tdclose >}}
{{< tdopen >}}
100mW+-10%
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Center Frequency
{{< tdclose >}}
{{< tdopen >}}
2.0 GHz
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Power Efficiency
{{< tdclose >}}
{{< tdopen >}}
\> 75%
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
RF Input Power
{{< tdclose >}}
{{< tdopen >}}
\< 20mW
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Distortion
{{< tdclose >}}
{{< tdopen >}}
\< -30dBc
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Inductor Q (@2GHz)
{{< tdclose >}}
{{< tdopen >}}
Use ASITIC
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Capacitor Q (@2GHz)
{{< tdclose >}}
{{< tdopen >}}
Infinite
{{< tdclose >}}

{{< trclose >}}
{{< tropen >}}
{{< tdopen >}}
Process
{{< tdclose >}}
{{< tdopen >}}
TSMC 0.18µ no high voltage transistor option
{{< tdclose >}}

{{< trclose >}}

{{< tableclose >}}

  

At no time allow the voltage across the gate oxide of any transistor to exceed 2.5V, even during transients.

The write-up for this project **is limited to 3 pages** plus schematics, Spectre plots, inductor design, layout, and any other figures. The report is due in session 25. This is not a trivial design, so start working soon.