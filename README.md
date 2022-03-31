# Mavis-Server

A reimplementation of SlimeVR's server/UI application to do body tracking in a different way.

## Pose and positioning algorithm

The algorithm will attempt to create a full table of values (x/y/z/pitch/yaw/roll) for all tracking points, regardless of which hardware trackers are actually equipped. We fill in this table in the following order:

- Collection of hardware sensor data
- OpenCV person detection using a webcam
- Tensorflow machine learning program that fills in the gaps, where data from the above two sources is used as the dataset

## C4 Diagrams

### Overview of the old software system:

![An overview of the old software system](design/C4-old-SlimeVR.png)

### Overview of the proposed software system:

![An overview of the proposed software system](design/C4-new-SlimeVR.png)

