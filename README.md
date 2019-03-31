# Description  
Reference git is master branch of https://bitbucket.org/theconstructcore/turtlebot.git.   
I modify some code to operate turtlebot at kinetic and melodic.  
I remove turtlebot/turtlebot_rtab/models_original/demo_mapping.bag. The file size is so large.  
I check only Gazebo Simulation , teleop operation , depth data, rgb data and lidar.  

# Run On Melodic
*Download & Build  
```bash
$git clone https://github.com/AuTURBO/turtlebot.git
$sudo apt-get install ros-melodic-pid
$cd ~/catkin_ws && catkin_make
$sb
$rospack profile
```
*Empty World on navigation package   
```bash
$roslaunch turtlebot_navigation_gazebo main.launch 
$roslaunch turtlebot_teleop keyboard_teleop.launch
$rviz
```
*Cafe World on navigation package  
It takes more than 10 minutes to download the Gazebo Cafe Model at first run.
```bash
$roslaunch turtlebot_navigation_gazebo main2.launch 
$roslaunch turtlebot_teleop keyboard_teleop.launch
$rviz
```
*Empty World on turtlebot_rtab package   
```bash
$roslaunch turtlebot_rtab main.launch 
$roslaunch turtlebot_teleop keyboard_teleop.launch
$rviz
```
*costa_coffee_mod World on turtlebot_rtab package  
It takes more than 10 minutes to download the Gazebo Cafe Model at first run.
```bash
$roslaunch turtlebot_rtab main2.launch 
$roslaunch turtlebot_teleop keyboard_teleop.launch
$rviz
```
# Run On Kinetic
*Download & Build  
```bash
$git clone https://github.com/AuTURBO/turtlebot.git
$sudo apt-get install ros-kinect-pid
$cd ~/catkin_ws && catkin_make
$sb
$rospack profile
```
*Empty World  
```bash
$roslaunch turtlebot_navigation_gazebo main.launch 
$roslaunch turtlebot_teleop keyboard_teleop.launch
$rviz
```
*Cafe World  
It takes more than 10 minutes to download the Gazebo Cafe Model at first run.
```bash
$roslaunch turtlebot_navigation_gazebo main2.launch 
$roslaunch turtlebot_teleop keyboard_teleop.launch 
$rviz
```

# Image Shot  
*Cafe World  
<img src="/picture/1.png" width="70%" height="70%">  
*costa_coffee_mod World  
<img src="/picture/2.png" width="70%" height="70%">  
*empty World  
<img src="/picture/3.png" width="70%" height="70%">  
