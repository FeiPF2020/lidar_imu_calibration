# LiDAR_IMU_Init  
Modified from [LiDAR_IMU_Init](https://github.com/hku-mars/LiDAR_IMU_Init) for RoboSense lidars.    


## 1 What modified  
### 1.1 config  
Added `robosense_airy.yaml` and `robosense_e1r.yaml`.  

### 1.2 preprocess
Added support for robosense point struct in `preprocess.h`.

### 1.3 launch
Added `robosense_airy.launch` and `robosense_e1r.launch`.

## 2 Download  
Download the `LiDAR_LiDAR_IMU_Init` as below.  
```sh
git clone https://github.com/Lya-M1RA/LiDAR_IMU_Init.git
```

## 3 Prerequisites  
### 3.1 Ubuntu and ROS
Ubuntu >= 18.04  

ROS    >= Melodic. [ROS Installation](http://wiki.ros.org/ROS/Installation)

### 3.2 PCL && Eigen
PCL    >= 1.8,   Follow [PCL Installation](http://www.pointclouds.org/downloads/linux.html).

Eigen  >= 3.3.4, Follow [Eigen Installation](http://eigen.tuxfamily.org/index.php?title=Main_Page).

```sh
sudo apt install libpcl-dev libeigen3-dev
```

### 3.3 livox_ros_driver
Follow [livox_ros_driver Installation](https://github.com/Livox-SDK/livox_ros_driver).

*Remarks:*
- Since the LiDAR_IMU_Init must support Livox serials LiDAR firstly, so the **livox_ros_driver** must be installed and **sourced** before run any LiDAR_IMU_Init launch file.
- How to source? The easiest way is add the line ``` source $Livox_ros_driver_dir$/devel/setup.bash ``` to the end of file ``` ~/.bashrc ```, where ``` $Livox_ros_driver_dir$ ``` is the directory of the livox ros driver workspace (should be the ``` ws_livox ``` directory if you completely followed the livox official document).

### 3.4 ceres-solver
The code has been tested on ceres-solver-2.0.0. Please download [ceres-solver-2.0.0](https://github.com/hku-mars/LiDAR_IMU_Init/releases/download/v1.0/ceres-solver-2.0.0.zip) and finish the  installation following the [instructions](http://ceres-solver.org/installation.html#linux).

## 5 More details
For more details, please refer to the original [README](https://github.com/Lya-M1RA/LiDAR_IMU_Init/blob/main/README_ORIGIN.md) of LiDAR_IMU_Init.