# 1 ASSIGNMENT of RT 2
# Our package consist of four nodes

go_to_point
user_interface
position_service
state_machine
# go_to_point
A service to start or stop the robot moving toward a location in the environment is implemented by the go to point node. Additionally, the node's service would be able to direct the robot at a specific angle and position in the (x,y) coordinate space (theta)
# user_interface:
With the attributes start and stop, the user interface node controls the robot and invokes the state machine node's service.
# position_service:
A random Position Server is implemented by the node PositionServer. Additionally, the service implemented in this node will provide random values for x, y, and a constraint that specifies that the values of x and y must fall between a minimum and maximum.
# state_machine:
 This nodes are implemented in c++ , state_machine node implements a service to start or stop the robot and call the other two service to drive the robot.
# CMakelist.txt
A list of directives and instructions describing the project's source files and targets may be found in the CMakeLists.txt file (executable, library, or both). CLion generates CMakeLists.... txt files to record the build, contents, and target guidelines for a subfolder of the assigned directory when you start a new project.
# dr20_ros_ctrl
he dr20 mobile robot may be controlled from the ros environment using the lua code in the dr20 ros ctrl file. Since there is no action server built, the robot will stop when it reaches the target when the user commands it to stop.

# package.xml
The package manifest is an XML file called package. xml that must be included with any catkin-compliant package's root folder. This file defines properties about the package such as the package name, version numbers, authors, maintainers, and dependencies on other catkin packages.

# srv
ROS uses a simplified service description language ("srv") for describing ROS service types. This builds directly upon the ROS msg format to enable request/response communication between nodes. Service descriptions are stored in .srv files in the srv/ subdirectory of a package.

                  [*]command.srv
                  [*]position.srv
                  [*]Randomposition.srv

# Coppeliasim Package:
This packages facilitates 'got to point' behavior-based robot control in the Coppeliasim environment. The robot then positions itself in relation to a randomly created target. It sets the linear speed to move to the desired position, and once there, it makes the necessary adjustments to get the desired angular position. The procedure will loop if the robot is not stopped, creating new goal destinations and poses. The "go to point" of the robot is implemented as a server. Only when it achieves the goal can the robot be stopped, and it will restart when the new goal is reached. If the robot receives the instruction "stop," the operation will be repeated continuously.


<img width="281" alt="image" src="https://user-images.githubusercontent.com/80621864/154863503-a7ca9ef1-44fe-40da-b905-4fe814e5341c.png">


## Command for Running the package:
1.A launch file has been provided to run all the ros nodes required for the control of robot in coppeliasim environment using ros:
- source ROS1 workspace.
- Vrep.launch: this launch file is used to launch all the required nodes.

```
roslaunch rt2_assignment1 vrep.launch
```
2.To open the coppeliasim application:
```../CoppeliaSim_Edu_V4_2_0_Ubuntu20_04/.coppeliaSim.sh``` 
 - this command will open the coppeliasim simulation.
