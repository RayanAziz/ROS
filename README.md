How to install ROS

# Virtual Box
First, you need a Linux distribution such as Ubuntu. You can either install Ubuntu as a standalone system or on a virtual machine. We are going to do it Virtual Box, which can be downloaded from here: https://www.virtualbox.org/wiki/Downloads
![ROS](/img/1.png)

# Install Ubuntu 20.04 on Virtual Box
1. Download Ubuntu Desktop 20.04 from: https://ubuntu.com/download/desktop
2. Install Virtual Box and run it.
  - Click on New.
  - Type: Linux, Version: Ubuntu 64-bit.
  - Memory size = your PC's memory size / 4.
  - Create a virtual hard disk now.
  - VDI.
  - Dynamically allocated.
  - 10 GB and click on create.

3. Start the the virtual machine you just created, you will be attemted to select a system file to boot from, select the Ubuntu ISO file you downloaded earlier.

4. Follow the on screen steps.
  - Choose Install Ubuntu.
  - Proceed with the intuitive installation process. You will only change the installation type to minimal, the rest should remain on the default selections and not changed.
  - Let Ubuntu install itself.
  - Restart Ubuntu.

# Install ROS
1. From inside Ubuntu, open the application drawer and run the Terminal.
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
4. After the installation progress is done, close the terminal and open a new one and type:
```shell
rosversion -d
```
which should print *noetic*. That's how you know it was installed correctly.
