FROM ros:humble-ros-core

# Rosdep update
RUN rosdep update

# Update all packages
RUN apt update && apt upgrade -y

# Allows ssh repository cloning
RUN apt install openssh-client -y

# Allows gdb
RUN apt install gdb -y

# Source the ROS humble setup file
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
