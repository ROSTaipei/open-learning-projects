# DA Lamp Learning Logs

## How to load URDF

機器檯燈的機構屬於 closed-loop chain 的四連桿（four-bar linkage）運動，而目前 URDF 內建的解析運動的 library 為 KDL，只支援樹狀結構。

#### 相關討論串
* [Support circular joint chains in spec](https://github.com/ros/urdf/issues/13)（來自 Github 中 ROS 官方的 URDF repository Issues）
* [[URDF-NG] ROS2 URDF2 discussion](https://discourse.ros.org/t/urdf-ng-ros2-urdf2-discussion/511/35)（ROS 官方 discourse 討論串）

### Potential Solutions

* 使用 URDF，但不利用內建的 KDL forward kinematics 去模擬，自己寫 Kinematics！
* 不要使用 URDF，改用 SDF 描述機器人，並搭配 Gazebo 模擬，找找有沒有工具（e.g. [Gazebo2Rviz](http://wiki.ros.org/gazebo2rviz)）可以串回 Rviz。
* 研究 SRDF?

## How to calibrate

現階段的版本是直接控制
