FROM ros:humble-ros-base

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Rosdep update
RUN rosdep update

# Source the ROS humble setup file
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
