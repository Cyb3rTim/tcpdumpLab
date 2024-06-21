<h1>Tcpdump Lab</h1>

<h2>Introduction</h2>
tcpdump is a command-line utility used primarily for packet analysis. It captures packet data from network interfaces and can use the Berkley Packet Filter (BPF) syntax. The key point to remember here is that it is a lightweight packet analysis tool and a common suite used by many organizations to conduct packet captures (PCAPs).
<br />

<br> 
<br> 


<b>Some of the most common parameters used with tcpdump:</b>

-#: Display line/packet number<br/>
-c count: Number of packets to capture before tcpdump automatically exits.<br/>
-D: Display interfaces<br/>
-e: Display Ethernet header data.<br/> 
expression: Specify a Berkeley Packet Filter (BPF) statement to filter traffic.<br/>
-i interface: Specify from which network interface you would like tcpdump to sniff. This generally requires administrative permissions.<br/>
-n: Don't resolve hostnames or well-known port numbers to their service.<br/> 
-r file: Specify an existing pcap file to read from instead of a network interface.<br/>
-s snaplen: Snapshot length, or the number of bytes to capture per packet. Default is 262,144 bytes but this may vary across platforms.<br/>
-w file: Specify a new pcap file to place filtered packets in.<br/>
-X: Show packet contents in hexadecimal and ASCII.<br/>
-v : Display verbose output<br/> 


<b>Task 1: Examining Packet Headers</b> <br>
1.1) We will start out by using tcpdump to examine packet headers. For example, if we wanted to display headers and line numbers of the first 20 packets, we would type the following command<br><br>
<b>Command:</b> tcpdump -n -r investigate.pcap -c 20 -#
<p align="center">
Examining Packet Headers: <br/>
<img src="https://i.imgur.com/b12pVbp.png" height="80%" width="80%"
<br>
  
*The “tcpdump” command above tells the system that we want to use tcpdump<br>
*The “-n” command tells the system that we do NOT want hostnames or well-known port numbers resolved to their services.<br>
*“-r investigate.pcap” tells the system we want to open this file. When you type “-r” remember to specify the file you want to open.<br>
*-c 20” Tell the system that we want to specify the number of packets to display. In this example, we chose to display 20 packets.<br>
*“-#” is used to number the packets neatly and clearly so that they are easier to read.<br>
<br />
1.2) In the output of the previous step, each line represents a single packet and shows the details associated with it. The following chart will help you understand how to read the output of these packets.
<br>
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
