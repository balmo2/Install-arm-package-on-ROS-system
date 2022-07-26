# Install-arm-package-on-ROS-system
### In this repository, we will mention the steps to install the robotic arm package and run it on the ROS system

#### Before starting, you must make sure that you have install ROS on ubnto using vertualbox, and then start by following these steps:
#### 
1 - first step is to install catkin package :
```
sudo apt-get install ros-noetic-catkin
```
2 - then create a workspace :
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
```
