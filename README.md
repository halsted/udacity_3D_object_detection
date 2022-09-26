# udacity_3D_object_detection

## Section 1: Compute Lidar Point-Cloud from Range Image

### Visualize range image channels

In this section, I wrote the code for the function show_range_image in objdet_pcl.py to visualize range image channels. The images below are the combined "range" and "intensity" channels within the range image.

Here is the range image for frame 0 of Sequence 1:

![image](https://user-images.githubusercontent.com/7365421/192066053-ba1f38c2-9d84-468b-bb80-906da45bed99.png)

Here is the range image for frame 1 of Sequence 1:

![image](https://user-images.githubusercontent.com/7365421/192066536-d3c6384f-3862-4f45-b26b-adc855db06f7.png)

### Visualize lidar point-cloud

#### Find 10 examples of vehicles with varying degrees of visibility in the point-cloud

### #1 - Frame 0
![image](https://user-images.githubusercontent.com/7365421/192372536-a503f0cb-f7f2-4443-9c34-949a551ea62a.png)
![image](https://user-images.githubusercontent.com/7365421/192373313-651b389e-ce41-400f-960c-019586bf1d28.png)

### #2 - Frame 15
![image](https://user-images.githubusercontent.com/7365421/192373812-671051c9-3dd9-423a-a8ce-c0f3c6f07a37.png)
![image](https://user-images.githubusercontent.com/7365421/192374402-ddfbb74f-4801-4ce7-8c8b-4160721c7349.png)

### #3 - Frame 30
![image](https://user-images.githubusercontent.com/7365421/192375796-60428906-a5ca-4e47-a9e1-8b2de4457d02.png)
![image](https://user-images.githubusercontent.com/7365421/192376225-1e66064f-92be-4210-9912-9d942b108938.png)

### #4 - Frame 45
![image](https://user-images.githubusercontent.com/7365421/192377170-50b66552-11c6-443d-88da-b453f34b711d.png)
![image](https://user-images.githubusercontent.com/7365421/192377875-be952fae-2ce1-494b-b7fe-314a65065346.png)

### #5 - Frame 60
![image](https://user-images.githubusercontent.com/7365421/192378149-5c5d0892-0f0c-4dfe-b606-7d04c050a68b.png)
![image](https://user-images.githubusercontent.com/7365421/192378436-ccebcab9-931f-4d58-bb5a-a1795c09d07a.png)

### #6 - Frame 75
![image](https://user-images.githubusercontent.com/7365421/192379793-99e8ae01-f795-4c1d-82d8-13024092fa08.png)
![image](https://user-images.githubusercontent.com/7365421/192380247-169c1e42-6094-45fd-b4f4-1fab41859546.png)

### #7 - Frame 90
![image](https://user-images.githubusercontent.com/7365421/192380515-e9831f42-98e0-4876-95cd-16da371e040c.png)
![image](https://user-images.githubusercontent.com/7365421/192380991-3773ea92-9e83-4c81-a5b5-cd0dcb6cb9c3.png)

### #8 - Frame 105
![image](https://user-images.githubusercontent.com/7365421/192381324-6cf564bf-242d-4ea9-8964-fe2d63dd5a2e.png)
![image](https://user-images.githubusercontent.com/7365421/192381936-2a5c3e39-357c-400c-a96f-aa468daebae6.png)

### #9 - Frame 120
![image](https://user-images.githubusercontent.com/7365421/192382151-141ec500-8e09-41fc-89e3-b3f31c6abad5.png)
![image](https://user-images.githubusercontent.com/7365421/192382648-1b61b54a-1c05-4e35-899e-f0e40f71f3a4.png)

### #10 - Frame 135
![image](https://user-images.githubusercontent.com/7365421/192382863-86f95347-cf21-4dcc-95f8-dd89a2999adf.png)
![image](https://user-images.githubusercontent.com/7365421/192383117-6991c1f6-fc7c-4bad-ae56-3707ba397c3c.png)

### #11 - Frame 150
![image](https://user-images.githubusercontent.com/7365421/192383321-05692afc-c871-4956-9d64-9f0b16a43499.png)
![image](https://user-images.githubusercontent.com/7365421/192383568-28ce45fb-0098-4ad7-b261-b016248da018.png)

### #12 - Frame 165
![image](https://user-images.githubusercontent.com/7365421/192383789-7c6517e8-fa2a-4f9f-b8fd-3d0d17fe19c0.png)
![image](https://user-images.githubusercontent.com/7365421/192384048-7035caa6-0d80-4244-8fc1-b9ddcb4f0db4.png)

### #13 - Frame 180
![image](https://user-images.githubusercontent.com/7365421/192384685-ada6bb03-7dba-4db4-b9d4-b3e2ebcfd42d.png)
![image](https://user-images.githubusercontent.com/7365421/192384991-0bd29352-cc83-49c5-ade9-4bdf84f3decd.png)

### #14 - Frame 195
![image](https://user-images.githubusercontent.com/7365421/192385159-19008abd-27be-482c-9573-9fe8c4d68ef5.png)
![image](https://user-images.githubusercontent.com/7365421/192385475-426a03a7-7544-4e14-a4bf-869a071f8946.png)

### Analysis


