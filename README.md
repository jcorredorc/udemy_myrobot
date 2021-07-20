# udacity_myrobot

This repo contains the autor's solution to the projects proposed in the course [Robotics Software Engineer Nanodegree Program](https://www.udacity.com/course/robotics-software-engineer--nd209). The package is tested in ROS Kinect.

## Installation

### Project 4. Where I Am

Make sure you have the following packages installed

```
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ sudo apt-get install ros-kinetic-amcl
```

Clone the repositories and build it in your workspace folder /src

```
git clone https://github.com/ros-teleop/teleop_twist_keyboard
git clone --depth 1 --branch Prj4.WhereIAm https://github.com/jcorredorc/udacity_myrobot.git
```

### Project 5. Map my World

Install,

```
sudo apt-get install ros-kinetic-rtabmap-ros
```
and install teleop_twist_keyboard.

## Usage

### Project 4. Where I Am

```
roslaunch my_robot world.launch
roslaunch my_robot amcl.launch
```

Now you could run the teleop script to test the localization via amcl package

```
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

Or you can use the 2D Navigation Goal tool from Rviz


![Localization](/images/xdp_imagenUdacity_proj3.jpg)


### Project 5.  Map my World

```
roslaunch my_robot world.launch
roslaunch my_robot mapping.launch
```

Run the teleop script to map the world

```
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

check the map in `/root/.ros/` folder, and open it with,

```
rtabmap-databaseViewer ~/.ros/rtabmap.db
```

[The rtabmap file is available here](https://drive.google.com/file/d/1QIIlQ-HIItu1ZlnsEeybUykcX_YJBXKK/view?usp=sharing)


![Mapping_rtabmap](/images/mapping01_tool.png)


