FROM ros:humble-ros-base

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Source the ROS Humble setup file
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
