# ROS installation

Reference: [ROS wiki - Installation](http://wiki.ros.org/noetic/Installation/Ubuntu)



### Setup sources & keys

```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```



### Installation

```bash
sudo apt update
sudo apt install ros-noetic-desktop-full
```



### Environment setup

```bash
source /opt/ros/noetic/setup.bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```



### Dependencies for building packages

```bash
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```



### Initialize rosdep

```bash
sudo rosdep init
rosdep update
```



### Create a ROS Workspace

```bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
```



