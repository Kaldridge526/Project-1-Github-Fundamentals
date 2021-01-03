# Project-1-Github-Fundamentals
These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the Azure Cloud Environment file may be used to install only certain pieces of it, such as Filebeat.

Filebeat Playbook
This document contains the following details:

Description of the Topology
Access Policies
ELK Configuration
Beats in Use
Machines Being Monitored
How to Use the Ansible Build
Description of the Topology
The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly reliable, in addition to restricting access to the network.

Load Balancers protect against DoS attacks. The advantage of the jump box is that it restricts access to one administrator. Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the actual machines and system logs.
Filebeat helps generate and organize log files to send to Logstash and Elasticsearch. Specifically, it logs information about the file system, including which files have changed and when.
Metricbeat is a lightweight shipper that you can install on your servers to periodically collect metrics from the operating system and from services running on the server. Metricbeat takes the metrics and statistics that it collects and ships them to the output that you specify, such as Elasticsearch or Logstash.
The configuration details of each machine may be found below:

Access Policies
The machines on the internal network are not exposed to the public Internet.

Machines within the network can only be accessed by accessing the DVWA container in the Jump Box VM.
Elk Configuration
Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...

What is the main advantage of automating configuration with Ansible? Ansible allows you to easily scale your containers and manage them (instead of managing one at a time).
The playbook implements the following tasks:

TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
Install Docker
Install Pip3
Checks on memory space
Downloads and launces the Elk Docker Container

arget Machines & Beats
This ELK server is configured to monitor the following machines:

10.0.0.7
10.0.0.8
10.0.0.9
We have installed the following Beats on these machines:

Filebeats
Metricbeats
These Beats allow us to collect the following information from each machine:

Filebeats collect log data and changes made for the VMs. Filebeats can show IPs from inbound traffic, Geolocation, Requests being made, etc.
Metricbeats collects activity and status of the connected VMs. Here you can see CPU, memory usage, number of containers, etc.
Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:

SSH into the control node and follow the steps below:

Copy the Ansible file to etc/ansible once logged into Jumpbox>AnsibleVM.
Update the hosts file to include the webserver IP addresses and the webservers group
Run the playbook, and navigate to the Virtual Machine to check that the installation worked as expected.
TODO: Answer the following questions to fill in the blanks:

_Which file is the playbook? Ansible Playbook Where do you copy it? /etc/ansible
Which file do you update to make Ansible run the playbook on a specific machine? Hosts file.
How do I specify which machine to install the ELK server on versus which to install Filebeat on? Add a group in the hosts file for the ELK machine(s) and include the IP address(es).
Which URL do you navigate to in order to check that the ELK server is running? http://104.42.109.198:5601/app/kibana#/home/
