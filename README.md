CSC 541 Project 1 – Readme File 
Software Defined Network with Mininet Emulator and Ryu controller

Name – Jaspreet Singh & Susmita Patange
Student ID – 210555347 & 210551057
Email: fjaspreetsingh1@toromail.csudh.edu & spatange1@toromail.csudh.edu
Github: https://github.com/JaspreetToro/ofworkspace

Steps to execute the program:
1.	Extract the zip file. 
2.	Open two terminal windows
3.	cd ofworkspace/mininet-topologies
4.	copy simple_controller.py, binary_coontroller.py & fat_tree_controller.py in the ~/ryu/app folder. 

Programming Task 1: 
1.	Type on the first terminal window. 
ryu-manager ryu.app.simple_controller ryu.app.ofctl_rest

 

2.	Type on second terminal window
sudo mn --custom simple.py --topo minimal --mac --switch ovs --controller remote

 

3.	Use the command to access the network connectivity

a)	Net
b)	Nodes
c)	Pingall

 
 

Programming Task 2:
1.	Type on the first terminal window. 
ryu-manager ryu.app.binary_tree_controller ryu.app.ofctl_rest

 

2.	Type on the second terminal window
sudo mn --custom binary_tree.py --topo dcbasic --mac --switch ovs --controller remote










 

3.	Use the command to access the network connectivity

a)	Net
b)	Nodes
c)	Pingall 

 
 
 

Programming Task 3: 
1.	Type on the first terminal window. 
ryu-manager ryu.app.fat_tree_controller ryu.app.ofctl_rest

 
2.	Type on the second terminal window
sudo mn --custom fat_tree.py --topo fattree --switch ovs --controller remote

 

 

4.	Use the command to access the network connectivity

a)	Net
b)	Nodes
c)	as_0_0 ping -c 1 cs_0, es_0_1 ping -c 1 as_0_1, es_3_0 ping -c 1 h_3_0_1

 
 
 

Note: In case of an error use the following commands:
1.	If mininet is already running.

sudo mn -c

2.	If open switch service is not starting, then do force start.

service openvswitch-switch start

3.	Task 1: Since rest api is used for controller, no need to mention the ip address explicitly.
Task 3: Since the path is hard coded for shortest path, please follow the one to one connection, as it there in the fat tree topology (48 links).

Contribution of the group member 1 (Jaspreet Singh):
1.	Installation of Ubuntu machine in VMware. 
2.	Installation of Mininet. 
3.	Installation of Ryu controller. 
4.	Code for implementing the project task:
a)	Packet transfer with IP Address.
b)	Binary Tree.
c)	Fat Tree. 
Contribution of the group member 2 (Susmita Patange):
1.	Installation of VMware in windows machine. 
2.	Installation of IDE Atom. 
3.	Research for OpenFlow controller and custom Mininet topologies.
4.	Code Implementation for controller
a)	Simple controller
b)	Binary controller
c)	Fat tree controller


