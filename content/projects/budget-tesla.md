---
title: "senior project"
description: "Budget Tesla: a semi-autonomous golf cart"
depth: 1
---

## Overview

Consisting of 5 members, Team Budget Tesla aimed to fully automate an electric golf cart.
The goal was to complete a prototype of a system that could taxi students around campus with a focus on the transportation of injured or disabled students.
We knew it was a bit too ambitious, but better to aim for the skies and scale down after research than to deliver a weak project.
An easy project would hardly teach us anything, after all.


Our 8 months of work culminated in a cart that could detect obstructions and hit the brakes; essentially a $700 brake assist system tacked on with duct tape and Tupperware.
An NVIDIA Jetson takes data from three input sensors (camera, radar, and GPS) and sends commands to the output sensors (braking).
Given the scale of the project, we were pleased with the work and could have a full prototype completed if given another semester.
We prioritized safety in our design and implementation, but had neither the time or resources to perform full safety testing.
As such, the cart is only a proof of concept and could not be deployed without rigorous checks to assure the safety of both passengers and pedestrians.

## My Role

My responsibilities bounced around as the year passed.
I started by researching software solutions for a queing/scheduling system, something students could use to call the cart for a pickup and ride.
As we downscaled the project and tossed this system aside, I ended up working on the A-to-B navigation system.
This consisted of a GPS chip that follows the cart along a route and a map of campus that plots this route according to the given start and end points.

The GPS chip was hooked up to a microcontroller, so I modified some code from TI's TivaWare library to enable USB communication with the Jetson.
This code was re-used for the other microcontrollers on the project.

I also worked on the administrative code.
This module, dubbed BT Admin, took data from the input sensors and gave commands to the output sensors.
A small script was made to help the other modules easily connect to the admin's Unix sockets.
The current implementation is a simple state machine that tells the brakes to trigger if any of the three input systems report negatively.

## Gallery



## Files

