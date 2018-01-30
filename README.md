# Approach1_DeepLearning
# 3D_Object_Seg_CNN
3D object segmentation using parameter estimation. 

Step 1)
Please run this file if you want the data:
1)run 'get_data.sh '

Step 2)
Please add the labels you want to train for in shapenet10.py file.

Step 3)
Train the mode, sun shape_3d_cnn.py
This will save the model with the name 'small_dataset.h5'
This may take a while depending on your system.

Step 4)
Please run test_one.py, and give the location of the saved point cloud.
Test the trained model with point cloud saved on the system.

 - data_shapes_3d_cnn.py : Does data parsing and saves them in numpy format.
 - volumetric_data contains few sample of the data
 - environment.yml/.json has is 'conda env export' saved files, has the configration of 
   conda on which these files were tested.

For PCL + ROS code : 

Step 1) Create a catkin workspace in ROS (http://wiki.ros.org/catkin/Tutorials/create_a_workspace). Copy the folder in 'camera code' in 'src' folder

Step 2) run 'catkin_make', plugin the camera, check  with 'lsusb' command if system can detect it

Step 3) run 'roslaunch camera_driver.launch'

Step 4) run 'rviz rviz -f /royale_camera_link'

Step 5) run 'rosrun pico_flexx_pcl plane_segmentation'

Step 6) Add PointCloud2 in Rviz, you should see a segmented point cloud of scene. Similar to : https://youtu.be/-TN0paktmRQ

