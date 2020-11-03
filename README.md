Vectornav ROS Driver
====================

A ROS node for VectorNav INS & GPS devices.

This package provides a sensor_msg interface for the VN100, 200, & 300 
devices. Simply configure your launch files to point to the serial port
of the deice and you can use rostopic to quickly get running.   

Forked from https://github.com/dawonn/vectornav



QuickStart Guide
----------------

This assumes that you have a VectorNav device connected to your computer 
via a USB cable and that you have already created a [catkin workspace][2]

Build:

1. cd ~/catkin_ws/src
2. git clone https://github.com/acachathuranga/vectornav.git
3. cd ..
4. catkin_make


Run:

5. (Terminal 1) roscore
6. (Terminal 2) roslaunch vectornav vectornav.launch
7. (Terminal 3) rostopic list
8. (Terminal 3) rostopic echo /vectornav/IMU
9. (Terminal #) ctrl+c to quit



Changes
-------
Added Udev Rules for vectornav IMUs. Please refer to 'udev_rules/vectornav.rules' file for more details.

Added launch file and configuration files for VN200

IMU topics are now scoped under the name of the package. Hence now it is possible to run multiple instances of the IMU node (Now multiple IMUs can be used together) without ROS namespacing.




