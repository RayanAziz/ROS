How to install ROS

# Virtual Box
First, you need a Linux distribution such as Ubuntu. You can either install Ubuntu as a standalone system or on a virtual machine. We are going to do it Virtual Box, which can be downloaded from here: https://www.virtualbox.org/wiki/Downloads

![ROS](/img/1.png)

# Install Ubuntu 20.04 on Virtual Box
1. Download Ubuntu Desktop 20.04 from: https://ubuntu.com/download/desktop

![ROS](/img/2.png)

2. Install Virtual Box and run it.
  - Click on New.
  
  ![ROS](/img/3.png)
  
  - Type: Linux, Version: Ubuntu 64-bit.
  
  ![ROS](/img/4.png)
  
  - Memory size = your PC's memory size / 4.
  
  ![ROS](/img/5.png)
  
  - Create a virtual hard disk now.
  
  ![ROS](/img/6.png)
  
  - VDI.
  
  ![ROS](/img/7.png)
  
  - Dynamically allocated.
  
  ![ROS](/img/8.png)
  
  - 10 GB and click on create.
  
  ![ROS](/img/9.png)

3. Start the the virtual machine you just created, you will be attemted to select a system file to boot from, select the Ubuntu ISO file you downloaded earlier.

![ROS](/img/10.png)

![ROS](/img/11.png)

4. Follow the on screen steps.
  - Choose Install Ubuntu.
  
  ![ROS](/img/12.png)
  
  - Proceed with the intuitive installation process. You will only change the installation type to minimal, the rest should remain on the default selections and not changed.
  
  ![ROS](/img/13.png)
  - Let Ubuntu install itself.
  
  ![ROS](/img/14.png)
  
  - Restart Ubuntu.
  
  ![ROS](/img/15.png)

# Install ROS
1. From inside Ubuntu, open the application drawer and run the Terminal.

![ROS](/img/16.png)

2. In the terminal type the following commands:
```shell
sudo apt-get update
sudo apt-get upgrade
 ```
 If an error is encountered during one of the commands, type:
 ```shell
 sudo apt --fix-broken install
 ```
3. Run the following script which will download a ROS installation script, give it permissions to execute, and run it:
```shell
wget -c https://raw.githubusercontent.com/qboticslabs/ros_install_noetic/master/ros_install_noetic.sh && chmod +x ./ros_install_noetic.sh && ./ros_install_noetic.sh
```
3. You will be asked to select how much of ROS you want to be installed. Enter 2 and hit enter.

![ROS](/img/17.png)

4. After the installation progress is done, close the terminal and open a new one and type:
```shell
rosversion -d
```
which should print *noetic*. That's how you know it was installed correctly.

![ROS](/img/18.png)
