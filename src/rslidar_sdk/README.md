# rslidar_sdk for Airy / E1R

Modified from [rslidar_sdk](https://github.com/RoboSense-LiDAR/rslidar_sdk).

## 1 What modified
### 1.1 config
Added `airy_config.yaml` and `e1r_config.yaml`.
### 1.2 launch
RViz window in all launch files has been disabled by default.
Added `airy_start.launch` and `e1r_start.launch`.
### 1.3 CMakeLists.txt
In line 8, `Custom Point Type` has been changed to `XYZIRT`, `ring` and `timestamp` added.
In line 48, `ENABLE_IMU_DATA_PARSE` has been turned on by default for imu messages.

## 2 Download
Download the rslidar_sdk as below. Since it contains the submodule rs_driver, please also download the submodule by
```sh
git clone https://github.com/Lya-M1RA/rslidar_sdk.git
cd rslidar_sdk
git submodule init
git submodule update
```
or
```sh
git clone https://github.com/Lya-M1RA/rslidar_sdk.git --recursive
```
## 3 Dependencies
```sh
sudo apt-get install -y libyaml-cpp-dev libpcap-dev
```
## 4 More details
For more details, please refer to the original [README](https://github.com/Lya-M1RA/rslidar_sdk/blob/main/README_EN.md) of rslidar_sdk.