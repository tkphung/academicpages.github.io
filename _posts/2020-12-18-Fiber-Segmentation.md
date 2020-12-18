---
title: 'Fiber Segmentation'
date: 2012-12-18
permalink: /posts/2020/12/Fiber-Segmentation/
tags:
  - Image Processing
  - MATLAB
---

Fiber Segmentation in MATLAB
======

I was recently automating segmentation of stress fibers laid down by epithelial cells in a cell culture. We were interested in quantifying the lengths of the stress fibers- in particular, how they change with different treatment conditions. Implementing an automated segmentation method would allow for batch processing of the data as well as removal of potential manual segmentation bias.

I developed the segmentation code in MATLAB by *Frankensteining* methods from two published stress fiber segmentation methods developed by [Rogge+ 2017](https://doi.org/10.1111/jmi.12593) and [Zhang+ 2017](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1684-y).  

Briefly, I implemented a fiber tracing algorithm from by [Rogge+ 2017](https://doi.org/10.1111/jmi.12593) to segment a pool of stress fiber fragments. Then, I implemented a fragment pairing algorithm based on [Zhang+ 2017](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-017-1684-y) to connect longer fibers. The segmentation function `segmentfibers.m` is available on the repository [SegmentFibers](https://github.com/tkphung/SegmentFibers).


Creating Synthetic Fiber Images
------

To test the segmentation algorithm, we generated synthetic stress fiber images with known fiber *lengths* and *widths* that are randomly aligned. To mimic stress fiber data, we included an option for generating locally aligned fibers. The code `Generate_FiberImage.m` in the [repository](https://github.com/tkphung/SegmentFibers) also provides options to adjust the image size and resolution.

Two sample images are shown below:
* **"DUAAD"** includes 1000 fibers with locally aligned regions
* **"SBXIQ"** includes 1000 fibers with random alignment

![segmentation example](https://raw.githubusercontent.com/tkphung/SegmentFibers/master/SegmentationExample.png)