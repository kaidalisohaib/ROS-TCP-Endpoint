# ROS TCP Endpoint

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Introduction

[ROS](https://www.ros.org/) package used to create an endpoint to accept ROS messages sent from a Unity scene using the [ROS TCP Connector](https://github.com/Unity-Technologies/ROS-TCP-Connector) scripts.

Instructions and examples on how to use this ROS package can be found on the [Unity Robotics Hub](https://github.com/Unity-Technologies/Unity-Robotics-Hub/blob/master/tutorials/ros_unity_integration/README.md) repository.

## Installation

Clone this repository into your ROS 2 workspace `src` folder, and ensure you checkout the `main-ros2-optimized` branch:

```bash
# Source your ROS 2 installation (replace <distro> with your ROS 2 version, e.g. humble, foxy)
source /opt/ros/<distro>/setup.bash

# Create a workspace if you don't already have one
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src

# Clone the optimized branch of the endpoint
git clone -b main-ros2-optimized https://github.com/kaidalisohaib/ROS-TCP-Endpoint.git

# Navigate to the workspace root and build
cd ~/ros2_ws
colcon build --symlink-install

# Source the newly built workspace
source install/setup.bash
```

## Community and Feedback

The Unity Robotics projects are open-source and we encourage and welcome contributions.
If you wish to contribute, be sure to review our [contribution guidelines](CONTRIBUTING.md)
and [code of conduct](CODE_OF_CONDUCT.md).

## Support
For questions or discussions about Unity Robotics package installations or how to best set up and integrate your robotics projects, please create a new thread on the [Unity Robotics forum](https://forum.unity.com/forums/robotics.623/) and make sure to include as much detail as possible.

For feature requests, bugs, or other issues, please file a [GitHub issue](https://github.com/Unity-Technologies/ROS-TCP-Endpoint/issues) using the provided templates and the Robotics team will investigate as soon as possible.

For any other questions or feedback, connect directly with the
Robotics team at [unity-robotics@unity3d.com](mailto:unity-robotics@unity3d.com).

## License
[Apache License 2.0](LICENSE)