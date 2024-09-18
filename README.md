# urdf_sim_tutorial
See the tutorials over at http://wiki.ros.org/urdf_tutorial
https://wiki.ros.org/urdf/Tutorials/Using%20a%20URDF%20in%20Gazebo

# Nonfunctional Gazebo Interface
    roslaunch urdf_sim_tutorial gazebo.launch

# Gazebo Plugin
    roscd urdf_sim_tutorial
    roslaunch urdf_sim_tutorial gazebo.launch model:=urdf/09-publishjoints.urdf.xacro

# Spawning Controllers with URDF
    roslaunch urdf_sim_tutorial 09-joints.launch 

# First Transmission
    roscd urdf_sim_tutorial
    roslaunch urdf_sim_tutorial 09-joints.launch model:=urdf/10-firsttransmission.urdf.xacro

# Joint Control
    roscd urdf_sim_tutorial
    roslaunch urdf_sim_tutorial 10-head.launch
    rostopic pub /r2d2_head_controller/command std_msgs/Float64 "data: -0.707"

    roslaunch urdf_sim_tutorial 10-head.launch model:=urdf/11-limittransmission.urdf.xacro
    rostopic pub /r2d2_head_controller/command std_msgs/Float64 "data: -0.707"

# Another Controller
    roslaunch urdf_sim_tutorial 12-gripper.launch

rostopic pub  /r2d2_gripper_controller/command std_msgs/Float64MultiArray "layout:
  dim:
  - label: ''
    size: 3
    stride: 1
  data_offset: 0
data: [0, 0.5, 0.5]"

# The Wheels on the Droid Go Round and Round
roslaunch urdf_sim_tutorial 13-diffdrive.launch

rostopic pub /r2d2_diff_drive_controller/cmd_vel geometry_msgs/Twist "linear:
  x: 1.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.5"




