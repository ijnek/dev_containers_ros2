FROM ros:foxy-ros-base

# Use ROS 2 testing repository
RUN echo "deb http://packages.ros.org/ros2-testing/ubuntu focal main" > /etc/apt/sources.list.d/ros2-testing.list

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Rosdep
RUN rosdep update

# Source the ROS foxy setup file
RUN echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
