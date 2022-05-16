# mechanical_arm_final
> **notice**：These files have not been secondary confirmed！I can only be sure that they can work properly in my environment, which is ubuntu 18.04 melodic + gazebo9

In this version, the robot arm can recognize and clip the target
Run the program and add the target.Note that  you should add the target(orange cube) by yourself.

after git clone the files at catkin_ws/src  and caktin_make, you can
```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ roslaunch arm1 gazebo.launch
```
run the image processing node.
For program logic reasons,the image processing node should be run first.
Otherwise, the program will not run.
```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ rosrun arm1 image_process
```
run the logical controller node.
```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ rosrun arm1 arm_command
```
View the rgb-camera topic
```
rqt_image_view /rgb_camera/image_raw
```
