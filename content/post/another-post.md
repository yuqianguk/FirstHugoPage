---
title: "Speed Test for YOLOv3 in C++/Python"
date: 2020-03-30
tags: []
---

In this post, we will measure and compare the speed of YoloV3 running on Darknet and OpenCV in both python and C++.

Here is the configuration of the test system we used.

* Machine : Intel I7-8550U. This machine has 4 vCPUs and 16 GB of RAM, but no GPU.

* Operating System : Windows 10 Pro.

* OpenCV version : 4.2.0

* Testing methodology : Run YoloV3 custom weight file to detect the same object in a video and measure how long it take to run.

## Using YOLOv3 with OpenCV ( Python )

The following gif file shows the performance of YOLOv3 on Darknet running python. It is not surprising the CPU version of Darknet can only achive 6 FPS. This is becasue Darknet is written in C, and it does not officially support Python. 

As you can see, It took 116 seconds to process the video.
![hugo logo](/img/python.gif) 


## Using YOLOv3 with OpenCV ( C++ )
Let us now see how to use YOLOv3 in OpenCV with C++ to perform object detection. It is not suprising that Darknet with OpenCV in C++ works much better than Darknet in Python even with OpenCv enable.

It took 24 seconds to process the same video.
![hugo logo](/img/cplusplus.gif) 


## Consultion.

In this test, the C++ YoloV3 CPU version is nearly 5x faster than python.