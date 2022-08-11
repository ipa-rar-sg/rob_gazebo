### Steps for now
- Source ros (I'm using Noetic)
- Clone this package into your catkin workspace
```bash
    git clone git@github.com:ipa-rar-sg/rob_gazebo.git
```
- Clone further required packages into your catkin workspace and still further dependencies ([Neobotix Simulation Packages](https://neobotix-docs.de/ros/ros1/installation.html#packages-for-simulation))
```bash
    git clone https://github.com/neobotix/neo_simulation.git
    git clone https://github.com/neobotix/neo_kinematics_omnidrive
    git clone https://github.com/neobotix/neo_msgs.git
    git clone https://github.com/neobotix/neo_srvs.git
    git clone https://github.com/neobotix/neo_common.git
    sudo apt-get install ros-$ROS_DISTRO-ros-controllers
    sudo apt-get install ros-$ROS_DISTRO-gazebo-ros-control
    sudo apt-get install ros-$ROS_DISTRO-navigation
    sudo apt-get install ros-$ROS_DISTRO-joy
    sudo apt-get install ros-$ROS_DISTRO-teleop-twist-keyboard
```
- Source your catkin environment
- For now, testing with Turtlebot3, export your env variable with the model:
```bash
    export TURTLEBOT3_MODEL=burger
```
- To see the world, just launch:
```bash
    roslaunch rob_gazebo rob.launch
```
- To operate the turtlebot, launch in another terminal (also with the model env variable, and sourced ros and workspace):
```bash
    roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
#### SLAM with Turtlebot3
##### Requirements
- Turtlebot3 and gmapping
```bash
    sudo apt install ros-noetic-turtlebot3 ros-noetic-slam-gmapping
```
##### Running steps
- Launch the slam module and then operate from the teleop terminal commands
```bash
    roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```
- To save the map:
```bash
    rosrun map_server map_saver -f "file_name_and_path_here"
```

### Useful important links
- [Gazebo plugins in ROS](https://classic.gazebosim.org/tutorials?tut=ros_gzplugins&cat=connect_ros#Tutorial:UsingGazebopluginswithROS)
- [URDF tutorials](https://wiki.ros.org/urdf/Tutorials)
- [Gazebo Ros Demos - Github Repo](https://github.com/ros-simulation/gazebo_ros_demos)

