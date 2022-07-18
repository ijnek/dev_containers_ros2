FROM ros:rolling-ros-core

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Allows gdb
RUN apt install gdb -y

# Source the ROS Rolling setup file
RUN echo "source /opt/ros/rolling/setup.bash" >> ~/.bashrc
