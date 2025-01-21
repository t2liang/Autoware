## Prerequisites
- Python 3.9 or higher
- pip or conda for dependency management
- install ROS2 Galactic
- docker container with latest version of Linux

## Installation
1. Clone the galactic branch of autowarefoundation/autoware and move to the directory.
   
   `git clone -b galactic https://github.com/autowarefoundation/autoware.git
cd autoware`
2.  install the dependencies by using the provided Ansible script.
   
   `./setup-dev-env.sh`

## Autoware Workspace
1. Create the src directory and clone repositories into it.
```python
cd autoware
mkdir src
vcs import src < autoware.repos
```
2. Install dependent ROS packages.
```python
source /opt/ros/galactic/setup.bash
rosdep update --include-eol-distros
rosdep install -y --from-paths src --ignore-src --rosdistro $ROS_DISTRO -r
```



