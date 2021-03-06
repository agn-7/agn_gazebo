### Compatible Versions:
 - *ROS: Kinetic*
 - *OS: Ubuntu-16.04*
 - *Gazebo 7.0*

# Dependencies:
 - [Velodyne Simulator](https://github.com/agn-7/modified_velodyne_simulator)
 - ```sudo apt-get install ros-kinetic-husky-gazebo```
 - [Hector NIST Arenas Elements](https://github.com/tu-darmstadt-ros-pkg/hector_nist_arenas_gazebo)

---
# Install:
Clone this project on your ROS workspace, then run the command below:

```~/catkin_ws$ catkin_make```

---

## Person LiDAR Gazebo model
A Gazebo model in order to [person detection](https://github.com/agn-7/hdl_people_tracking) purpose in an outdoor location using 3D LiDAR Velodyne which is 
compatible to ROS.

### Usage:
Launch its launch files:

 - **Fixed persons**:
    ```
    roslaunch agn_gazebo static_velodyne.launch
    ```

 - **Animated persons**:
    ```
    roslaunch agn_gazebo animated_person.launch
    roslaunch agn_gazebo movement.launch
    ```
    
 - To store the persons position in .csv files run the command below:
    ```
    roslaunch agn_gazebo groundtruth.launch
    ```   
Gazebo:
![default_gzclient_camera(1)-2019-05-23T15_06_12 310211](https://user-images.githubusercontent.com/14202344/58246505-7dade880-7d6c-11e9-8482-28f42baeb138.jpg "Person and LiDAR")

Rviz:
![RVIZ-MARKER](https://user-images.githubusercontent.com/14202344/58627451-911cfe80-82ec-11e9-8270-592f09e5c37a.png "Animated person and LiDAR") 
---

## Pioneer P3DX Gazebo model
A Gazebo model in order to [wall-following]() and go-to algorithms purpose like the [Bug](https://github.com/agn-7/bugs) navigation algorithm 

### Usage:
Launch its launch file:

```
roslaunch agn_gazebo pioneer.launch
```
![default_gzclient_camera(1)-2019-05-30T15_22_49 379103](https://user-images.githubusercontent.com/14202344/58628547-3638d680-82ef-11e9-91a0-3ee7d6ac8893.jpg "Ready to wall following or goto x,y scenario")

---

## Rescue robot exploration Gazebo model
A Gazebo model in order to prepare an environment for a rescue robot on [Exploration]() task in a ramped maze map. 

### Usage:
Launch its launch file:

```
roslaunch agn_gazebo rescue.launch
```

![default_gzclient_camera(1)-2019-09-09T13_59_48 114326](https://user-images.githubusercontent.com/14202344/64522067-6f311000-d30e-11e9-8a6e-b416ad28bdd3.jpg "Rescue robot in maze map")

---