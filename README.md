# MissionToMars-Swarmathon-PCC-CSPU


========= Installation guide for the Swarmathon_world with hector_quadrotor package =========

1. install all the supportive ROS package:
$cd [SwarmathonBoseCode-PCC-CPSU-directory]
$rosdep install --from-path src --ignore-src

2.build the workspace
$catkin build

======== set up the simulation world ==============================

once the rqt GUI is successfully loaded,
1. click to choose a saved world
2. from the list choose: five_homes_with_mars_ground.world
3. choose 4 rovers or any number
4. click on "build simulation"


========= How to control the hector quadrotor ====================

1/source the project
cd to the [SwarmathonBoseCode-PCC-CPSU-directory]
$source ~/[SwarmathonBoseCode-PCC-CPSU-directory]/devel/setup.bash

2/ turn on the server for control
$ ~/[SwarmathonBoseCode-PCC-CPSU-directory]/src/hector_quadrotor$ rosservice call /enable_motors "enable: true"

3/turn on the controlling command input environment
$~/[SwarmathonBoseCode-PCC-CPSU-directory]/src/hector_quadrotor$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py

