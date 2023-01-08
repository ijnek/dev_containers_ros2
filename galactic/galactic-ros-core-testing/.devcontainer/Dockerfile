FROM ros:galactic-ros-core

# Use ROS 2 testing repository
RUN echo "deb http://packages.ros.org/ros2-testing/ubuntu focal main" > /etc/apt/sources.list.d/ros2-testing.list

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Install dependencies not included for ROS Core Docker Images
RUN apt install build-essential -y
RUN apt install git -y
RUN apt install python3-colcon-common-extensions -y
RUN apt install python3-rosdep -y

# Rosdep init and update
RUN rosdep init
RUN rosdep update --include-eol-distros

# Source the ROS galactic setup file
RUN echo "source /opt/ros/galactic/setup.bash" >> ~/.bashrc
