## ROS2 setup
1. First ensure that the Ubuntu Universe repository is enabled.
```python
sudo apt install software-properties-common
sudo add-apt-repository universe
```
2. add the ROS 2 GPG key with apt & add rep to sources list.
```python
curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | apt-key add -
echo "deb http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" | tee /etc/apt/sources.list.d/ros2-latest.list
apt update
```
3. Desktop install

`apt install -y ros-galactic-desktop`



