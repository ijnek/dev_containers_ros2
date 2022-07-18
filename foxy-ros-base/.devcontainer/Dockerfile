FROM ros:foxy

# # Switch from sh to bash
# SHELL ["/bin/bash", "-c"]

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Source the ROS Foxy setup file
RUN echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
