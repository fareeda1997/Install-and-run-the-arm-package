# Install-and-run-the-arm-package


# First: I downloaded and installed the Virtual Box and Ubuntu 16.

I used Ubuntu 16 because version 18 was not able to install it on the computer, so I used version 16, and of course, because I have version 16, I used (Kinetic) instead of (Melodic).

# Second: I wrote these commands as shown below on the terminal .

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

apt-cache search ros-kinetic

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update

sudo apt-get install ros-noetic-catkin

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm.git 

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-kinetic-moveit

sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control


# Here I opened another window for the terminal and wrote the last steps :

I wrote this:
    Source /home/fareeda/catkin_ws/devel/setup.bash
Inside a file named (bashrc) by typing the command:
   sudo nano ~/.bashrc
   
**bashrc is a file to run internal programs in Ubuntu**


sudo nano ~/.bashrc


 source /home/fareeda/catkin_ws/devel/setup.bash

source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch
 
