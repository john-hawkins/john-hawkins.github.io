---
title: "Estimating Gaze Duration Error from Eye Tracking Data"
collection: talks
type: "Talk"
permalink: /talks/2023-03-25-Estimating-Gaze-Duration-Error-from-Eye-Tracking-Data
venue: "MLHMI 2023 - Paper Presentation."
date: 2023-03-25
location: "Singapore"
---


Eye tracking applications produce a series of gaze fixation points that can be attributed to
objects within a subject's field of vision. Error is typically measured on the basis of individual
gaze fixation point measurements. These applications are often used to infer a gaze duration
metric from a series of fixation measurements. There is no direct method for infering the error in
a gaze duration measurement from an error in fixation points.

In this work we develop an algorithm for estimating
the error distribution of gaze duration measurement through monte carlo simulation
using the content of an eye tracking calibration log file.
We provide this algorithm in an open source application
to allow researchers to understand the error in their gaze duration measurements.
We use this application to conduct experiments on the expected error bounds for different duration
measurements across a fixed session length for a simulated advertising area of interest
study on a mobile device.
The results indicate that error in gaze duration estimation is sensitive to
fixation error beyond a bound that will depend on the size of interest and the session length.

http://www.mlhmi.org/2023.html

