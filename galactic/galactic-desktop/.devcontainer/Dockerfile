FROM osrf/ros:galactic-desktop

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install gdb -y

# Rosdep update
RUN rosdep update --include-eol-distros

# Source the ROS galactic setup file
RUN echo "source /opt/ros/galactic/setup.bash" >> ~/.bashrc
