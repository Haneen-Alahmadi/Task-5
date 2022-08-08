# Task-5


USE TURTLEBOT3 WITH SLAM APPROACH TO CREATE AND SAVE A MAP

cd catkin_ws

source devel/setup.bash

export TURTLEBOT3_MODEL=waffle_pi

roslaunch turtlebot3_gazebo turtlebot3_world.launch

#waiting
#open another terminal

source devel/setup.bash

export TURTLEBOT3_MODEL=waffle_pi

roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methodes:=gmapping

#waiting
#open thid terminal 

source devel/setup.bash

export TURTLEBOT3_MODEL=waffle_pi

roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

#waiting,don't close the terminal
#open fourth terminal 

source devel/setup.bash

export TURTLEBOT3_MODEL=waffle_pi

rosrun map_server map_server -f ~/map

#now we will back to third terminal and close it if done.

#then we will back to second terminal and close it if done.

#Gazebo active now

#In last terminal

source devel/setup.bash

export TURTLEBOT3_MODEL=waffle_pi

rroslaunch turtlebot3_navigation turtlebot3_nanigation.launch map_file:=$HOME/map.yaml

#RVIZ active now
#we will click on (2D pose Estimate ,then 2D nav Goal)


