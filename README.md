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

# After seeing the successful ping request on the kali virtual machine, I then verify that Wireshark on the windows IP is receiving the ping as seen in the figure below.
<img src="images\5.PNG">

# I save the captured ICMP packets leaving the Kali virtual machine in a PCAP file as “ICMP_Stream_PCAP” for future analysis.

# Looking through the applications available on Kali that I think would be useful for intrusion detection and incident response, here are some that I think would be useful.

# Responder: A useful program that can passively discover possible target systems with its analyze mode and can poison responses, while capturing any credentials in the meantime.

# Mitmproxy: “An interactive man-in-the-middle proxy for HTTP and HTTPS. It provides a console interface that allows traffic flows to be inspected and edited on the fly” (Mitmproxy: Kali linux tools 2022)

# Burpsuite: Burpsuite can be very useful because it can help you identify vulnerabilities and attack vectors affecting your applications. It is similar to Mitmproxy in that it can be used as a proxy server and scanner.

# Hamster: Hamster can be useful because it can allow you to hijack an attacker’s session and it “acts as a proxy server that replaces your cookies with session cookies stolen from somebody else” (Hamster-sidejack: Kali linux tools 2022)

# Ettercap-common: a handy program that “supports active and passive dissection of many protocols… and includes many feature for network and host analysis”(ETTERCAP: Kali linux tools 2022)

# Driftnet: “A program which listens to network traffic and picks out images from TCP streams it observes” (Driftnet: Kali linux tools 2022) Sounds pretty handy for intrusion detection.

# Moving on, I open up wireshark and select the PCAP file to observe any “incidents”. I don’t really see any obvious incidents and move on to network miner to see if I find anything.

# After opening the PCAP file into Network Miner, I didn’t notice any incidents as seen in the figure below:
<img src="images\6.PNG">

# Some of the tools that I’ve included above are very useful for incident detection and response because these tools give us the ability to analyze network traffic data and as a lot of malware and cyber attacks use the network, this is invaluable for incident detection. 
# The main tool that was used in this lab, Wireshark, gives us a nice overview of the types of traffic because it captures packets across the network and gives valuable information for admins to look over. It can include visual hints for hostile activity and allows for further investigation into such incidents.

# An example of Wireshark hinting at a scanning attempt is “a single machine connecting with a number of different systems within the network may indicate attempts at scanning or lateral movement” ((Poston, 2021))

# I went ahead and did another scan with the Kali-hunt machine to nmap scan the Win-hunt virtual machine while its Wireshark is running and as seen in the figure below, Wireshark is giving indication that some hostile activity might be going on and this gives the admin an opportunity to respond to this scan.
<img src="images\7.PNG">

# Bibliography

# Mitmproxy: Kali linux tools. Kali Linux. (2022, August 5). Retrieved February 2, 2023, from https://www.kali.org/tools/mitmproxy/

# Hamster-sidejack: Kali linux tools. Kali Linux. (2022, August 5). Retrieved February 2, 2023, from https://www.kali.org/tools/hamster-sidejack/

# ETTERCAP: Kali linux tools. Kali Linux. (2022, August 5). Retrieved February 2, 2023, from https://www.kali.org/tools/ettercap/

# Driftnet: Kali linux tools. Kali Linux. (2022, November 16). Retrieved February 2, 2023, from https://www.kali.org/tools/driftnet/

# Poston, H. (2021, November 22). Wireshark for Incident Response 101. Infosec Resources. Retrieved February 2, 2023, from https://resources.infosecinstitute.com/topic/wireshark-for-incident-response-101/