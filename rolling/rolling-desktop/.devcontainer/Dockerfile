FROM osrf/ros:rolling-desktop

# Update all packages
RUN apt update && apt upgrade -y

# Install extra packages
RUN apt install build-essential -y
RUN apt install gdb -y
RUN apt install git -y
RUN apt install python3-colcon-common-extensions -y
RUN apt install python3-rosdep -y

# Rosdep update
RUN rosdep update

# Source the ROS Rolling setup file
RUN echo "source /opt/ros/rolling/setup.bash" >> ~/.bashrc
