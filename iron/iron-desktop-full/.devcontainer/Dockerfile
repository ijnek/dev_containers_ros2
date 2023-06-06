FROM osrf/ros:iron-desktop-full

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Rosdep update
RUN rosdep update

# Source the ROS iron setup file
RUN echo "source /opt/ros/iron/setup.bash" >> ~/.bashrc
