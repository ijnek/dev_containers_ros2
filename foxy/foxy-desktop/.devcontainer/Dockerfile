FROM osrf/ros:foxy-desktop

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Allows gdb
RUN apt install gdb -y

# Source the ROS foxy setup file
RUN echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
