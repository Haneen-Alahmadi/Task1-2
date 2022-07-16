#Task2

#Install ROS2

1-Set locale:
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings

2-Setup Sources:

apt-cache policy | grep universe

3- add the ROS 2 apt repository to your system:

sudo apt update && sudo apt install curl gnupg2 lsb-release

sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg

4-add the repository to your sources list:

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null

5-Install ROS 2 packages:
sudo apt update
sudo apt upgrade
sudo apt install ros-foxy-desktop
sudo apt install ros-foxy-ros-base

6-ros2 run 

7-Environment setup:
source /opt/ros/foxy/setup.bash

8-Source the setup file and then run a Python:
source /opt/ros/foxy/setup.bash
ros2 run demo_nodes_py listener
