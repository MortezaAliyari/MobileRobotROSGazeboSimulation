# MobileRobotROSGazeboSimulation
This repo relate to a real robot which design in Gazebo and controlled by Gazebo and ROS plugins. 
[Also you can follow me on linkdin page](www.linkedin.com/in/morteza-aliyari-1609a1107)
---
If you like the project give me a star! :star: 

You can see the video: &nbsp;&nbsp;
[![website](./img/youtube-dark.svg)](https://www.youtube.com/watch?v=XaLbEKf8UhA)
&nbsp;&nbsp;
---

### The requirements of this project are :
- Ubuntu Focal 
- ROS Noetic
- GAzebo 11

------------------------------------------------------------------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
This project is related to a real Two-Wheeled Mobile Robot but at the first step, it was designed at Gazebo Environment. This project will help you explore features and tools provided by ROS (Robot Operating System). We start building the robot from the scratch, using URDF (Unified Robot Description Format) and RViz to visualize it. Further, we describe the inertia and show how to simplify the URDF using XACROS. Later, motion planning algorithms, such as Obstacle Avoidance and robot_localization methods will be used to create a map in order to path planning the robot to our goal point.
Here's what you will accomplish in this tutorial:
- [x] Build your own robot from scratch
- [x] Add Lidar and IMU sensors to the Robot
- [x] Create your own map or building in Gazebo11
- [x] Work with Topics and related commands
- [x] Work with RVIZ environmnet 
- [x] Create MAP of your envirnment with Gmapping Method
- [x] Find optimal path from your robot position to goal point
### Install 
---
```
source /opt/ros/noetic/setup.bash
cd catkin_ws
wget https://gist.githubusercontent.com/airuchen/5e58eb5dc54d6dc38ea5d2bedd53f69e/raw/ae3b850aca5a0577105c682eec1ab3b534161cc2/multi_omnibot.repos
catkin_make
source devel/setup.bash
```
 Open terminal then type blow commands:
 
 ```
roslaunch turtlebot3_gazebo Multi_turtlebot3_Closeworld2.launch
```

If you haven't seen error the Gazebo environment should launch. Then type below command:

![Gazebo Environment](./img/gazebo.PNG)

 ```
roslaunch turtlebot3_navigation multi_turtlebot3_navigation.launch
```

![RVIZ Environment](./img/rviz.PNG)
Then click right on "2D nav Goal"  and add "Tool Properties" as new panel to RVIZ.
Then you can change the 2D nav Goal topic to "/tb3_1/move_base_simple/goal" or "/tb3_2/move_base_simple/goal" like below picture:

![RVIZ Environment](./img/2dnav.PNG)
