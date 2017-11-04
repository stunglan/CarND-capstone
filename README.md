# Notes to capstone project 


# Set up the environment

## Preparation
I used the recipe from 
[CarND-Capstone project's Docker container](https://github.com/bydavy/CarND-Capstone-Docker)

1. Go to your project directory

```sh
cd /Users/knuttungland/src/CarND-TrackMasters-stunglan-Capstone
```

2. Download the script into your project

```sh 
wget https://raw.githubusercontent.com/bydavy/CarND-Capstone-Docker/master/utils/run.sh && chmod u+x run.sh
```

download the simulator from the classroom

## Usage

1. Start the script

```sh
./run.sh
```
2. You're now within the container and the current directory contains the source code of your project.

### Inside the docker

1. clone the project

```sh
git clone https://github.com/khalilia2000/CarND-TrackMasters-Capstone
```
2. Install python dependencies
```sh
cd CarND-TrackMasters-Capstone
pip install -r requirements.txt
```
3. Make and run styx
```sh
cd ros

catkin_make && source devel/setup.sh && roslaunch launch/styx.launch
# logging
tail -f /home/udacity/.ros/log/latest/dbw_node-4-stdout.log
# topics
rostopic echo /vehicle/throttle_cmd


```

## Start the simulator on the mac

and it works (the simulator and ros talks)



### Aliases

Here are some of the cool aliases that are defined in the container
```sh
udacity_make #Compiles the project
udacity_run #Executes the project
Multiple bash sessions
```
Simply open a new terminal and run the script again,  if your container is currently running it will attach to it. Therefore, you can have one terminal session to run the project and another one to query ROS's topic or what have you.


# Tasks


## DBM Node

### Message types
```
rostopic type /current_velocity
```
```
rosmsg show geometry_msgs/TwistStamped
```
```
std_msgs/Header header
  uint32 seq
  time stamp
  string frame_id
geometry_msgs/Twist twist
  geometry_msgs/Vector3 linear
    float64 x
    float64 y
    float64 z
  geometry_msgs/Vector3 angular
    float64 x
    float64 y
    float64 z
```

```
rostopic type vehicle/dbw_enabled

std_msgs/Bool
rosmsg show std_msgs/Bool             
bool data
```

common commands
```
cd /udacity/CarND-TrackMasters-Capstone/ros && catkin_make && source devel/setup.sh && roslaunch launch/styx.launch
# logging
tail -f /home/udacity/.ros/log/latest/dbw_node-4-stdout.log
#nodes
rosnode list
# topics
rostopic list
rostopic echo /vehicle/throttle_cmd
rostopic echo /vehicle/steering_cmd
rostopic echo /vehicle/brake_cmd
rostopic echo /rosout
```
mac commands

```

open system_integration.app/

open /Applications/Docker.app/ 

```





