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
