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

![Original nutcracker design; simplest geometry]({{ "assets/images/old-nutcracker.jpg" | relative_url }}){: style="width: 90%"}

Unfortunately, my diagram was not drawn to scale, and I realized that the nut was far closer to the pin than was feasibly physically possible. 
<br>
As a result, I redesigned the geometry so that the distance to the pins and the output lever arms could be made arbitrarily small by placing the input and outputs perpendicular to each other (instead of along the same arm).

![New design; perpendicular output]({{ "assets/images/nutcracker-fbd.jpg" | relative_url }}){: style="width: 90%"}

This design allows the output arms to be made essentially arbitrarily short (within the constraints of the size of the nut, of course) and the distance between the handles to be essentially whatever you want (partly thanks to the assumption that the input force will always be only in the $$y$$-direction).