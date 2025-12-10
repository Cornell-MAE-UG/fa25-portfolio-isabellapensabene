---
layout: project
title: Torque Wrench Analysis and Design
description: Class project with CAD and Ansys
technologies: [Soldiworks, Ansys, MATLAB]
image: /assets/images/TWCAD.png
---


For our Mechanics of Engineering Materials class, we were asked to use Ansys to analyze a base design for a torque wrench. We did this by using MATLAB to write a script to hand calculate the stresses in the wrench and factors of safety against brittle failure, fatigue failure, and failure with crack growth. Then, we cadded the base model of the torque wrench in Solidworks and used Ansys to analyze the stresses and deformation in the wrench. We compared these values to the values we hand calculated. 

The next part of the project was to design our own torque wrench to meet specific safety factor and strain gauge sensitivity requirements. First we had to choose our material, for which we selected Titanium, specifically, Ti-6Al-4V. One reason we selected this material is because it has a very high strength to weight ratio. This is optimal for a tool that someone may need to carry around because it will be light enough to carry but still offer the strength required of a tool under high loads. Another reason we chose this material is because it has a high fatigue life as compared to aluminum, which is also light. This is also important for our application because the torque wrench will be used over and over again, so it needs to have a high fatigue life. Titanium is also less stiff than steel, which helps us meet our sensitivity goal. 

With our material selected, we used our MATLAB script to iterate through different dimensions of the torque wrench until we found a combination which met both the required saftey factors and sensitivity requirements. Below is a diagram of our CAD model with the relevant dimensions called out. 

<img src="{{ '/assets/images/TWCAD.png' | relative_url }}" width="200">

We used Ansys Static Structural to analyze the torque wrench we had designed. We applied zero displacement supports to the 4 sides of the drive. We applied the force of 37.5 lbs (equal to the moment = 600 in-lbs divided by the length from the end to the center of the drive) to the end of the torque wrench. These supports and loads are displayed in the image below. 

![Picture of Supports]({{ "/assets/images/TWsupports.png" | relative_url }}) 

From our FEM analysis, we retrieved the normal strain contours (in the strain gauge direction) and contour plot of the maximum stress, picutred below. The maximum deflection occured at the load point and had a value of __. The maximum normal stress occured in the drive of the torque wrench, with a value of __ psi. 

![Maximum Normal Stress]({{ "/assets/images/TWmaxprinstress.png" | relative_url }})
![Load Point Deflection]({{ "/assets/images/TWdeform.png" | relative_url }})

The strains at the strain gauge location were __. This is also shown in the image below. 

![Strain Probe]({{ "/assets/images/TWstrainprobe.png" | relative_url }}) 

torque wrench sensitivty and strain gauge seleciton 
