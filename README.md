<h1>Digging Deeper into Active Directory</h1>

<h2>Description</h2>
</b>
The goal of this lab was to dip a bit deeper into Active Directory and learn how to set up different settings that you might see in an enterprise setting. This was more of an explore lab rather than a lab that was designed with one specific goal. In this Lab I used two machines, one Server and one Client using Virtual Box for both. 
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/7tCPQBV.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>

<br/>
<br/>

<h2>Utilities Used</h2>

- Active Directory
- Group Policy Management
- Sysinternals
- Share/NTFS permissions
- Drive Mapping

<br/>

<h2>Program Walk Through</h2>
The following information will just be documentation of what I was able to accomplish here in the order that I did it. I first started off by creating an Active Directory on my Server and starting a new Domain called "homelab.local". I installed and setup DHCP, DNS, and RAS/NAT server for later on the in project when I needed to connect to to the Client machine. I documented this process in one of my previous labs.   

<p align="center">
<img src="https://i.imgur.com/lcV2tOl.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

I practiced adding OU's, groups, and users to partially simulate a work environment. 

<p align="center">
<img src="https://i.imgur.com/qMsTiop.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

I started up my Client and joined it to the domain
<p align="center">
<img src="https://i.imgur.com/5vYrYuw.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

Back on the server, I started up group policy management, created a handful of GPOS and assigned them to my Client. I gpupdate /forced the changes and everything seemed to be working. 

<p align="center">
<img src="https://i.imgur.com/mJkbHEU.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/UJqBkJQ.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

I mapped a random network drive to my client and changed the permissions from read only to full access. 

<p align="center">
<img src="https://i.imgur.com/33Ux4eW.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/i17kVmc.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/lD9yNLr.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

I messed around in the File Server Resource Manager adding a quota and limiting the type of files that are accepted. 

<p align="center">
<img src="https://i.imgur.com/m8oziGy.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/Hee78Y1.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<br/>
<br/>

Lastly, I simulated what it might be like to set up a Service Account with special configurations. I created a Service account in AD and installed the AutoLogin sysinternals tool. The idea here was to get the machine to automatically bring up a webpage during start up that required no human intervention. I chose the Nike website here as an example. The last photo is what it looked like after I hit restart and let the automation take over from there. 

<p align="center">
<img src="https://i.imgur.com/Pv9LcaZ.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/BXi36WC.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/vHkJtQ9.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/NylqM8t.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>
<p align="center">
<img src="https://i.imgur.com/WIC2jm2.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


