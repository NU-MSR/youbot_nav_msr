Introduction
============

This is a simple demo of the
[ROS navigation "stack"](http://wiki.ros.org/navigation) running on the
[KUKA youBot](http://www.kuka-labs.com/en/service_robotics/research_education/youbot/).
The demo uses a
[Hokuyo URG-04LX-UG01](http://www.hokuyo-aut.jp/02sensor/07scanner/download/products/urg-04lx-ug01/)
laser scanner and the [hokuyo_node](http://wiki.ros.org/hokuyo_node) ROS package
for obtaining laser scan data used in detecting obstacles. The demo uses the
[eband_local_planner](http://wiki.ros.org/eband_local_planner) for a local
planner, and the
[youbot_driver_ros_interface](https://github.com/youbot/youbot_driver_ros_interface)
for controlling the youBot and providing odometry information.


Running the Demo
================

The youBot must be powered on, and the motors must have power. Then we simply
need to launch the main launch file using

```bash
roslaunch youbot_nav_msr move_base_eband.launch
```

If there are no errors, then we start `rviz` to interact with the demo. Type the
following in a new terminal:

```bash
roscd youbot_nav_msr
cd launch/
rosrun rviz rviz -d youbotnav.rviz
```

Then you should be able to set a "2D Nav Goal" and watch the youBot navigate to
the location.


Resources
=========

Here are a few links that may be useful to figure out what is going on:

1. ROS Navigation main page: http://wiki.ros.org/navigation
2. ROS Navigation tutorials: http://wiki.ros.org/navigation#Tutorials
3. ROS Wiki page on costmaps: http://wiki.ros.org/costmap_2d

