This is taken from the original wiki shown at the following:
http://www.youbot-store.com/wiki/index.php?title=Gazebo_simulation&hmswSSOID=10b4d7be36c130126e02a9c81ce579a7f71c954f


ROS Indigo
Since no pre-compiled debian packages are available so far, you have to check out manually. To do that, first create a Catkin workspace, and enter in a terminal

sudo apt-get install ros-indigo-ros-control ros-indigo-ros-controllers ros-indigo-gazebo-ros-control
cd <your-catkin-folder>/src
git clone http://github.com/youbot/youbot_description.git -b indigo-devel
git clone http://github.com/youbot/youbot_simulation.git
catkin_make

The last command should run through without errors. In order to launch it, enter

roslaunch youbot_gazebo_robot youbot.launch 


Note: the simulated motion of the robot can be very slow, as the mobile base uses a non-optimized controller.
