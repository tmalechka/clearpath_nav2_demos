
**Please provide the following information:**
 - OS: (e.g. Ubuntu 24.04)
 - ROS 2 Distro: (e.g. Jazzy)
 - Built from source or installed: installed
 - Package version: jazzy-version of clearpath_nav2_demos
 - Real hardware or simulation: simulation

 **Expected behaviour**
 /map frame appears in RVIZ


 **Actual behaviour**
I attempted to run the SLAM simulation by launching all three required launch files as described:
 1. ros2 launch clearpath_gz simulation.launch.py
 2. ros2 launch clearpath_viz view_navigation.launch.py namespace:=a200_0000
 3. ros2 launch clearpath_nav2_demos slam.launch.py setup_path:=$HOME/clearpath/ use_sim_time:=true

The slam_toolbox node is successfully launched. However, it does not subscribe to the expected /a200_0000/sensors/lidar2d_0/scan topic (see attached file). As a result, it cannot generate and publish the /map frame, and the mapping step does not proceed.
Additionally, when inspecting the graph in rqt_graph, I notice (two?) unnamed nodes represented as small circles.


[Screenshot from 2025-05-12 19-11-05](https://github.com/user-attachments/assets/65c0c2e3-2c9d-4d62-9398-98c760f5f508
