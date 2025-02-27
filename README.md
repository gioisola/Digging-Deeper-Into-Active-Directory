<h1>Digging Deeper into Active Directory</h1>

<h2>Description</h2>
</b>
The goal of this lab was to dip a bit deeper into Active Directory and learn how to set up different settings that you might see in an enterprise setting.  
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/FLmCr2X.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>

<br/>
<br/>

<h2>Utilities Used</h2>

- Active Directory
  - Group Policy
  - 

<br/>

<h2>Program Walk Through</h2>
I created a resource group to house the lab, a virtual network to allow the VM to connect to the public network, the VM itself, and the logging space using Sentinel and Log Analytics Workspace (Disregard gio-vmlab and TEST-2-group).

<p align="center">
<img src="https://i.imgur.com/Jwt6rmn.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

All inbound rules were removed within the network security group to allow free access to our network.

<p align="center">
<img src="https://i.imgur.com/FwaqcBi.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

All windows firewall protections were turned off

<p align="center">
<img src="https://i.imgur.com/vN2yvSy.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

To connect the log analytics workspace and SIEM (sentinel) to our VM and allow us to view logs, I installed windows security event and the azure monitoring agent. 

<p align="center">
<img src="https://i.imgur.com/3dmmxK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/hr4L1G9.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

proof of log acquisition (this is a photo of what it looked like as I was recreating the project for the 3rd time for this walk through. The first time I did it I left the VM on for 5+ hours and got 10,000+ logs with attackers with IPs from Asia, Europe, and South America). 

<p align="center">
<img src="https://i.imgur.com/P5boBXW.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

Finally, I created a workbook and copy and pasted a JSON file that was designed to present the data in a map format. I used a query within the log viewer to connect the map and the logs coming in (this is the data that was saved from my first attempt that better respresents what it should look like).

<p align="center">
<img src="https://i.imgur.com/wj9aHXa.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>
