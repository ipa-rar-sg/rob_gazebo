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
    sudo apt install ros-$ROS_DISTRO-slam-gmapping
```
- Source your catkin environment
- To see the world, just launch:
```bash
    roslaunch rob_gazebo rob.launch
```
- To operate the turtlebot, launch in another terminal (also with the model env variable, and sourced ros and workspace):
```bash
    roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
#### Running Simulation
##### Running steps
- Check the sim.launch file for the possible arguments, and modify them if required (or specify them at launch time)
- Just launch sim.launch
```bash
    roslaunch rob_gazebo sim.launch
```

#### Running neo_simulation
- Check the following [Neobotix - Starting with simulation](https://neobotix-docs.de/ros/ros1/simulation.html)
- In the neo_simulation package, in the file simulation.launch, set the map for your desired map, and same for the launching arguments.
```bash
    roslaunch neo_simulation simulation.launch
```

### Useful important links
- [Gazebo plugins in ROS](https://classic.gazebosim.org/tutorials?tut=ros_gzplugins&cat=connect_ros#Tutorial:UsingGazebopluginswithROS)
- [URDF tutorials](https://wiki.ros.org/urdf/Tutorials)
- [Gazebo Ros Demos - Github Repo](https://github.com/ros-simulation/gazebo_ros_demos)

