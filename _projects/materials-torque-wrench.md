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

<img src="{{ '/assets/images/TWCAD.png' | relative_url }}" width="450">

We used Ansys Static Structural to analyze the torque wrench we had designed. We applied zero displacement supports to the 4 sides of the drive. We applied the force of 37.5 lbs (equal to the moment = 600 in-lbs divided by the length from the end to the center of the drive) to the end of the torque wrench. These supports and loads are displayed in the image below. 

<img src="{{ '/assets/images/TWsupports.png' | relative_url }}" width="450"> 

From our FEM analysis, we retrieved the normal strain contours (in the strain gauge direction) and contour plot of the maximum principle stress, picutred below.

Normal strain contours in strain gauge direction: 
<img src="{{ '/assets/images/TWstrainingaugedir.png' | relative_url}}" width="450>

Maximum principle stress:
<img src="{{ '/assets/images/TWmaxprinstress.png' | relative_url }}" width="450">

The maximum normal stress in the x-direction in the drive was _ psi. 
<img src="{{ '/assets/images/TWmaxnorm.png' | relative_url }}" width="450">

The maximum deflection occured at the load point and had a value of 0.45967 in. 
<img src="{{ '/assets/images/TWdeform.png' | relative_url }}" width="450">

The strains at the strain gauge location were __. This is also shown in the image below. 

<img src="{{ '/assets/images/TWstrainprobe.png' | relative_url }}" width="450"> 

Our FEM analysis showed a maximum strain (which occurs along the z axis as expected) of 1.2093*10-3 in/in, which is equal to 1209.4 microstrain, and a sensitivity of 1.209 mV/V. This is reasonably close to our calculated sensitivity of 1.17 mV/V, and is likely a little bit larger due to the fact that our code assumed that it could only deform axially, however that’s not entirely true in real life.

We have selected to use a double linear strain gauge, which is most commonly used to measure bending. It is 0.354” x 0.354” so it should have no trouble fitting on our torque wrench.