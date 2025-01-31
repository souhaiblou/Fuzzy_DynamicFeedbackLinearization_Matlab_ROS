# Fuzzy_DynamicFeedbackLinearization_Matlab_ROS

As presented in Fig. A The initial stage is to configure the ROS network to assure the wireless
communication between a Powerful PC and a Laptop PC This sort of communication is master-slave.
The powerful PC, as a high-level master, runs rescore inside, and the low-level PC slave runs the
rosaria node to deliver commands and odometry subjects. Set ROS Network setup
In the remote (master) PC, add this command in the .bashrc file.
export ROS HOSTNAME=192.168.0.121 for example
export ROS MASTER URI=http://192.168.0.121:11311
In Netbook PC (slave), add this command in the .bashrc file
export ROS HOSTNAME=192.168.0.200 for example
export ROS MASTER URI=http://192.168.0.121:11311

Run this command on the remote PC: roscore This command runs the ROS master and parameter
server.
Run this command on the netbook PC. – rosrun rosaria rosaria This program executes the rosaria
node for the interface between a robot and computer that delivers all topic requests for transmitting
velocity commands to the /RosAria/cmd vel and Odomety topic /RosAria/pose
For further assistance and supplementary information, look to these official resources:
https://www.ros.org/ Main gateway for ROS middleware.
https://wiki.ros.org/ Documentation Official documentation and package descriptions.
https://www.turtlebot.com/turtlebot2/ Official homepage for the TurtleBot2 mobile robot.
\url{https://wiki.ros.org/ROSARIA/Tutorials/How%20to%20use%20ROSARIA} Tutorial how to com-
municate between robot and computer within ROS by using rosaria node in rosaria ROS package

References:


