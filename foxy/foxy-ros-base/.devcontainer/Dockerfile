FROM ros:foxy-ros-base

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Rosdep
RUN rosdep update

# Source the ROS foxy setup file
RUN echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
