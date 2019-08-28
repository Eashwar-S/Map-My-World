# Map-My-World
Simultaneous Localization and Mapping of robot in an environment.

In this project, the robot creates a map of a dynamic environment using SLAM technique. The map of the environment and the number of loop closures can be seen with rtabmap viewer. First, world.launch file present in launch folder of my_robot is launched in ROS. This launches the robot in gazebo an opens the rviz. Then teleop_twist_keybooard.py python file present in teleop_twist_keyboard folder is made to run in ROS. This makes the robot the robot to be operated manually. Finally, mapping.launch file is launched, which creates the rtab-map of the environment of the environment as the robot is operate manually through teleop_twist_keyboard in gazebo. After this, the process is eliminated. As the process is completed, the mapping.launch file creates a database file rtabmap.db, which contains the information about the places the robot visited in the gazebo world and also the numberof loop closure. The database file can be only viewed by rtabmap viewer.

Software Required:-
1. ROS
2. Gazebo
3. Rviz
4. Rtab-map viewer (Real time appearance based mapping)
5. Linux Operating System

Commands used:-

1. For launching gazebo and rviz (both present in world.launch)

roslaunch my_robot world.launch

2. For launching teleop_twist_keyboard

rosrun teleop_twist_keyboard teleop_twist_keyboard.py

3. For launching rtab-map 

roslaunch my_robot mapping.launch

