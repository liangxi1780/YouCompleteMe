# IAI Kinect2

## Maintainer

- [Thiemo Wiedemeyer](http://u.720life.cn/g/92657b56d6dda1a06a8c653f2a9e1ba084e9f6d089b1e5de907d2cea6111b6f25184ac47674d417d7b411202d9c40da5)   >, [Institute for Artificial Intelligence](http://u.720life.cn/g/5f365e406c94cb3e913c992abf0e067d20cf1bd2a79f92c249aa7f8ce94e74a6  University of Bremen

## Read this first

Please read this README and the ones of the individual components throughly before asking questions. We get a lot of repeated questions, so when you have a problem, we urge everyone to check the [github issues  (including closed ones)](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dfe5d3c061cdd0a44234525878551862fb9da0c4bdfdfd85d1394fa38446ec3fd39978bf93c83148003118b4b4f3bd82f6dce440367aa96bd7479e1fcf0973d8  Your issue is very likely discussed there already.

The goal of this project is to give you a driver and the tools needed to receive data from the Kinect-2 sensor, in a way useful for robotics. You will still need to know how to use ROS to make use of it. Please follow the [ROS tutorials](http://u.720life.cn/g/214cba4ede9838afaceac6b9476b87941618bc93246437f3341705128ecfefdee4100d73ac1955678ebc2ca5e1f6e0f6  You will also need to learn how to work with point-clouds, or depth-clouds, or images (computer vision) to do useful things with the data.

*Note:* ***Please use the GitHub issues*** *for questions and problems regarding the iai_kinect2 package and its components.* ***Do not write emails.***

## Table of contents
- [Description](#description)
- [FAQ](#faq)
- [Dependencies](#dependencies)
- [Install](#install)
- [GPU acceleration](#gpu-acceleration)
  - [OpenCL with AMD](#opencl-with-amd)
  - [OpenCL/CUDA with Nvidia](#openclcuda-with-nvidia)
  - [OpenCL with Intel](#opencl-with-intel)
- [Citation](#citation)
- [Screenshots](#screenshots)

## Description

This is a collection of tools and libraries for a ROS Interface to the Kinect One (Kinect v2).

It contains:
- [a calibration tool](kinect2_calibration) for calibrating the IR sensor of the Kinect One to the RGB sensor and the depth measurements
- [a library](kinect2_registration) for depth registration with OpenCL support
- [the bridge](kinect2_bridge) between [libfreenect2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d82c653a0c142518fe673bc215ab762622e06d8efd9ce6067255794f026d027)  and [ROS](http://u.720life.cn/g/e5c747114f07c28aa5e627404392ff8439eaa6d2f053124bea465e0ecc41dd41) 
- [a viewer](kinect2_viewer) for the images / point clouds

## FAQ

#### If I have any question or someting is not working, what should I do first?

First you should look at this FAQ and the [FAQ from libfreenect2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d82c653a0c142518fe673bc215ab76237de60af2265d3b8ad2d82a054a6554a 
Secondly, look at [issue page from libfreenect2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d82c653a0c142518fe673bc215ab762c79151e1bac82404acb77ebe24e85b1412ae1928b66d91ed3bfb037d59e5f213)  and
the [issue page of iai_kinect2](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dfe5d3c061cdd0a44234525878551862d829a8677a384d42074acbe9fa2b0493)  for similar issues and solutions.

#### Point clouds are not being published?

Point clouds are only published when the launch file is used. Make sure to start kinect2_bridge with `roslaunch kinect2_bridge kinect2_bridge.launch`.

#### Will it work with OpenCV 3.0

Short answer: No.

Long answer: Yes, it is possible to compile this package with OpenCV 3.0, but it will not work.
This is because cv_bridge is used, which itself is compiled with OpenCV 2.4.x in ROS Indigo/Jade and
linking against both OpenCV versions is not possible. Working support for OpenCV 3.0 might come with a future ROS release.

#### kinect2_bridge is not working / crashing, what is wrong?

There are many reasons why `kinect2_bridge` might not working. The first thing to find out whether the problem is related to `kinect2_bridge` or `libfreenect2`.
A good tool for testing is `Protonect`, it is a binary located in `libfreenect2/build/bin/Protonect`.
It uses libfreenect2 directly with a minimal dependency on other libraries, so it is a good tool for the first tests.

Execute:
- `./Protonect gl` to test OpenGL support.
- `./Protonect cl` to test OpenCL support.
- `./Protonect cpu` to test CPU support.

Before running `kinect2_bridge` please make sure `Protonect` is working and showing color, depth and ir images.
If some of them are black, than there is a problem not related to `kinect2_bridge` and you should look at the issues from the libfreenect2 GitHub page for help.

If one of them works, try out the one that worked with `kinect2_bridge`: `rosrun kinect2_bridge kinect2_bridge _depth_method:= `.
You can also change the registration method with `_reg_method:= `.

#### Protonect works fine, but kinect2_bridge is still not working / crashing.

If that is the case, you have to make sure that `Protonect` uses the same version of `libfreenect2` as `kinect2_bridge` does.
To do so, run `make` and `sudo make install` in the build folder again. And try out `kinect2_bridge` again.

```bash
cd libfreenect2/build
make & sudo make install
```

Also make sure that you are not using OpenCV 3.0.

If it is still crashing, compile it in debug and run it with gdb:

```bash
cd  
catkin_make -DCMAKE_BUILD_TYPE="Debug"
cd devel/lib/kinect2_bridge
gdb kinect2_bridge
# inside gdb: run until it crashes and do a backtrace
run
bt
quit
```

Open an issue and post the problem description and the output from the backtrace (`bt`).

#### kinect2_bridge hangs and prints "waiting for clients to connect"

This is the normal behavior. 'kinect2_bridge' will only process data when clients are connected (ROS nodes listening to at least one of the topics).
This saves CPU and GPU resources. As soon as you start the `kinect_viewer` or `rostopic hz` on one of the topics, processing should start.

#### rosdep: Cannot locate rosdep definition for [kinect2_bridge] or [kinect2_registration]

`rosdep` will output errors on not being able to locate `[kinect2_bridge]` and `[kinect2_registration]`.
That is fine because they are all part of the iai_kinect2 package and `rosdep` does not know these packages.

#### Protonect or kinect2_bridge outputs [TransferPool::submit] failed to submit transfer

This indicates problems with the USB connection.

#### I still have an issue, what should I do?

First of all, check the issue pages on GitHub for similar issues, as they might contain solutions for them.
By default you will only see the open issues, but if you click on `closed` you will the the ones solved. There is also a search field which helps to find similar issues.

If you found no solution in the issues, feel free to open a new issue for your problem. Please describe your problem in detail and provide error messages and log output.

## Dependencies

- ROS Hydro/Indigo
- OpenCV (2.4.x, using the one from the official Ubuntu repositories is recommended)
- PCL (1.7.x, using the one from the official Ubuntu repositories is recommended)
- Eigen (optional, but recommended)
- OpenCL (optional, but recommended)
- [libfreenect2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d82c653a0c142518fe673bc215ab762622e06d8efd9ce6067255794f026d027)  (>= v0.2.0, for stability checkout the latest stable release)

## Install

1. Install the ROS. [Instructions for Ubuntu 14.04](http://u.720life.cn/g/214cba4ede9838afaceac6b9476b879402c8d19cb90f0cc250b5fb6711047c8f78a26b67f9d9852ac51858b9a2e41fa5) 
2. [Setup your ROS environment](http://u.720life.cn/g/214cba4ede9838afaceac6b9476b87941618bc93246437f3341705128ecfefdea2792636e54c3d28500b28008e5acf007bc1cbd0ecc21fe20d19398afd23448bf7113f82991528950f346917d7a300a7) 
3. Install [libfreenect2](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d82c653a0c142518fe673bc215ab762ef4009aa4d6cf0723bf33c8069bce354 

   Follow [the instructions](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468d82c653a0c142518fe673bc215ab7623d0bb585ce743eecafa006f8c31b36e8866ba38f6489b01a6adc9fcc9d01a05b)  and enable C++11 by using `cmake .. -DENABLE_CXX11=ON` instead of `cmake ..`. If you are compiling libfreenect2 with CUDA, use `cmake .. -DENABLE_CXX11=ON -DCUDA_PROPAGATE_HOST_FLAGS=off`.

   If something is not working, check out the latest stable release, for example `git checkout v0.2.0`.

4. Clone this repository into your catkin workspace, install the dependencies and build it:

    ```bash
    cd ~/catkin_ws/src/
    git clone https://github.com/code-iai/iai_kinect2.git
    cd iai_kinect2
    rosdep install -r --from-paths .
    cd ~/catkin_ws
    catkin_make -DCMAKE_BUILD_TYPE="Release"
    ```

   *Note: `rosdep` will output errors on not being able to locate `[kinect2_bridge]` and `[depth_registration]`.
   That is fine because they are all part of the iai_kinect2 package and `rosdep` does not know these packages.*

   *Note: If you installed libfreenect2 somewhere else than in `$HOME/freenect2` or a standard location like `/usr/local`
   you have to specify the path to it by adding `-Dfreenect2_DIR=path_to_freenect2/lib/cmake/freenect2` to `catkin_make`.*

5. Connect your sensor and run `kinect2_bridge`:

    ```bash
    roslaunch kinect2_bridge kinect2_bridge.launch
    ```

6. Calibrate your sensor using the `kinect2_calibration`. [Further details](kinect2_calibration#calibrating-the-kinect-one)
7. Add the calibration files to the `kinect2_bridge/data/ ` folder. [Further details](kinect2_bridge#first-steps)
8. Restart `kinect2_bridge` and view the results using `rosrun kinect2_viewer kinect2_viewer kinect2 sd cloud`.

## GPU acceleration

### OpenCL with AMD

Install the latest version of the AMD Catalyst drivers from https://support.amd.com and follow the instructions. Also install `opencl-headers`.

```bash
sudo apt-get install opencl-headers
```

### OpenCL/CUDA with Nvidia

Go to [developer.nvidia.com/cuda-downloads](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484fd1e6f42e23c223dd2569a2f11f17fae69475c14e4b28977ad02c85eabcf6e05)  and select `linux`, `x86_64`, `Ubuntu`, `14.04`, `deb(network)`.
Download the file and follow the instructions. Also install `nvidia-modprobe` and `opencl-headers`.

```bash
sudo apt-get install nvidia-modprobe opencl-headers
```

You also need to add CUDA paths to the system environment, add these lines to you `~/.bashrc`:

```bash
export LD_LIBRARY_PATH="/usr/local/cuda/lib64:${LD_LIBRARY_PATH}"
export PATH="/usr/local/cuda/bin:${PATH}"
```

A system-wide configuration of the libary path can be created with the following commands:

```bash
echo "/usr/local/cuda/lib64" | sudo tee /etc/ld.so.conf.d/cuda.conf
sudo ldconfig
```

### OpenCL with Intel

You can either install a binary package from a PPA like [ppa:floe/beignet](http://u.720life.cn/g/50427b74640a5a0d7a20b955d81e1ca3a28323e71fba61febc348e3341f0b818f435599b684d178c783e4c03f51bae2acfb1dce99ae69cbe9e46e501c0448069  or build beignet yourself.
It's recommended to use the binary from the PPA.

```bash
sudo add-apt-repository ppa:floe/beignet && sudo apt-get update
sudo apt-get install beignet beignet-dev opencl-headers
```

## Citation

If you used `iai_kinect2` for your work, please cite it.

```tex
@misc{iai_kinect2,
  author = {Wiedemeyer, Thiemo},
  title = {{IAI Kinect2}},
  organization = {Institute for Artificial Intelligence},
  address = {University Bremen},
  year = {2014 -- 2015},
  howpublished = {\url{https://github.com/code-iai/iai\_kinect2}},
  note = {Accessed June 12, 2015}
}
```

The result should look something similar to this (may depend on the bibliography style used):

```
T. Wiedemeyer, “IAI Kinect2,” https://github.com/code-iai/iai_kinect2,
Institute for Artificial Intelligence, University Bremen, 2014 – 2015,
accessed June 12, 2015.
```

## Screenshots

Here are some screenshots from our toolkit:
![color image](http://ai.uni-bremen.de/wiki/_media/software/kinect2_color.jpg)
![depth image](http://ai.uni-bremen.de/wiki/_media/software/kinect2_depth_colored.png)
![point cloud](http://ai.uni-bremen.de/wiki/_media/software/kinect2_cloud.png)
![image viewer](http://ai.uni-bremen.de/wiki/_media/software/kinect2_viewer.png)




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)