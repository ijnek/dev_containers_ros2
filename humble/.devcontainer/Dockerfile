FROM ros:humble

# # Switch from sh to bash
# SHELL ["/bin/bash", "-c"]

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Source the ROS Humble setup file
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
