### Steps for now
- Source ros (I'm using Noetic)
- Clone this package into your catkin workspace
- Source the package
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

