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
3 - now we will add the robot arm package in src folder :
```
cd ~/catkin_ws/src
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
4 - if everything is ok , we will install the dependencies :
```
cd ~/catkin_ws
rosdep install --from-paths src --ignore-src -r -y
sudo apt-get install ros-kinetic-moveit
sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui
sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher
sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
catkin_make
```
5 - Excellent, let's try if the install is correct
```
roslaunch robot_arm_pkg check_motors.launch
```
it will show this page 

<div>
<img src="https://user-images.githubusercontent.com/101142149/181014160-8f2daae1-fd2e-49ae-acf7-0d72a10cc972.jpg" width="400">
  </div>
  
  #### Now lat's install arduino IDE to see the actuall result 
  Follow the following steps :
  
  1 - Go to arduino Download page , then install the package :
  [downlod arduino](https://www.arduino.cc/en/software)
  then choose linux 64 (depend on your divase)
  
  2 - Now extract the file and place it on the home page , You can change the name or leave it .
  
 3 - Open your terminal and add this code :
 ```
 cd arduino 
 sudo ./install.sh
 ```
 4 - Then open a new terminal in arduino file and add this code to open the package :
 ```
 ./arduino
 ```
##### Great , now lat's install the library
