---
layout: project
title: Nutcracker Designs - ENGRD 2020 Homework 4
description: ENGRD 2020 (Statics) Homework Assignment
technologies: [Nothing, really; just an iPad and a notetaking app (also, why is this variable an array? doesn't a single string work fine? its elements get joined back together with commas anyway in the default project.html layout)]
image: /assets/images/nutcracker-fbd.jpg
---

<b>Design Objective:</b> Find dimensions and geometry for a nutcracker with enough mechanical advantage to crack the shell of a macadamia nut using the average adult maximum grip strength. 


<hr>
<b>Design Constraints:</b> 
The following data was gathered from various online sources.
<ul>
    <li>Macadamia nut compressive strength: \(222.18\pm18.54\) kgf (source: <a href="https://link.springer.com/article/10.1007/s10071-007-0131-2#appendices" target="_blank">Do capuchin monkeys use weight to select hammer tools? Appendix 1</a>)</li>
    <li>Average maximum grip strength: \(<17\) kgf (source: <a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC10777545/#Sec3" target="_blank">Hand grip strength as a proposed new vital sign of health</a> ) </li>
    <li>Commercial macadamia nut sizes: \(16\text{\textendash18}\) mm (small); \(>28\) mm (extra large) (source: <a href="https://unece.org/fileadmin/DAM/trade/agr/standard/dry/dry_e/InshellMacadamiaNutsRec2008_e.pdf" target="_blank">New UNECE Standard for Inshell Macadamia Nuts</a> ) </li>
    
    <li>Average hand breadth: \(~8\) cm (male); \(~7\) cm (female) (source: <a href="https://www.researchgate.net/figure/Measurements-cm-of-hand-breadth-in-males-and-females_tbl2_257737146" target="_blank"> Determination of sex from hand dimensions and index/ring finger length ratio in Upper Egyptians </a>) </li>
</ul>
Based on the data above, the following design parameters were chosen:
<ul>
    <li>Force amplification of \(\frac{250}{15}=\frac{50}{3}\approx 16.7\)</li>
    <li>Maximum input distance (i.e. between handles) of \(\sim 70\) mm</li>
    <li>Maximum length of \(\sim 150\) mm (arbitrarily chosen as about \(6\) in; feels like a reasonable maximum size for a handheld device)</li>
</ul>
Note that I did not consider material properties or internal loads, that I do not have a rigorous metric of how "usable" the design is (I did not get a lot of data on ergonomics or anything; most of the dimensional restraints were pure estimates), and many simplifications were made with respect to the input and output force directions (e.g. they are both aligned with the axes defined in the FBD no matter the angle between the handles or where the contact with the nut was).
<br>
It is also worth noting that the input distance limitation combined with the mechanical advantage ratio gives an output distance of $$\frac{3}{50}(70)=4.2$$ mm of output movement. This was assumed to be enough for the results of the study to apply, where 5 mm and 10 mm displacements were used (which the study stated had no perceivable difference).


<b>Approach:</b>
I originally planned to design the simplest geometry possible by making the handle arms $$\frac{50}{3}$$ times the distance of the nut to the pivot pin, as shown below.

{:style="text-align:center;"}
![Original nutcracker design; simplest geometry]({{ "assets/images/old-nutcracker.jpg" | relative_url }}){: style="width: 90%"}

Unfortunately, my diagram was not drawn to scale, and I realized that the nut was far closer to the pin than was feasibly physically possible. 
<br>
As a result, I redesigned the geometry so that the distance to the pins and the output lever arms could be made arbitrarily small by placing the input and outputs perpendicular to each other (instead of along the same arm).

{:style="text-align:center;"}
![New design; perpendicular output]({{ "assets/images/nutcracker-fbd.jpg" | relative_url }}){: style="width: 90%"}

This design allows the output arms to be made essentially arbitrarily short (within the constraints of the size of the nut, of course) and the distance between the handles to be essentially whatever you want (partly thanks to the assumption that the input force will always be only in the $$y$$-direction).

We can calculate the mechanical advantage via a moment balance about point $$B$$ for one of the handles, as below:

{:style="text-align:center;"}
![New design; perpendicular output]({{ "assets/images/nutcracker-handle-FBD.jpg" | relative_url }}){: style="width: 90%"}

$$\sum M_B=(9)\frac{1}{2}(F_{out})-150(F_{in})=0$$

$$\frac{F_{out}}{F_{in}}=2\left(\frac{150}{9}\right)=22\left(\frac{50}{3}\right)$$

which is twice the previously stated goal for the mechanical advantage of this device (again, the dimensions can be adjusted quite freely; for example, the handles could be made half the length to make the mechanism smaller while still achieving the intended mechanical advantage).

<b>Usability:</b> The final design provides much greater freedom to fit the design constraints that I decided on and could easily be modified to go beyond (if new metrics for greater usability are found, for example). The length of the design is relatively convenient at about $$6$$ inches long, and the mechanical advantage as the dimensions currently are is more than enough for the average adult to crack open a macadamia nut (since it was designed to over-accomodate for even the weaker end of average maximum grip strength, macadamia nut strength, and macadamia nut size). More information would be needed with regards to materials to determine the durability, reliability, and comfort of the design.