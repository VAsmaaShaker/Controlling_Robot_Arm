# Controlling_Robot_Arm-
Implementing a robot arm on ROS by joint_state_publisher, Moveit, and kinematics.

### Step1: Creating a ROS Workspace
1- Enter the following commands in your cmd:
```bash
 source /opt/ros/noetic/setup.bash
 mkdir -p ~/catkin_ws/src
 cd ~/catkin_ws/ 
 catkin_make
 source devel/setup.bash
```
 Your ROS workspace is now prepared to install packages.


### Step2: Installing Arduino Robot Arm Package
** Note: Add the “arduino_robot_arm” package to “src” folder.
```bash
 cd catkin_ws/src/
 sudo apt install git
 git clone https://github.com/smart-methods/arduino_robot_arm
```


### Step3: Installing Dependencies

```bash
 cd catkin_ws
 sudo apt-get install ros-noetic-moveit
 sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
 sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
 sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```

### Step4: Compiling Packages

```bash
catkin_make
```

## Usage
### Controlling the Robot Arm

#### 1. Launching RViz with Joint State Publisher

```bash
roslaunch robot_arm_pkg check_motors.launch
```
![image](https://github.com/VAsmaaShaker/Controlling_Robot_Arm-/assets/174564364/07a38e86-c4df-4e3a-a53c-77e76c6937a0)
![image](https://github.com/VAsmaaShaker/Controlling_Robot_Arm-/assets/174564364/72ca14d2-266f-47c6-ab7a-2555135b2046)

#### 2. Running Gazebo Simulation

```bash
roslaunch robot_arm_pkg check_motors_gazebo.launch
```
![image](https://github.com/VAsmaaShaker/Controlling_Robot_Arm-/assets/174564364/95ce5e23-aef7-4868-8bde-0d68c6db8df2)

#### 3. Using Moveit for Kinematics

```bash
roslaunch moveit_pkg demo.launch
```
![image](https://github.com/VAsmaaShaker/Controlling_Robot_Arm-/assets/174564364/77a7e1c3-ca23-4f1c-99de-89710a3f588f)





