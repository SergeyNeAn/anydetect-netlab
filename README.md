# Netlab Installation Guide

Step 1: Check and Install pip on Ubuntu
First, ensure that pip is installed. You can check if it is already installed by running:
bash
pip --version
If pip is not installed, you can install it using the following command:
bash
sudo apt update
sudo apt install python3-pip

Step 2: Install Python
If Python is not already installed on your Ubuntu system, you can install it using:
bash
sudo apt update
sudo apt install python3

Step 3: Install Netlab
After ensuring that Python and pip are installed, you can install Netlab by running:
bash
python3 -m pip install networklab

Step 4: Add topology.yml
Add a topology.yml file in your project directory to define your network topology. This file should include the necessary configurations for your network devices and connections.

Step 5: Start Netlab
Once your topology.yml file is set up, you can start Netlab by executing:
bash
netlab up
This command will bring up the defined network topology and all its components.

Step 6: Install Softflowd
To install Softflowd, you can run the playbook softflowd_install.yml. This playbook automates the installation and configuration of Softflowd on the switch, which generates NetFlow packets for monitoring and analysis.
bash
ansible-playbook softflowd_install.yml

Step 7: Clone and Run
To clone the repository and run the required scripts, use the playbook clone_and_run.yml. This playbook handles cloning the repository from GitHub, copying it to the collector container, and making necessary modifications to configuration files.
bash
ansible-playbook clone_and_run.yml