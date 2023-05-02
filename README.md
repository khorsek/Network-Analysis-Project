# Network-Analysis-Project

# The purpose of this project is to get acquainted with some of the intrusion detection tools that are available by way of an interactive session. I’ve used Wireshark in the past and I recall it being an especially useful tool for any cybersecurity user, its network analysis being immensely useful. 

# I first open a windows VM and begin by opening up a terminal by typing in “cmd” into the search tab and enter the command: “ipconfig” as seen below:
<img src="images\2.PNG">

# Now that I know the IP address for our system, 172.16.3.14, I can proceed to start Wireshark and begin the next step for this project.Now that Wireshark is up and running, I leave the virtual machine open and start up a new virtual machine, this time, a kali-linux VM.

# As seen in figure 3 below, Kali comes with an abundance of applications pre-installed, many of which help in different categories like “Information Gathering”, or maybe even “Vulnerability Analysis”.
<img src="images\3.PNG">

# Now that I’ve looked through some of the applications on Kali, I open up a terminal and type in the command: “ifconfig”, to open up the ip configuration settings and determine my ip address.

# As seen below, the ip configuration on linux is slightly different from the windows configuration, including a different command. Nonetheless, the IP address for this virtual machine is: 172.16.3.109.

# After looking at the instructions and even googling what it means by an ICMP stream, I determine that it’s merely a ping from one server to another. As seen in the figure below, the ping from the kali ip is being received by the window ip.
<img src="images\4.PNG">