# ORB-SLAM2
**ORB-SLAM2 Authors:** [Raul Mur-Artal](http://u.720life.cn/g/8c1a32ab04b122d969e0c6d038546ab7b1fb7f4aee44a7933393fa5ecd762286aa519d71129067b1af32c34923254e99  [Juan D. Tardos](http://u.720life.cn/g/8c1a32ab04b122d969e0c6d038546ab7014d2888abca2723d6a438fe0b00a2295bc8ce34de24cb94e6167bae229f4ee8  [J. M. M. Montiel](http://u.720life.cn/g/8c1a32ab04b122d969e0c6d038546ab771e774f1cc641f6df7e2528673ec172f7126778d7ba64319ac39c7501657f438)  and [Dorian Galvez-Lopez](http://u.720life.cn/g/082c5281602353fe0ae84644a12acde7d4bf62a171dba9cee7d22d848693c326)  ([DBoW2](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304698bb13107f188419d6f189b741dc2293612b59e430f675d29692ef6be3a665dc 
The original implementation can be found [here](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4d3abf265b29ed76f79f6690aec6cf88739820b0058ff10aef3b27995f16b35 

# ORB-SLAM2 ROS node
This is the ROS implementation of the ORB-SLAM2 real-time SLAM library for **Monocular**, **Stereo** and **RGB-D** cameras that computes the camera trajectory and a sparse 3D reconstruction (in the stereo and RGB-D case with true scale). It is able to detect loops and relocalize the camera in real time. This implementation removes the Pangolin dependency, and the original viewer. All data I/O is handled via ROS topics. For vizualization you can use RViz. This repository is maintained by [Lennart Haller](http://u.720life.cn/g/621977f82cb5c6cf251443b33c1a9d1c8ceabb2ee2b416af81da31345e1845e0)  on behalf of [appliedAI](http://u.720life.cn/g/a189aa807004a93c4c169d0b003e50c13058a54eee592e7dff4883ba5f5050bf 
## Features
- Full ROS compatibility
- Supports a lot of cameras out of the box, such as the Intel RealSense family. See the run section for a list
- Data I/O via ROS topics
- Parameters can be set with the rqt_reconfigure gui during runtime
- Very quick startup through considerably sped up vocab file loading
- Full Map save and load functionality based on [this PR](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046e4d3abf265b29ed76f79f6690aec6cf879c01344c4ac7e76871f07c660498b50 
- Loading of all parameters via launch file
- Supports loading cam parameters from cam_info topic

### Related Publications:
[Monocular] Raúl Mur-Artal, J. M. M. Montiel and Juan D. Tardós. **ORB-SLAM: A Versatile and Accurate Monocular SLAM System**. *IEEE Transactions on Robotics,* vol. 31, no. 5, pp. 1147-1163, 2015. (**2015 IEEE Transactions on Robotics Best Paper Award**). **[PDF](http://u.720life.cn/g/8c1a32ab04b122d969e0c6d038546ab7b1fb7f4aee44a7933393fa5ecd762286e9462697a53fb830bb67c0837bf1cbd8530a7c61352be5d0c37cbf1213a47501 

[Stereo and RGB-D] Raúl Mur-Artal and Juan D. Tardós. **ORB-SLAM2: an Open-Source SLAM System for Monocular, Stereo and RGB-D Cameras**. *IEEE Transactions on Robotics,* vol. 33, no. 5, pp. 1255-1262, 2017. **[PDF](http://u.720life.cn/g/df51c401e5bda0655a95f22b00e33f97f4b3056bc472d2bf28784aa554e6a830874358909c677142ebc7f6398f15e783 

[DBoW2 Place Recognizer] Dorian Gálvez-López and Juan D. Tardós. **Bags of Binary Words for Fast Place Recognition in Image Sequences**. *IEEE Transactions on Robotics,* vol. 28, no. 5, pp.  1188-1197, 2012. **[PDF](http://u.720life.cn/g/082c5281602353fe0ae84644a12acde7b0d29bed0b15b870c1447ca7cd8ae40431aef3f913c1e7b6476bfd07daeb33cc94cce37daab543ad65edcb494bebc311 

# 1. License
ORB-SLAM2 is released under a [GPLv3 license](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468056cbbbc50225170948ace94d2450f8ebdec2aa07727ca1552515825b2055782440f10a38d7d3a24fa217ead005b85973ddbae4a90b2cadfdfbfd796c052e11  For a list of all code/library dependencies (and associated licenses), please see [Dependencies.md](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468056cbbbc50225170948ace94d2450f8ebdec2aa07727ca1552515825b20557884f316cdaa7925aa8a445d003eae608a4bc6e7c4603482a3b56522fb5c5cb887 

For a closed-source version of ORB-SLAM2 for commercial purposes, please contact the authors: orbslam (at) unizar (dot) es.

If you use ORB-SLAM2 (Monocular) in an academic work, please cite:

    @article{murTRO2015,
      title={{ORB-SLAM}: a Versatile and Accurate Monocular {SLAM} System},
      author={Mur-Artal, Ra\'ul, Montiel, J. M. M. and Tard\'os, Juan D.},
      journal={IEEE Transactions on Robotics},
      volume={31},
      number={5},
      pages={1147--1163},
      doi = {10.1109/TRO.2015.2463671},
      year={2015}
     }

if you use ORB-SLAM2 (Stereo or RGB-D) in an academic work, please cite:

    @article{murORB2,
      title={{ORB-SLAM2}: an Open-Source {SLAM} System for Monocular, Stereo and {RGB-D} Cameras},
      author={Mur-Artal, Ra\'ul and Tard\'os, Juan D.},
      journal={IEEE Transactions on Robotics},
      volume={33},
      number={5},
      pages={1255--1262},
      doi = {10.1109/TRO.2017.2705103},
      year={2017}
     }

# 2. Building orb_slam2_ros
We have tested the library in **Ubuntu 16.04** with **ROS Kinetic** and **Ubuntu 18.04** with **ROS Melodic**. A powerful computer (e.g. i7) will ensure real-time performance and provide more stable and accurate results.
A C++11 compiler is needed.

## Getting the code
Clone the repository into your catkin workspace:
```
git clone https://github.com/appliedAI-Initiative/orb_slam_2_ros.git
```

## ROS
This ROS node requires catkin_make_isolated or catkin build to build. This package depends on a number of other ROS packages which ship with the default installation of ROS.
If they are not installed use [rosdep](http://u.720life.cn/g/214cba4ede9838afaceac6b9476b87946b191dfb8563590155cd547cb5b466bc)  to install them. In your catkin folder run
```
sudo rosdep init
rosdep update
rosdep install --from-paths src --ignore-src -r -y
```
to install all dependencies for all packages. If you already initialized rosdep you get a warning which you can ignore.

## Eigen3
Required by g2o. Download and install instructions can be found [here](http://u.720life.cn/g/0b718b6d2214b81e95b43a5bb462cdf333663f3dd3367afa7d7d0f8333256052 
Otherwise Eigen can be installed as a binary with:
```
sudo apt install libeigen3-dev
```
**Required at least Eigen 3.1.0**.

## Building
To build the node run
```
catkin build
```
in your catkin folder.

# 3. Configuration
## Vocab file
To run the algorithm expects both a vocabulary file (see the paper) which ships with this repository.

# Config
The config files for camera calibration and tracking hyper paramters from the original implementation are replaced with ros paramters which get set from a launch file.

## ROS parameters, topics and services
### Parameters
There are three types of parameters right now: static- and dynamic ros parameters and camera settings.
The static parameters are send to the ROS parameter server at startup and are not supposed to change. They are set in the launch files which are located at ros/launch. The parameters are:

- **load_map**: Bool. If set to true, the node will try to load the map provided with map_file at startup.
- **map_file**: String. The name of the file the map is loaded from.
- **voc_file**: String. The location of config vocanulary file mentioned above.
- **publish_pointcloud**: Bool. If the pointcloud containing all key points (the map) should be published.
- **publish_pose**: Bool. If a PoseStamped message should be published. Even if this is false the tf will still be published.
- **pointcloud_frame_id**: String. The Frame id of the Pointcloud/map.
- **camera_frame_id**: String. The Frame id of the camera position.
- **load_calibration_from_cam**: Bool. If true, camera calibration is read from a `camera_info` topic. Otherwise it is read from launch file params.

Dynamic parameters can be changed at runtime. Either by updating them directly via the command line or by using [rqt_reconfigure](http://u.720life.cn/g/214cba4ede9838afaceac6b9476b8794fce4d207ac20a2f6c5fca61187bd3898deff4c618892f488815d47a2a0f38c75)  which is the recommended way.
The parameters are:

- **localize_only**: Bool. Toggle from/to only localization. The SLAM will then no longer add no new points to the map.
- **reset_map**: Bool. Set to true to erase the map and start new. After reset the parameter will automatically update back to false.
- **min_num_kf_in_map**: Int. Number of key frames a map has to have to not get reset after tracking is lost.
- **min_observations_for_ros_map**: Int. Number of minimal observations a key point must have to be published in the point cloud. This doesn't influence the behavior of the SLAM itself at all.

Finally, the intrinsic camera calibration parameters along with some hyperparameters can be found in the specific yaml files in orb_slam2/config.

### Published topics
The following topics are being published and subscribed to by the nodes:
- All nodes publish (given the settings) a **PointCloud2** containing all key points of the map.
- Also all nodes publish (given the settings) a **PoseStamped** with the current pose of the camera.
- Live **image** from the camera containing the currently found key points and a status text.
- A **tf** from the pointcloud frame id to the camera frame id (the position).

### Subscribed topics
- The mono node subscribes to:
    - **/camera/image_raw** for the input image
    - **/camera/camera_info** for camera calibration (if `load_calibration_from_cam`) is `true`

- The RGBD node subscribes to:
    - **/camera/rgb/image_raw** for the RGB image
    - **/camera/depth_registered/image_raw** for the depth information
    - **/camera/rgb/camera_info** for camera calibration (if `load_calibration_from_cam`) is `true`

- The stereo node subscribes to:
    - **image_left/image_color_rect** and
    - **image_right/image_color_rect** for corresponding images
    - **image_left/camera_info** for camera calibration (if `load_calibration_from_cam`) is `true`

# 4. Services
All nodes offer the possibility to save the map via the service node_type/save_map.
So the save_map services are:
- **/orb_slam2_rgbd/save_map**
- **/orb_slam2_mono/save_map**
- **/orb_slam2_stereo/save_map**

The save_map service expects the name of the file the map should be saved at as input.

At the moment, while the save to file takes place, the SLAM is inactive.

# 5. Run
After sourcing your setup bash using
```
source devel/setup.bash
```
## Suported cameras
| Camera               | Mono                                                           | Stereo                                                           | RGBD                                                       |
|----------------------|----------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------|
| Intel RealSense r200 | ``` roslaunch orb_slam2_ros orb_slam2_r200_mono.launch ```     | ``` roslaunch orb_slam2_ros orb_slam2_r200_stereo.launch ```     | ``` roslaunch orb_slam2_ros orb_slam2_r200_rgbd.launch ``` |
| Intel RealSense d435 | ``` roslaunch orb_slam2_ros orb_slam2_d435_mono.launch ```     | -                                                                | ``` roslaunch orb_slam2_ros orb_slam2_d435_rgbd.launch ``` |
| Mynteye S            | ```roslaunch orb_slam2_ros orb_slam2_mynteye_s_mono.launch ``` | ```roslaunch orb_slam2_ros orb_slam2_mynteye_s_stereo.launch ``` | -                                                          |                     |                                                            |                                                              |                                                            |

Use the command from the corresponding cell for your camera to launch orb_slam2_ros with the right parameters for your setup.

# 6. Docker
An easy way is to use orb_slam2_ros with Docker. This repository ships with a Dockerfile based on ROS kinetic.
The container includes orb_slam2_ros as well as the Intel RealSense package for quick testing and data collection.

# 7. FAQ
Here are some answers to frequently asked questions.
### How to save the map
To save the map with a simple command line command run one the commands (matching to your node running):
```
rosservice call /orb_slam2_rgbd/save_map map.bin
rosservice call /orb_slam2_stereo/save_map map.bin
rosservice call /orb_slam2_mono/save_map map.bin
```
You can replace "map.bin" with any file name you want.
The file will be saved at ROS_HOME which is by default ~/.ros

**Note** that you need to source your catkin workspace in your terminal in order for the services to become available.

### Using a new / different camera
You can use this SLAM with almost any mono, stereo or RGBD cam you want.
In order to use this with a different camera you need to supply a set of paramters to the algorithm. They are loaded from a launch file from the ros/launch folder.
1) You need the **camera intrinsics and some configurations**. [Here](http://u.720life.cn/g/1aab72e505bd64910b029a0d957a58dd7b415253edaf6c5fe4d7b90a456a9844d0deab7dfda987f029f49f23e5312c95645349936312068c79f7edbfb3813931e9b9a27522ee7f7b0c043d6ff1bc0435)  you can read about what the camera calibration parameters mean. Use [this](http://u.720life.cn/g/214cba4ede9838afaceac6b9476b8794c36825277ea6dd6ff68629e9b264f82a059b509fec52e6f0334cc7c1d0bd945a)  ros node to obtain them for your camera. If you use a stereo or RGBD cam in addition to the calibration and resolution you also need to adjust three other parameters: Camera.bf, ThDepth and DepthMapFactor.
2) **The ros launch file** which is at ros/launch needs to have the correct topics to subscribe to from the new camera.
**NOTE** If your camera supports this, orb_slam_2_ros can subscribe to the camera_info topic and read the camera calibration parameters from there.

### Problem running the realsense node
The node for the RealSense fails to launch when running
```
roslaunch realsense2_camera rs_rgbd.launch
```
to get the depth stream.
**Solution:**
install the rgbd-launch package with the command (make sure to adjust the ROS distro if needed):
```
sudo apt install ros-melodic-rgbd-launch
```



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)