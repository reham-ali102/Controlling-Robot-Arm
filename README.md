# Controlling-Robot-Arm
# Controlling-Robot-Arm
This structured guide provides clear steps for setting up and controlling the robot arm using ROS, including running simulations and using MoveIt for kinematics.

### Step 1: Creating a ROS Workspace
In your Terminal, Enter the following commands:
```sh
 source /opt/ros/noetic/setup.bash
 mkdir -p ~/catkin_ws/src
 cd ~/catkin_ws/ 
 catkin_make
 source devel/setup.bash
```
Installing packages is now possible in your ROS workspace. 

### Step2: Installing Arduino Robot Arm Package
In the "src" folder, add the "arduino_robot_arm" package.
```sh
 cd catkin_ws/src/
 sudo apt install git
 git clone https://github.com/smart-methods/arduino_robot_arm
 ```
### Step3: Installing Dependencies
```sh
 cd catkin_ws
 sudo apt-get install ros-noetic-moveit
 sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
 sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
 sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
 ```
### Step4: Compiling Packages
```sh
catkin_make
 ```
### Implementing a Robot Arm Using ROS
 1: Joint State Publisher Launches RViz
  ```sh
roslaunch robot_arm_pkg check_motors.launch
 ```
![Turtlesim running](https://github.com/reham-ali102/Controlling-Robot-Arm/blob/main/1.png)
![Turtlesim running](https://github.com/reham-ali102/Controlling-Robot-Arm/blob/main/2.png)

2. Running Gazebo Simulation
```sh
roslaunch robot_arm_pkg check_motors_gazebo.launch
 ```
![Turtlesim running](https://github.com/reham-ali102/Controlling-Robot-Arm/blob/main/3.png)

3. Using Moveit for Kinematics
```sh
roslaunch moveit_pkg demo.launch
 ```
![Turtlesim running](https://github.com/reham-ali102/Controlling-Robot-Arm/blob/main/4.png)
