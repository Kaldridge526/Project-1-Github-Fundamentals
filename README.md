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
