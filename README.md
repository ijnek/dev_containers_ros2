# Dev Containers ROS2

Personal dev containers for ROS2 projects

## Instructions

You must add to your host-machine's ``~/.bashrc``,

```sh
xhost +local:root > /dev/null  # Allows GUI in dev container to work
```

if you want to open any GUI programs from inside dev-containers.


## Notes

In ``devcontainer.json``:

* ``mounts``
  * ``source=/tmp/.X11-unix,target=/tmp/.X11-unix,type=bind,consistency=cached`` allows GUI programs to work. This is necessary for
  RQt to work.
* ``runArgs``
  * ``--device=/dev/video0:/dev/video0:mwr`` allows the container to access the host's webcam. This is necessary for nodes such as ``usb_cam``or ``v4l2_camera``.
  * ``--network=host`` allows the container to share the host’s networking namespace, and the container does not get its own IP-address allocated.
  This is necessary for nodes inside the docker container to communicate to
  nodes on the same network but on a different machine.
  * ``--device=/dev/dri:/dev/dri`` allows the container to access the host's GPU. This is needed to run ``rviz2``.
