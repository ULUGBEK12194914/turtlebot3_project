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
# SBC Setup
#Prepare microSC Card and Reader

#Download TurtleBot3 SBC Image
https://www.robotis.com/service/download.php?no=2064

#Burn the image file with the Rapsberry Pi Imager
https://www.raspberrypi.org/software/
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.35.09.png?raw=true)
#Resize the Partition
```bash
ulugbekmirzabakhromov@ubuntu:~$ sudo apt install gparted

#Open GParted and resize the Partition
ulugbekmirzabakhromov@ubuntu:~$ gparted
```
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.32.09.png)
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.33.40.png)
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.34.15.png)
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.34.27.png)
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.34.47.png)
# Configure the WIFI settings
```bash
----------------------------
ubuntu@ubuntu:~$ cd /media/ubuntu/writable/etc/netplan/

#Edit the yaml file with a superuser permission 'sudo'. When the editor is opened, replace WIFI_SSID and WIFI_PASSWORD with your SSID and password
----------------------------------
ubuntu@ubuntu:/media/ubuntu/writable/etc/netplan$ sudo nano 50-cloud-init. yaml
```
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.43.53.png)
#Turtlebot configuration
```bash
#Boot up the Raspberry Pi(Connect the Raspberry Pi using micro hdmi to the Monitor)
#Insert the microSD card
#Login with ID 'ubuntu' and Password 'turtlebot'
```
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.36.52.png)
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.36.38.png)
# ROS2 Network Configuration
#The default ROS DOMAIN ID for Turtlebot3 is set to 30 in the .bashrc file.Please modify the ID.
```bash
#Add the following code inside the bashrc file(both in computer and turtlebot)
ROS_DOMAIN_ID=30 #TURTLEBOT3
```
#In your terminal type the command
```bash
ubuntu@ubuntu:~$ ssh 'ip_address'
```
![](https://github.com/ULUGBEK12194914/turtlebot3_project/blob/main/images/Screenshot%202022-11-02%20at%2015.36.27.png)
