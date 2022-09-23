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

![image](https://user-images.githubusercontent.com/7365421/192069556-0e730843-412d-4143-93ee-a4df827c238a.png)


![image](https://user-images.githubusercontent.com/7365421/192067657-461d71ef-89a2-4924-b8c9-0250cf5317ab.png)

Frame 1, Sequence 3, Lidar point-cloud in 3d viewer

![image](https://user-images.githubusercontent.com/7365421/192068776-909c83aa-3a1a-4633-addd-b37bbc62d69f.png)

In Frame 1, the two cars ahead of the Waymo Driver are visible in both the lidar point-cloud and the intensity channel of the range image. 
