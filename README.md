# Map-My-World
Simultaneous Localization and Mapping(SLAM) of robot in an environment.

In this project, the robot creates a map of a dynamic environment using SLAM technique. 
The map of the environment and the number of loop closures can be seen with a software tool calledrtabmap viewer.
First, world.launch file present in launch folder of my_robot is launched in ROS. This launches the robot in gazebo and also opens the rviz.
Then teleop_twist_keybooard.py, a python file present in teleop_twist_keyboard folder is made to run in separate terminal. This will provide list of keys through which we can move the robot in gazebo in all the directions. It will also provide keys to vary the speeds.
To put in simpler terms, we are just adding manual controls to robot in gazebo.
Finally, mapping.launch file is launched in another terminal, which creates the rtab-map of the environment as the robot is operated manually through teleop_twist_keyboard in gazebo.
After operating the robot the process is stopped to check the output.
The mapping.launch file creates a database file rtabmap.db, which contains the information about the places the robot visited in the gazebo world and also the number of loop closures. 
The database file can be only viewed by rtabmap viewer.
We can see as the robot is moving in the dynamic environment, it will create a map of it using SLAM.

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

