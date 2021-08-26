# SMA-leader-follower

roscore

rosrun map_server map_server map.yaml

roslaunch amclmulti launch_gazebo.launch

for random robot location

./n_robot.sh

for specific location

roslaunch amclmulti turtle_multiple.launch multi_robot_name:=tb3_0 x_pos:=2.0 y_pos:=1.0

roslaunch amclmulti turtle_multiple.launch multi_robot_name:=tb3_1 x_pos:=2.0 y_pos:=0.0

roslaunch amclmulti turtle_multiple.launch multi_robot_name:=tb3_2 x_pos:=2.0 y_pos:=-1.0

on new terminal

rosrun amclmulti leader_follower_v2.py tb3_0 tb3_1 leader1

on another terminal

rosrun amclmulti leader_follower_v2.py tb3_1 tb3_2 leader2

on another terminal

ROS_NAMESPACE=tb3_0 rosrun turtlebot3_teleop turtlebot3_teleop_key
