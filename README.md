# Download & Build On Melodic   
```bash
$sudo apt-get install ros-melodic-rtabmap ros-melodic-rtabmap-ros
$sudo apt-get remove ros-melodic-rtabmap ros-melodic-rtabmap-ros
```
```bash
$cd ~
$git clone https://github.com/introlab/rtabmap.git rtabmap 
$cd rtabmap/build
$cmake ..
$make 
$sudo make install
```
```bash
$cs
$git clone https://github.com/introlab/rtabmap_ros.git
$cm
$sb
$rospack profile
```
```bash
$git clone https://github.com/AuTURBO/turtlebot.git
$git clone https://github.com/JustWon/my_turtlebot_simulator.git
$git clone -b master https://github.com/turtlebot/turtlebot_create.git
$sudo apt-get install ros-melodic-pid 
$cd ~/catkin_ws && catkin_make
$sb
$rospack profile
```
# Modyfie code   
해당 파일의 아래 부분을 주석 처리해주세요. melodic에서 nodelet 돌리면 동작을 안함.   
애러 안나는 분은 삭제하지 마세요 이게 있어야 맨 마지막 예제도 도는것 같음.   
~/catkin_ws/src/my_turtlebot_simulator/turtlebot_gazebo/launch/includes/kobuki.launch.xml   
```bash
  <!--<node pkg="nodelet" type="nodelet" name="mobile_base_nodelet_manager" args="manager"/>
  <node pkg="nodelet" type="nodelet" name="cmd_vel_mux"
        args="load yocs_cmd_vel_mux/CmdVelMuxNodelet mobile_base_nodelet_manager">
    <param name="yaml_cfg_file" value="$(find turtlebot_bringup)/param/mux.yaml"/>
    <remap from="cmd_vel_mux/output" to="mobile_base/commands/velocity"/>
  </node>-->
```

# Run On Melodic

```bash
$roslaunch turtlebot_gazebo turtlebot_world.launch world_file:=/home/hyunoklee/catkin_ws/src/my_turtlebot_simulator/turtlebot_gazebo/worlds/empty.world
$roslaunch rtabmap_ros demo_turtlebot_mapping.launch simulation:=true
$roslaunch rtabmap_ros demo_turtlebot_rviz.launch
$roslaunch turtlebot_teleop keyboard_teleop.launch
```
It takes more than 10 minutes to download the Gazebo Wall Model at first run.
```bash
$roslaunch turtlebot_gazebo turtlebot_world.launch world_file:=/home/hyunoklee/catkin_ws/src/turtlebot/turtlebot_navigation_gazebo/worlds/empty.world
$roslaunch rtabmap_ros demo_turtlebot_mapping.launch simulation:=true
$roslaunch rtabmap_ros demo_turtlebot_rviz.launch
$roslaunch turtlebot_teleop keyboard_teleop.launch
```

