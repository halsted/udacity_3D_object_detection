# udacity_3D_object_detection

## Section 1: Compute Lida Point-Cloud from Range Image

In this section, I wrote the code for show_range_image in the file objdet_pcl.py. I made the following code changes in loop_over_dataset.py:

data_filename = 'training_segment-1005081002024129653_5313_150_5333_150_with_camera_labels.tfrecord' # Sequence 1

show_only_frames = [0, 1] # show only frames in interval for debugging

sequence = "1"

exec_visualization = ['show_range_image'] # options are 'show_range_image', 'show_bev', 'show_pcl', 'show_labels_in_image', 'show_objects_and_labels_in_bev', 'show_objects_in_bev_labels_in_camera', 'show_tracks', 'show_detection_performance', 'make_tracking_movie'

Here is the range image for frame 0:

![image](https://user-images.githubusercontent.com/7365421/192066053-ba1f38c2-9d84-468b-bb80-906da45bed99.png)

Here is the range image for frame 1:

![image](https://user-images.githubusercontent.com/7365421/192066536-d3c6384f-3862-4f45-b26b-adc855db06f7.png)
