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

In Frame 0, tail-lights and bumpers can be seen in the range image (intensity channel). There seems to be a line of parked cars on the left side of the road and a truck and car in the right lane, travelling in the same direction as the Waymo car. In the lidar point-cloud (LPC), the side-view mirrors of the vehicles can be detected as well as the shape of the vehicle.

### #2 - Frame 15
![image](https://user-images.githubusercontent.com/7365421/192373812-671051c9-3dd9-423a-a8ce-c0f3c6f07a37.png)
![image](https://user-images.githubusercontent.com/7365421/192374402-ddfbb74f-4801-4ce7-8c8b-4160721c7349.png)

In Frame 15, the same vehicles and the same features (tail-lights, bumpers and side-view mirrors) as in Frame 0 can be seen.

### #3 - Frame 30
![image](https://user-images.githubusercontent.com/7365421/192375796-60428906-a5ca-4e47-a9e1-8b2de4457d02.png)
![image](https://user-images.githubusercontent.com/7365421/192376225-1e66064f-92be-4210-9912-9d942b108938.png)

In Frame 30, the same features as in Frames 0 and 15 can be seen. The Waymo car has caught up to the truck and is in the process of passing it.

### #4 - Frame 45
![image](https://user-images.githubusercontent.com/7365421/192377170-50b66552-11c6-443d-88da-b453f34b711d.png)
![image](https://user-images.githubusercontent.com/7365421/192391589-95349503-036a-4edb-b7a8-1946cf80c003.png)

In Frame 45, the range image shows the side view of two cars, one on each side of the Waymo car. There are also two cars ahead of the Waymo car in the right lane. 

### #5 - Frame 60
![image](https://user-images.githubusercontent.com/7365421/192378149-5c5d0892-0f0c-4dfe-b606-7d04c050a68b.png)
![image](https://user-images.githubusercontent.com/7365421/192378436-ccebcab9-931f-4d58-bb5a-a1795c09d07a.png)

In Frame 60, there are two cars in the right lane ahead of the Waymo car. The range image clearly shows the tail-lights and bumpers. The LPC also shows these vehicles and shows the general shape of the vehicles. A car approaching on the left is also clearly visible in the LPC.

### #6 - Frame 75
![image](https://user-images.githubusercontent.com/7365421/192379793-99e8ae01-f795-4c1d-82d8-13024092fa08.png)
![image](https://user-images.githubusercontent.com/7365421/192380247-169c1e42-6094-45fd-b4f4-1fab41859546.png)

Frame 75 shows the same two vehicles in the right lane. There is a vehicle approaching on the left side of the road, but it appears to be a different vehicle from the one on Frame 60. The general vehicle shape can be seen in the LPC. 

### #7 - Frame 90
![image](https://user-images.githubusercontent.com/7365421/192380515-e9831f42-98e0-4876-95cd-16da371e040c.png)
![image](https://user-images.githubusercontent.com/7365421/192380991-3773ea92-9e83-4c81-a5b5-cd0dcb6cb9c3.png)

### #8 - Frame 105
![image](https://user-images.githubusercontent.com/7365421/192381324-6cf564bf-242d-4ea9-8964-fe2d63dd5a2e.png)
![image](https://user-images.githubusercontent.com/7365421/192392402-169be4b3-5888-4ce5-aec1-9ff917341508.png)

### #9 - Frame 120
![image](https://user-images.githubusercontent.com/7365421/192382151-141ec500-8e09-41fc-89e3-b3f31c6abad5.png)
![image](https://user-images.githubusercontent.com/7365421/192392766-02af1b90-b0d1-4e1d-8f16-fea98586f041.png)

In Frame 120, two vehicles can be seen in both the range image and the LPC. One vehicle is on the right, travelling in the same direction as the Waymo car and the other vehicle is on the left and is going the opposite direction from the Waymo car. The bumpers and tail-lights are visible in the range image.

### #10 - Frame 135
![image](https://user-images.githubusercontent.com/7365421/192382863-86f95347-cf21-4dcc-95f8-dd89a2999adf.png)
![image](https://user-images.githubusercontent.com/7365421/192393144-25161c05-a11a-41e0-85e9-30ae8fbbb554.png)

In Frame 135, two humans are visible in the distance to the left of the Waymo car. The people are visible in both the range image and the LPC. The vehicle in the right lane is also clearly visible.

### #11 - Frame 150
![image](https://user-images.githubusercontent.com/7365421/192383321-05692afc-c871-4956-9d64-9f0b16a43499.png)
![image](https://user-images.githubusercontent.com/7365421/192383568-28ce45fb-0098-4ad7-b261-b016248da018.png)

In Frame 150, the people and the car in the right lane are visible, as they were in Frame 135.

### #12 - Frame 165
![image](https://user-images.githubusercontent.com/7365421/192383789-7c6517e8-fa2a-4f9f-b8fd-3d0d17fe19c0.png)
![image](https://user-images.githubusercontent.com/7365421/192384048-7035caa6-0d80-4244-8fc1-b9ddcb4f0db4.png)

### #13 - Frame 180
![image](https://user-images.githubusercontent.com/7365421/192384685-ada6bb03-7dba-4db4-b9d4-b3e2ebcfd42d.png)
![image](https://user-images.githubusercontent.com/7365421/192384991-0bd29352-cc83-49c5-ade9-4bdf84f3decd.png)

### #14 - Frame 195
![image](https://user-images.githubusercontent.com/7365421/192385159-19008abd-27be-482c-9573-9fe8c4d68ef5.png)
![image](https://user-images.githubusercontent.com/7365421/192391362-b82e65b7-79ed-4619-96cf-28c519948fd3.png)

### Summary
The LPC shows 3D shapes that identify the shape of the vehicle. Often the side-view mirrow can be distinguished. The intensity channel of the range image shows tail-lights and bumpers quite well. The side-view of vehicles can also be seen clearly in the range image. Both the LPC and the range image contain valuable information that can be used for tracking vehicles, cyclists or pedestrians.

## Section 2: Create Birds-Eye View from Lidar PCL

### Convert sensor coordinates to BEV-map coordinates

![image](https://user-images.githubusercontent.com/7365421/192896591-70c32a62-3f81-40bc-8ee6-6449c307279d.png)

### Compute intensity layer of the BEV map
![image](https://user-images.githubusercontent.com/7365421/192897097-8a58604c-d31f-4618-ad94-75214e1fa883.png)

### Compute height layer of the BEV map
![image](https://user-images.githubusercontent.com/7365421/192897225-c8b1c194-7000-4f36-9507-2161d0c038dd.png)

## Section 3: Model-based Object Detection in BEV Image

Frame 50 (Model: fpn_resnet)

Detections =  [[9.7223872e-01 3.5127075e+02 2.1875238e+02 1.0574490e+00 1.6241086e+00 2.0172737e+01 4.7542793e+01 1.3822034e-02]
 [6.2091374e-01 3.1184229e+02 3.5521008e+02 1.1316251e+00 1.7765539e+00 2.0849136e+01 4.6748154e+01 8.4769009e-03]]

![image](https://user-images.githubusercontent.com/7365421/192911955-7fd8bd96-1f2c-46d5-9582-ee04e4cd8a4c.png)
![image](https://user-images.githubusercontent.com/7365421/192912025-d0dd1f36-06cc-431a-9664-8135d9353363.png)

Frame 51 (Model: fpn_resnet)

Detections =  [[ 9.0935498e-01  3.5153265e+02  2.1939409e+02  1.0489278e+00  1.6082902e+00  2.0308041e+01  4.8363377e+01  1.2367926e-02]
 [ 8.0556726e-01  3.1226596e+02  3.5451572e+02  1.1078370e+00 1.7661636e+00  2.0709120e+01  4.8925690e+01  6.6410162e-02]
 [ 7.8161055e-01  3.5299170e+02  6.0305402e+02  1.2087984e+00 1.6976428e+00  1.9822773e+01  5.0056713e+01 -3.2651678e-02]]
![image](https://user-images.githubusercontent.com/7365421/192912481-f8537f5f-8424-4758-9285-770169e87cd0.png)
![image](https://user-images.githubusercontent.com/7365421/192912556-f37d4636-bcd3-4de9-a148-be5755f76d54.png)

## Section 4: Performance Evaluation for Object Detection

### Compute intersection-over-union between labels and detections

Frame 50 (Model: darknet)

ious =  [0.8234376907650102, 0.8903358055776488, 0.8747769919519454]

center_devs =  [[tensor(0.1402), tensor(-0.0197), 1.0292643213596193], [tensor(-0.0818), tensor(0.0686), 0.8291298942401681], [tensor(0.0840), tensor(0.0247), 0.8929607095304846]]

Frame 51 (Model: darknet)

ious =  [0.8151514220492396, 0.8872181822459977, 0.846240903597746]

center_devs =  [[tensor(0.1476), tensor(0.0107), 0.9899635729132115], [tensor(-0.0901), tensor(0.0576), 0.8152483974641882], [tensor(0.0823), tensor(-0.0027), 0.8711946193956237]]

### Compute precision and recall
configs_det.use_labels_as_objects = False # True = use groundtruth labels as objects, False = use model-based detection

using darknet

Loaded weights from /home/workspace/tools/objdet_models/darknet/pretrained/complex_yolov4_mse_loss.pth

p =  306 tp =  289 fn =  17 fp =  15

precision = 0.9506578947368421, recall = 0.9444444444444444

![image](https://user-images.githubusercontent.com/7365421/192907413-b9caa972-b8ef-4ef6-8cd1-5289d3b83535.png)

configs_det.use_labels_as_objects = True # True = use groundtruth labels as objects, False = use model-based detection

using darknet

Loaded weights from /home/workspace/tools/objdet_models/darknet/pretrained/complex_yolov4_mse_loss.pth

p =  306 tp =  306 fn =  0 fp =  0

precision = 1.0, recall = 1.0

![image](https://user-images.githubusercontent.com/7365421/192908171-5ff37a0f-09e0-4221-b99d-5cdadca01f37.png)
