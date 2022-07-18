FROM ros:galactic

# # Switch from sh to bash
# SHELL ["/bin/bash", "-c"]

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Source the ROS Galactic setup file
RUN echo "source /opt/ros/galactic/setup.bash" >> ~/.bashrc
