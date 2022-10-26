# turtlebot3_project(FOXY VERSION)
###Smart mobility engineering(working with turtlebot3)

#Install ROS on Remote PC
----------------------------
```bash
#Make sure your system is up-to-date
ulugbekmirzabakhromov@ubuntu:~$ sudo apt update
[sudo] password for ulugbekmirzabakhromov: 
Hit:1 http://packages.ros.org/ros/ubuntu focal InRelease                       
Hit:2 http://us.archive.ubuntu.com/ubuntu focal InRelease                      
Get:3 http://security.ubuntu.com/ubuntu focal-security InRelease [114 kB]
Hit:4 https://dl.google.com/linux/chrome/deb stable InRelease                  
Hit:5 http://packages.ros.org/ros2/ubuntu focal InRelease                      
Get:6 http://us.archive.ubuntu.com/ubuntu focal-updates InRelease [114 kB]     
Get:7 http://security.ubuntu.com/ubuntu focal-security/main amd64 DEP-11 Metadata [40.7 kB]
.............
ulugbekmirzabakhromov@ubuntu:~$ sudo apt upgrade -y
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Calculating upgrade... Done
The following package was automatically installed and is no longer required:
  libxmlb1
Use 'sudo apt autoremove' to remove it.
The following NEW packages will be installed:
  libxmlb2 linux-headers-5.15.0-52-generic linux-h
  ...............
  
#Download ROS foxy installation scripts
---------------------------------------
ulugbekmirzabakhromov@ubuntu:~$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros2_foxy.sh

#Run the script file
----------------------
ulugbekmirzabakhromov@ubuntu:~$ sudo chmod 755 ./install_ros2_foxy.sh
ulugbekmirzabakhromov@ubuntu:~$ bash ./install_ros2_foxy.sh

#Install ROS Packages
ulugbekmirzabakhromov@ubuntu:~$ sudo apt-get install ros-foxy-gazebo-*
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-cartographer
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-cartographer-ros
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-navigation2
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-nav2-bringup
ulugbekmirzabakhromov@ubuntu:~$source ~/.bashrc

#Install Turtlebot3 via Debian Packages
----------------------------------------
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-dynamixel-sdk
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-turtlebot3-msgs
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install ros-foxy-turtlebot3

#Environmen configuration
---------------------------
ulugbekmirzabakhromov@ubuntu:~$ echo 'export ROS_DOMAIN_ID=30 #TURTLEBOT3' >> ~/.bashrc
ulugbekmirzabakhromov@ubuntu:~$ source ~/.bashrc
```
#SBC Setup
## Prepare microSC Card and Reader
## Download TurtleBot3 SBC Image
![]()
#Resize the Partition
```bash
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install gparted

#Open GParted and resize the Partition
ulugbekmirzabakhromov@ubuntu:~$ gparted
```
![]()
```bash
#Configure the WIFI settings
----------------------------
ubuntu@ubuntu:~$ cd /media/ubuntu/writable/etc/netplan/
ubuntu@ubuntu:/media/ubuntu/writable/etc/netplan$ sudo nano 50-cloud-init. yaml
```
![]()
```bash
#Boot up the Raspberry Pi(Connect the Raspberry Pi to the Monitor)
#Insert the microSD card
#Login with ID 'ubuntu' and Password 'turtlebot'

