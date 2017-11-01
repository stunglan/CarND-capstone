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
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```

## Start the simulator on the mac

and it works



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



