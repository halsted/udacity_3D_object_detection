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

Frame 29, Sequence 3, Lidar point-cloud in 3d viewer (Bird's Eye View)

![image](https://user-images.githubusercontent.com/7365421/192071478-39775195-4e3d-4ab6-a40a-908b49d0959a.png)

Frame 29, Sequence 3, Street perspective of lidar point-cloud

![image](https://user-images.githubusercontent.com/7365421/192071850-ec540a93-0a5d-4259-8f5e-f80d60c315ac.png)

In frame 29, the Waymo driver has passed many of the passed cars on the left side of the road, as seen in the BEV point-cloud. I can still see the bumper and tail-lights of the car in front of the Waymo Driver in the range image. The car appears to be travelling at about the same speed and staying the same distance ahead of the Waymo Driver. This car can also be seen in the lidar point-cloud as a cyan blob.

Frame 37, Sequence 3, Intensity channel of range image

![image](https://user-images.githubusercontent.com/7365421/192072283-d9a35664-c501-4fdc-94c0-a343d2361d3d.png)

Frame 37, Sequence 3, Zoomed view of Lidar point-cloud (BEV) 

![image](https://user-images.githubusercontent.com/7365421/192072436-9b4f08e7-62e2-40d7-b58a-93674ecc86c5.png)

Again, bumpers and tail-lights are distinguishing features in the range image. There are no distinguishable features from the lidar point-cloud.


