

# ROS Network Setup for Master-Slave Communication

# 1.Overview

This guide provides instructions for setting up a ROS (Robot Operating System) network between a powerful PC (master) and a laptop PC (slave) for wireless communication. The master PC runs roscore, while the slave PC executes the rosaria node to handle robot control and odometry data.

# 2.Installation and Configuration

Step 1: Configure ROS Network

On the Master PC

Edit the .bashrc file by adding the following commands:
```bash export ROS_HOSTNAME=192.168.0.121
$ export ROS_HOSTNAME=192.168.0.121   # Replace with your master PC's IP
$ export ROS_MASTER_URI=http://192.168.0.121:11311 # Master URI

Then, apply the changes:

$ source ~/.bashrc # Source the .bashrc file 

On the Slave PC

Edit the .bashrc file by adding the following commands:

$ export ROS_HOSTNAME=192.168.0.200   # Replace with your slave PC's IP
$ export ROS_MASTER_URI=http://192.168.0.121:11311 

Then, apply the changes:

$ source ~/.bashrc

Step 2: ROS Master and Required Packages 

On the Master PC
Run the following command to start the ROS master and parameter server in the command line 
$ roscore

On the Slave PC
Run the following command to start the rosaria node:
$ rosrun rosaria RosAria

This node interfaces the robot with the netbook computer (slave), handling topic communication for velocity commands (/RosAria/cmd_vel) and odometry data (/RosAria/pose).

# Additional Resources

For further assistance, refer to the following official ROS documentation and tutorials:

https://wiki.ros.org/   % Documentation Official documentation and package descriptions.
https://wiki.ros.org/Documentation % ROS Official Documentation
https://www.turtlebot.com/turtlebot2/ % TurtleBot2 Homepage
https://wiki.ros.org/ROSARIA ROSARIA Tutorial % How to use ROSARIA

# References:

[1] MathWorks, "MATLAB Documentation," [Online]. Available: MATLAB ROS Nodes. [Accessed: 31-Jan-2025].


