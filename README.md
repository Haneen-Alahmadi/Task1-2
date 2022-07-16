# Task1

#Install ROS1 on ubuntu

1-Setup your sources.list:
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

2-Set up your keys:
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

3-Installation:
sudo apt update
sudo apt install ros-noetic-desktop-full

4-Environment setup
source /opt/ros/noetic/setup.bash

5-roscore
