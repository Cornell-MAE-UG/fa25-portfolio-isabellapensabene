---
layout: project
title: System Analysis and Animation
description: System Analysis and Animation
technologies: [MATLAB]
image: /assets/images/SystemsMATLABss.png
---

I created an animation of the sailboat which shows the sailboat’s movement and heading relative to the X-axis. The variables available to control include the controller gains, Kpc and Kdc, the initial heading of the boat, initial angular velocity of the boat, the reference input heading, and a constant velocity with which the boat will be traveling. After all of the initial inputs, the script calls the ODE to retrieve the heading and rotational velocity values for the boat throughout the time range [0s, 120s]. Then, it draws the shape of the boat and its sail and makes them into patch objects so they can be more easily moved around and rotated throughout the animation. The animation loop uses the theta values obtained from the ODE to construct a rotation matrix, which is used to rotate the boat and sail. The new positions of these objects are also updated based on the speed and direction of travel. The title is updated to display the time elapsed since the beginning of the boat’s travel and its heading/angle of travel relative to the x-axis.

[Sailboat Animation Video](https://drive.google.com/file/d/1QwL0y0bT1wxmcWsLCj_QUwKfntXd6zuN/view?usp=drive_link)