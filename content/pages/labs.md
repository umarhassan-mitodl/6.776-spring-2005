---
content_type: page
description: The lab section provides information on lab information sheet, J310 Spice
  Model, Noise Simulation, and Final Comments.
learning_resource_types:
- Laboratory Assignments
ocw_type: CourseSection
title: Labs
uid: 3628204c-86d0-b8ed-62f5-928b9fd6503c
video_files:
  video_thumbnail_file: null
video_metadata:
  youtube_id: null
---

Lab Information Sheet
---------------------

### Equipment

The lab space has oscilloscopes, multimeters, and 5 V power supplies (on breadboard boxes) at each station. There are also soldering irons, several curve tracers, and an LCR impedance analyzer in the room. We only have available one high frequency signal generator. This signal generator is on one of the desks and must be time-shared among groups. There is a parts cabinet located on the other side of the lab that contains general components such as resistors and capacitors.

### Parts

Three different components needed for this lab were handed out in class.

1.  {{% resource_link "21904c77-0baa-41dd-9fab-3eba9dec42aa" "ON Semiconductor J310 JFET" %}} 
2.  {{% resource_link "1eb772ea-bc66-4309-bea2-b42fddb42b11" "Sprague-Goodman GCL 20000 Variable Capacitor" %}} (0.8 pF - 20 pF)
3.  {{% resource_link "82a926ad-fed1-4dc8-ab9a-8780ccf0dbad" "Toko 294SN-T1013Z Tunable Inductor" %}} - Nominal value of 0.47 µH

We have ordered additional transistors and variable capacitors, in addition to various fixed inductors (0.047 µH, 0.1 µH, 0.33 µH, 0.56 µH). We also have 1 µH tunable inductors. These parts will be made available in the lab. One other note is that the tunable inductors have limited tuning range. We advise you to use the tunable inductors as fixed inductors, and rely on the variable capacitors to tune your amplifier.

### Models

J310 Spice Model ({{% resource_link 78984821-a1ad-05ac-6333-283874019730 "SCS" %}})

The J310 Spice model above is compatible with Spectre. This model may or may not be accurate as there are many different manufacturers of J310 transistors and there may be considerable variability in the transistor operating characteristics from lot to lot as well as part to part. I have tweaked the value of the threshold voltage, VTO, in the model based on DC measurements performed on **one** of the transistors. You are encouraged to verify and modify the model, as needed, by comparing simulation results to measured DC characteristics of your specific device. For example, the model currently does not model output conductance. You will want to either measure g{{< sub "ds" >}}, or find its value from the datasheets at your operating point. Transconductance is another important DC device characteristic you should verify.

In order to use the model, copy the model file, jfet.scs, to your MIT server account. Then,

1.  Open a schematic.
2.  Open the Affirma Analog Design Environment window by clicking _Tools_ -> _Analog Environment.  
    _
3.  Click _Setup_ -> _Model Libraries_ ...
4.  Under _Model Library File_, type in the name of the model file and click _Add_. For example, if you placed the model file in your home directory, you would type ~/jfet.scs.
5.  In your schematic view, add the symbol component, **njfet,** that can be found in analogLib.
6.  Edit the properties of your instance and under Model name, type jmod. This is the model name used in the model file.
7.  Make sure any scaling factors in the parameter list for **njfet** are set to 1.

You should then be able to run simulations based on the J310 Spice model.

### Noise Simulation

In this lab project, you will be required to simulate the noise figure of your amplifier. I will list the basic steps necessary to simulate noise figure using Spectre.

1.  In the Affirma Analog Design Environment window, click _Analysis_ -> _Choose_ -> _noise.  
    _
2.  Under _Sweep Variable_, click _Frequency.  
    _
3.  Under _Sweep Range,_ click _Start-Stop_ and type in an appropriate frequency range.
4.  Choose a desired _Sweep Type_ and type in either a number of points or a step size.
5.  Under _Output Noise,_ select _voltage_ and then select your output node as the _Positive Output Node_ and the circuit gnd as your _Negative Output Node.  
    _
6.  Under _Input Noise,_ you can either select an _Input Voltage Source_ or an _Input Port Source._ In either case, click on the input source you are using on the schematic. This input source should have a source resistance of 50 ohms (either embedded in the source if it's a port, or placed external to the source in series, if it's a voltage source).
7.  Click _OK_.
8.  Run the simulation.
9.  Click on _Results_ -> _Direct Plot._ From here, you can plot _Equivalent Output Noise, Equivalent Input Noise, Squared Output Noise, Squared Input Noise,_ or _Noise Figure._ For _Noise Figure,_ select the input node (the top of the input voltage source), the output node, and specify the source resistance as 50 ohms. You will then get a plot of noise figure vs. frequency. If you used a port, the noise figure will be plotted automatically.
10.  You can also do some analysis by clicking _Results_ -> _Print_ -> _Noise Summary.  
    _
11.  Specify _spot noise, Frequency Spot_ _\= 50 MHz, flat weighting, and include All Types._ You can then list the noise contributors individually to see what circuit elements are degrading your noise figure. You can also verify noise figure by taking the total output noise and dividing by the output noise contribution due to the source resistance.

### Final Comments

Keep in mind that we are using JFETs, not MOSFETs. They are similar except their threshold voltage is negative. The device will draw plenty of current with Vgs = 0. Put some thought into how you want to bias your devices.

As we mentioned in class, we encourage you to use lab equipment and parts available to you through your research labs. Most noticeably, we do not have a network analyzer there, which makes it difficult to measure your input match.

Please do your best to clean up after yourselves in the lab. We are using lab space and equipment reserved for other classes so let's not abuse our privileges.

Good luck and have fun!