# Dev Containers ROS2

Personal dev containers for ROS2 projects

## Before you start

You must add to your host-machine's ``~/.bashrc``,

```sh
xhost +local:root > /dev/null  # Allows GUI in dev container to work
```

This lets you open GUI programs from within the dev-containers.

## Instructions

1. Clone this repository
1. In VS Code, Click on ``Open Folder... [Ctrl+K Ctrl+O]``, and open one of the subdirectories that contain a ``.devcontainer`` folder. (eg. ``rolling-desktop``)
1. VS Code will bring up a dialog, asking about opening the folder in a dev container. Click on ``Reopen in Container``.

VS Code will then build the devcontainer. This takes some time the first time, but the second time should be much quicker.

If VS Code opens a dev container successfully, you now have ROS 2 (Rolling Desktop packages in this case) pre-installed, and ready to be used within that window. You can create a ROS 2 workspace and start developing!

If the build fails (it happens sometimes), open a GitHub Issue and post any available logs in it!

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
