# SmartMesthod Task-1 Robotic arm

we set up ros on virtual machine and using Ubuntu 18.04 

![image](https://github.com/suliman016/SmartMesthod-Task-1-Robotic-arm/assets/139249285/f7f5af37-1304-4aaa-8bce-d759aa41e721)

then we open terminal and insert commands
> sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
> 
> sudo apt install curl
> 
> curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
> 
> sudo apt update
> 
> sudo apt install ros-melodic-desktop-full
> 
> apt search ros-melodic
> 
> echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
> 
> source ~/.bashrc
> 
> sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
> 
> sudo apt install python-rosdep
> 
> sudo rosdep init
> 
> rosdep update
> 
![1](https://github.com/suliman016/suliman016/assets/139249285/ca4da400-507d-490f-8de3-723e84f22ee4)

## making a workspace

we insert these commands in terminal

> source /opt/ros/melodic/setup.bash
>
> mkdir -p ~/catkin_ws/src
>
> cd ~/catkin_ws/
>
> catkin_make

## Add the “arduino_robot_arm” package to “src” folder

> cd ~/catkin_ws/src
>
> sudo apt install git
>
> git clone https://github.com/smart-methods/arduino_robot_arm

![image](https://github.com/suliman016/SmartMesthod-Task-1-Robotic-arm/assets/139249285/88b33ea1-63aa-478e-bbdb-52d4a52a3bde)

![image](https://github.com/suliman016/SmartMesthod-Task-1-Robotic-arm/assets/139249285/f4a1b3c6-57d8-4f4a-81ac-6931751a1ac7)

## Install all the dependencies 

> cd ~/catkin_ws
>
>  rosdep install --from-paths src --ignore-src -r -y
>
> sudo apt-get install ros-melodic-moveit
>
> sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
>
> sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
>
> sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
>
> catkin_make



## Controlling the motors

> source /home/slom/catkin_ws/devel/setup.bash
>
> roslaunch robot_arm_pkg check_motors.launch

![image](https://github.com/suliman016/SmartMesthod-Task-1-Robotic-arm/assets/139249285/1d9a95d1-e76f-42ae-9e31-635c082b99b2)
![image](https://github.com/suliman016/SmartMesthod-Task-1-Robotic-arm/assets/139249285/223e7811-5b20-46cd-a3ab-e5d5010f9da9)







