Please install this packages:

- fath_pivot_mount_description: 'sudo apt-get install ros-noetic-gazebo-*'
- fath_pivot_mount_description: 'sudo apt-get install ros-noetic-gmapping*'
sudo apt-get install ros-noetic-robot-state-*
sudo apt-get install ros-noetic-joint-*
sudo apt-get install ros-noetic-move-base*
sudo apt-get install ros-noetic-nav*
sudo apt-get install ros-noetic-dwa-local-planner
sudo apt-get install ros-noetic-teb*
sudo apt-get install ros-noetic-costmap-*
sudo apt-get install ros-noetic-controller-*
sudo apt-get install ros-noetic-husky*

Create workspace:
Buka terminal (Ctrl+Alt+T)
Buat folder catkin_ws di home (mkdir catkin_ws)
cd catkin_ws
Buat folder src (mkdir src)
Extract zip ke dalam src
catkin_make (untuk mengcompile)

Run the program:
Ctrl+Alt+T
cd catkin_ws 
source devel/setup.bash
roslaunch husky_gazebo husky_playpen.launch
Ctrl+Alt+T
cd catkin_ws 
source devel/setup.bash
roslaunch husky_navigation gmapping_demo.launch
Ctrl+Alt+T
cd catkin_ws 
source devel/setup.bash
roslaunch husky_viz view_robot.launch
di rviz, klik 2D Nav Goal lalu click dimana saja Anda ingin menjalankan robot 

RRT configuration
Open folder catkin_ws/src/husky/husky_navigation/config
Di dalam folder tersebut, Anda dapat menemukan planner.yaml
Di dalam planner.yaml, ada RRTStartPlanner yang di bawahnya adalah parameter yang berkaitan
method = 0 adalah RRT* dan method = 1 adalah RRT

Kode yang mengimplementasikan algoritma RRT ada di:
catkin_ws/src/rt_star_global_planner/src/rrt_star.cpp


