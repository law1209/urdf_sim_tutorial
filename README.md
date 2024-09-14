# urdf_sim_tutorial
See the tutorials over at http://wiki.ros.org/urdf_tutorial
https://wiki.ros.org/urdf/Tutorials/Using%20a%20URDF%20in%20Gazebo

# Nonfunctional Gazebo Interface
    roslaunch urdf_sim_tutorial gazebo.launch

# Gazebo Plugin
    roslaunch urdf_sim_tutorial gazebo.launch model:=urdf/09-publishjoints.urdf.xacro

# Spawning Controllers with URDF
    roslaunch urdf_sim_tutorial 09-joints.launch 

# Transmissions
    roslaunch urdf_sim_tutorial 09-joints.launch model:=urdf/10-firsttransmission.urdf.xacro

# Joint Control
    roslaunch urdf_sim_tutorial 10-head.launch 
    roslaunch urdf_sim_tutorial 10-head.launch model:=urdf/11-limittransmission.urdf.xacro

# Another Controller
    roslaunch urdf_sim_tutorial 12-gripper.launch

# The Wheels on the Droid Go Round and Round
    roslaunch urdf_sim_tutorial 13-diffdrive.launch

