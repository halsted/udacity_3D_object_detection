# udacity_3D_object_detection

## Section 1: Compute Lidar Point-Cloud from Range Image

### Visualize range image channels

In this section, I wrote the code for the function show_range_image in objdet_pcl.py to visualize range image channels. The images below are the combined "range" and "intensity" channels within the range image.

Here is the range image for frame 0 of Sequence 1:

![image](https://user-images.githubusercontent.com/7365421/192066053-ba1f38c2-9d84-468b-bb80-906da45bed99.png)

Here is the range image for frame 1 of Sequence 1:

![image](https://user-images.githubusercontent.com/7365421/192066536-d3c6384f-3862-4f45-b26b-adc855db06f7.png)

### Visualize lidar point-cloud

Frame 1, Sequence 3, Intensity channel of range image

![image](https://user-images.githubusercontent.com/7365421/192069829-36fe9c20-b972-4b15-a1f5-9d49ed9d2664.png)

Frame 1, Sequence 3, Lidar point-cloud in 3d viewer

![image](https://user-images.githubusercontent.com/7365421/192069653-6b16ec9d-7c2e-4df1-8c12-0b54fcb6fea7.png)

In Frame 1, I can see a line of parked cars on the left of the range image and also in the lidar point-cloud as a sequence of cyan rectangles. In the range image, I can see the rear bumper and tail-lights of several cars in front of the Waymo Driver. It seems that two separate cars from the range image are a single blob in the lidar point-cloud. Here is a 3d rotated view of the same lidar point-cloud.

![image](https://user-images.githubusercontent.com/7365421/192070860-662d20dc-b468-4cf9-9a23-8ab03882b68f.png)

Frame 29, Sequence 3, Intensity channel of range image

![image](https://user-images.githubusercontent.com/7365421/192071381-7bd010ec-af40-43be-9663-39e5a45c8f3e.png)
