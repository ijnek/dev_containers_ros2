FROM ros:rolling-ros-core

# Use ROS 2 testing repository
RUN echo "deb http://packages.ros.org/ros2-testing/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-testing.list

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Install dependencies not included for ROS Core Docker Images
RUN apt install build-essential -y
RUN apt install git -y
RUN apt install python3-colcon-common-extensions -y
RUN apt install python3-rosdep -y

# Rosdep update
RUN rosdep update

# Source the ROS Rolling setup file
RUN echo "source /opt/ros/rolling/setup.bash" >> ~/.bashrc
