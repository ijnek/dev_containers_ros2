FROM osrf/ros:galactic-desktop

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Allows gdb
RUN apt install gdb -y

# Source the ROS galactic setup file
RUN echo "source /opt/ros/galactic/setup.bash" >> ~/.bashrc
