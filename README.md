# ROS Noetic 环境搭建作业
GitHub用户名：fox439922

## 一、安装步骤
1. 安装vmware虚拟机，搭建Ubuntu 20.04 LTS，完成系统基础配置。
2. 添加ROS Noetic软件源与GPG密钥，执行apt update更新软件包索引。
3. 安装ros-noetic-desktop-full完整版ROS。
4. 将ROS环境变量写入~/.bashrc，执行source生效环境。
5. 安装rosdep、rosinstall等工具，执行sudo rosdep init与rosdep update。
6. 环境校验：lsb_release -a确认Ubuntu版本；rospack校验ROS Noetic安装成功。
7. 小海龟测试：终端依次启动roscore、turtlesim_node、turtle_teleop_key，使用键盘方向键控制海龟移动。

## 二、遇到的问题与解决办法
1. 问题：执行sudo rosdep init时网络超时，无法连接外网。
解决：更换国内rosdep镜像源，修改对应的源文件后重新执行rosdep update。
2. 问题：按下方向键，小海龟不移动。
解决：必须将鼠标焦点选中turtle_teleop_key所在终端窗口，方向键才会生效。
3. 问题：新开终端无法找到roscore等ROS命令。
解决：确认已经把source /opt/ros/noetic/setup.bash写入.bashrc，重新source环境。
4.问题：环境配置超时。
解决：确认虚拟机时间，改为与主机时间一致。

## 文件说明
1.Ubuntu20.04与ROS Noetic版本截图。
2.20~30秒小海龟键盘控制移动录屏。
