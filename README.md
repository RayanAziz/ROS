How to install ROS

# Virtual Box
First, you need a Linux distribution such as Ubuntu. You can either install Ubuntu as a standalone system or on a virtual machine. We are going to do it Virtual Box, which can be downloaded from here: https://www.virtualbox.org/wiki/Downloads

# Install Ubuntu 20.04 on Virtual Box
1) Download Ubuntu Desktop 20.04 from: https://ubuntu.com/download/
2) In Virtual Box: New > Type: Linux, Version: Ubuntu 64-bit > Memory size = your PC's memory size / 4 > Create a virtual hard disk now > VDI > Dynamically allocated > 10 GB > Create
3) Start the the virtual machine you just created, you will be attemted to select a system file to boot from, select the Ubuntu ISO file you downloaded earlier.
4) Follow the on screen steps and let Ubuntu install itself.

# Install ROS
1) From inside Ubuntu, open the application drawer and run the Terminal.
2) In the terminal type the following commands:
sudo apt-get update
sudo apt-get upgrade
3) Run the following script which will download a ROS installation script, give it permissions to execute, and run it:
wget -c https://raw.githubusercontent.com/qboticslabs/ros_install_noetic/master/ros_install_noetic.sh && chmod +x ./ros_install_noetic.sh && ./ros_install_noetic.sh
3) You will be asked to select how much of ROS you want to be installed. Enter 2 and hit enter.
4) After the installation progress is done, close the terminal and open a new one and type:
rosversion -d
which should print noetic. That's how you know it was installed correctly.
