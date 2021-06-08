# UTCyber
Project 1 

Network diagram link: https://drive.google.com/file/d/1d3sAHRrZwP6awFRDAJ-Uuy-Nug82TUhh/view?usp=sharing
  
## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![TODO: Update the path with the name of your diagram](https://drive.google.com/file/d/1d3sAHRrZwP6awFRDAJ-Uuy-Nug82TUhh/view?usp=sharing)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the playbook file may be used to install only certain pieces of it, such as Filebeat.

  - _TODO: Enter the playbook file._

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly responsive, in addition to restricting access to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_
--They protect systems from DDoS attacks through shifting attacking traffic.  The advantage is that the user has access from a single node that can be secure and monitored.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the jumpbox and system network.
- _TODO: What does Filebeat watch for?_ Watches for any information in the file system that has been changed.
- _TODO: What does Metricbeat record?_ Takes the metrics and stats and puts them to the output specified by the user.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.4   | Linux            |
| Web-1     |Server   |  10.0.0.5  |Linux                |
| Web-2     |Server   |  10.0.0.5  |Linux                 |
| Web-3     |Server   |  10.0.0.7  |Linux                  |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the virtual machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_10.0.0.208

Machines within the network can only be accessed by JumpBox.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_JumpBoxProvisioner VM: IP- 10.0.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 10.0.0.208     |
| Web-1    |  No                 | 10.0.0.4       |
| Web-2    |  No                 | 10.0.0.4       |
| Web-3    |  No                 | 10.0.0.4       |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_The user can put commands into multiple servers from one playbook.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- Install: docker.io
-Install: python-pip
- Install: docker
- Launch docker container: elk

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance. Link to the VM is no longer running.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_VM1 10.0.0.5- VM3 10.0.0.7

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_Filebeat and metricbeat

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._Filebeay collects the changes and Metric beat collects metrics and statistics.

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:  

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running? Kibana link

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
