## This branch contains a skeleton version of the original package, the lightweight version, for installation on the go1!


## Overview
Welcome to the *interbotix_ros_manipulators* repository! This repo contains custom ROS packages to control the various types of arms sold at [Trossen Robotics](https://www.trossenrobotics.com/). These ROS packages build upon the ROS driver nodes found in the [interbotix_ros_core](https://github.com/Interbotix/interbotix_ros_core) repository. Support-level software can be found in the [interbotix_ros_toolboxes](https://github.com/Interbotix/interbotix_ros_toolboxes) repository.

### Build Status

| ROS Distro | X-Series ROS Manipulators Build |
| :------- | :------- |
| ROS 1 Melodic | [![build-xs-melodic](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-melodic.yaml/badge.svg)](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-melodic.yaml) |
| ROS 1 Noetic | [![build-xs-noetic](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-noetic.yaml/badge.svg)](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-noetic.yaml) |
| ROS 2 Galactic | [![build-xs-galactic](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-galactic.yaml/badge.svg)](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-galactic.yaml) |
| ROS 2 Humble | [![build-xs-humble](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-humble.yaml/badge.svg)](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-humble.yaml) |
| ROS 2 Rolling | [![build-xs-rolling](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-rolling.yaml/badge.svg)](https://github.com/Interbotix/interbotix_ros_manipulators/actions/workflows/xs-rolling.yaml) |

## Repo Structure
```
GitHub Landing Page: Explains repository structure and contains a single directory for each type of manipulator.
├── Manipulator Type X Landing Page: Contains 'core' arm ROS packages.
│   ├── Core Arm ROS Package 1
│   ├── Core Arm ROS Package 2
│   ├── Core Arm ROS Package X
│   └── Examples: contains 'demo' arm ROS packages that build upon some of the 'core' arm ROS packages
│       ├── Demo Arm ROS Package 1
│       ├── Demo Arm ROS Package 2
│       ├── Demo Arm ROS Package X
│       └── Demo Scripts: contains example scripts that build upon the interface modules in the interbotix_ros_toolboxes repository
│           ├── Demo Script 1
│           ├── Demo Script 2
|           └── Demo Script X
├── CITATION.cff
├── LICENSE
└── README.md
```
As shown above, there are five main levels to this repository. To clarify some of the terms above, refer to the descriptions below.

- **Manipulator Type** - Any robotic arm that can use the same *interbotix_XXarm_control* package is considered to be of the same type. For the most part, this division lies on the type of actuator that makes up the robot. As an example, all the X-Series arms are considered the same type of manipulator since they all use various Dynamixel X-Series servos (despite the fact that they come in different sizes, DOF, and motor versions). However, a robotic arm made up of some other manufacturer's servos, or even half made up of Dynamixel servos and half made up of some other manufacturer's servos would be considered a different manipulator type.

- **Demo Script** - This refers to demo scripts that build upon the interface modules in the *interbotix_ros_toolboxes* repository. These modules essentially abstract away all ROS code, making it easy for a researcher with no ROS experience to interface with an arm as if it was just another object. It also makes sequencing robot motion a piece of cake. These scripts are written in languages that users may feel more comfortable with like Python and MATLAB. The directories that contain demo scripts for each language may be found the in example directory, or in the package that specifically relates to their usage, such as the perception packages.

Over time, the repo will grow to include more types of manipulators.

## Contributing
Feel free to send PRs to add features to currently existing Arm ROS packages or to include new ones. Note that all PRs should follow the structure and naming conventions outlined in the repo including documentation.

## Contributors
- [Solomon Wiznitzer](https://github.com/swiz23) - **ROS Engineer**
- [Luke Schmitt](https://github.com/lsinterbotix) - **Robotics Software Engineer**
- [Levi Todes](https://github.com/LeTo37) - **CAD Engineer**

## Citing

If using this software for your research, please include the following citation in your publications:

```bibtex
@software{Wiznitzer_interbotix_ros_manipulators,
  author = {Wiznitzer, Solomon and Schmitt, Luke and Trossen, Matt},
  license = {BSD-3-Clause},
  title = {{interbotix_ros_manipulators}},
  url = {https://github.com/Interbotix/interbotix_ros_manipulators}
}
