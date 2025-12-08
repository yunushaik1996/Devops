Ansible is an open-source automation and configuration management tool.
It helps us to:

Install and configure software
Manage servers and infrastructure
Deploy applications efficiently.

Ansible is an agentless server works on push based mechanism it supports n number of plugins developed in python language. 

Ansible uses protocol ssh (22)

Example Scenario
We have 100 servers and we need to install Nginx on all 100 servers.

 Without Ansible
	• We must log in to each server manually
	• Run installation commands one by one
	• This is slow, repetitive, and time-consuming

With Ansible
	• We write one playbook
	• Run it once from the Ansible control machine
	• Ansible automatically installs Nginx on all 100 servers at the same time.



Use cases:
 
	1. Uptime --> Shows how long the system has been running
	2. Ping --> Used to check connectivity with a server 
	3. Find / -name fine name --> To find a file anywhere


Note:
Common username for all the servers
Password less authentication

If all the 100 servers having different passwords it's very difficult to connect 
Make sure to use same user name (common user)
We can use easy ansible as a configuration management tool.


Other configuration management tools:

Chef --> Pull based 
Puppet --> Pull based
Salt stack  --> Pull based 

<img width="880" height="560" alt="Ansibleimage" src="https://github.com/user-attachments/assets/c43d0a42-bc3f-4dcf-9e2a-c4d7759c1e5b" />


Push-Based Model

 Control happens from the central server
 Server pushes configurations/updates to target nodes
 Nodes wait for instructions

Controller → Push configuration → Target Machines

Pull-Based Model

Nodes pull configurations from a central server
Each server checks for updates and applies them on schedule

Target Machines → Pull config → Central Server



Ansible Components 








<img width="1328" height="2794" alt="image" src="https://github.com/user-attachments/assets/360c7f49-06c5-4c7a-8831-5fb80483b1cb" />
