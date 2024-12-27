<p align="center">
<img src="https://i.imgur.com/1aYDBzI.png"/>
</p>

<h1>Observing ICMP Traffic</h1>
This project tutorial will outline and walkthrough the observation of a packet capture and filtering of ICMP traffic using a "ping" within Windows10 and Linux Ubuntu Virtual Machines via Wireshark and Powershell. Monitoring ICMP traffic helps with troubleshooting and diagnosis in network performance, reachability, and security analysis. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- WireShark
- Powershell
  

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Linux/Ubuntu </b>

<h2>List of Prerequisites</h2>

- Computer Desktop/Laptop
- Wifi Connection
- Azure Account
- Remote Desktop
- Wireshark Installation
- Npcap 1.79 Setup Installation

<h2>ICMP Traffic Tutorial Steps</h2>
Step 1:
<p>
<img src="https://i.imgur.com/RsxiQFc.png"/>
</p>
<p>
Go into Virtual Machines in your Azure account and start both your Linux and Windows 10 Virtual Machines. Make sure to retreive (copy+paste) the Public IP address for the Windows10 Virtual machine for it will be needed in remote desktop in the next step.
</p>
<br />
Step 2:
<p>
<img src="https://i.imgur.com/hZIQqAU.png"/>
</p>
<p>
After starting the virtual machines, go into the remote desktop app and click add PC's. Paste the Windows10 Public IP address in the PC name box to connect to the virtual machine in Azure and in the display name box type in windows10-vm.
</p>
<br />
Step 3:
<p>
<img src="https://i.imgur.com/fpRUVwh.png"/>
</p>
<p>
On this screen, this is where you will see all of the different PC's or Virtual Machines you have created within Azure. They will pop up here on your saved PC's. Click on the Windows10-vm icon to log on.
</p>
<br />
Step 4:
<p>
<img src="https://i.imgur.com/893lV5u.png"/>
</p>
<p>
Log in with the credentials you created and used in the Administrator Account section when creating this Windows10-vm in Azure. 
</p>
<br />
Step 5:
<p>
<img src="https://i.imgur.com/OyEvcNl.png"/>
</p>
<p>
Once the windows10-vm is up and running in remote desktop, go into the internet  browser within remote desktop and type in www.wireshark.org. 
</p>
<br />
Step 6:
<p>
<img src="https://i.imgur.com/c9nK5RZ.png"/>
</p>
<p>
Use the Windows x64 Installer to install the Wireshark App. Download and open the files to install within the windows10-vm remote desktop. The next steps will walkthrough the Wireshark installation.
</p>
<br />
Step 7:
<p>
<img src="https://i.imgur.com/pPeAu5i.png"/>
</p>
<p>
On the first Wireshark installation page press Next. 
</p>
<br />
Step 8:
<p>
<img src="https://i.imgur.com/GPLsDOa.png"/>
</p>
<p>
On the License Agreement page press the noted/next button.
</p>
<br />
Step 9:
<p>
<img src="https://i.imgur.com/shPJ5yx.png"/>
</p>
<p>
You will then be brought to a Donations page, just press next. 
</p>
<br />
Step 10:
<p>
<img src="https://i.imgur.com/iy4fQ5m.png"/>
</p>
<p>
On the Choose Components page press next.
</p>
<br />
Step 11:
<p>
<img src="https://i.imgur.com/E4IE1XY.png"/>
</p>
<p>
On the Additional Tasks page make sure the Wireshark Start Menu and Associate Trace File Extensions are checked off. Press next.
</p>
<br />
Step 12:
<p>
<img src="https://i.imgur.com/Tx4POHg.png"/>
</p>
<p>
Press next on the Choose Install location page.
</p>
<br />
Step 13:
<p>
<img src="https://i.imgur.com/KVBrxj7.png"/>
</p>
<p>
On the Packet Capture page make sure to check off Install Npcap. Press next.
</p>
<br />
Step 14:
<p>
<img src="https://i.imgur.com/yl39782.png"/>
</p>
<p>
On the next page, leave the Install USBPcap box unchecked and press install.
</p>
<br />
Step 15:
<p>
<img src="https://i.imgur.com/KkW80nT.png"/>
</p>
<p>
Application will begin to install. 
</p>
<br />
Step 16:
<p>
<img src="https://i.imgur.com/gS3ENiu.png"/>
</p>
<p>
While Wireshark application is installing the Npcap License Agreement will pop up. Just press agree. 
</p>
<br />
Step 17:
<p>
<img src="https://i.imgur.com/K1m8JsE.png"/>
</p>
<p>
The Npcap agreement application will begin to install.
</p>
<br />
Step 18:
<p>
<img src="https://i.imgur.com/nw30V43.png"/>
</p>
<p>
Once installation is complete press finish.
</p>
<br />
Step 19:
<p>
<img src="https://i.imgur.com/DwQiCKf.png"/>
</p>
<p>
After the license agreement is completed the Wireshark application should be done installing so just press next.
</p>
<br />
Step 20:
<p>
<img src="https://i.imgur.com/p2VEc16.png"/>
</p>
<p>
Press finsh.
</p>
<br />
Step 21:
<p>
<img src="https://i.imgur.com/u2nhbTO.png"/>
</p>
<p>
Next go to the start menu of the windows10-vm remote desktop and search for Wireshark. Click on and open up the app.
</p>
<br />
Step 22:
<p>
<img src="https://i.imgur.com/FiJ1W7v.png"/>
</p>
<p>
On the homepage click on the Ethernet tab. 
</p>
<br />
Step 23:
<p>
<img src="https://i.imgur.com/1vID4CM.png"/>
</p>
<p>
Next in the upper left corner click on the blue shark symbol to begin running a packet capture within Wireshark.
</p>
<br />
Step 24:
<p>
<img src="https://i.imgur.com/QOjOt1j.png"/>
</p>
<p>
When running the packet capture try to make an observation of the spam traffic amongst the private ip address of the windows10-vm.
</p>
<br />
Step 25:
<p>
<img src="https://i.imgur.com/ZVB4ugp.png"/>
</p>
<p>
Next filter for ICMP traffic by typing in ICMP in the search bar of the Wireshark app. 
</p>
<br />
Step 26:
<p>
<img src="https://i.imgur.com/BG5lJVB.png"/>
</p>
<p>
For right now all of the spam traffic will disappear.
</p>
<br />
Step 27:
<p>
<img src="https://i.imgur.com/tUI231d.png"/>
</p>
<p>
Go back into Azure virtual machines and click on Linux Ubuntu. 
</p>
<br />
Step 28:
<p>
<img src="https://i.imgur.com/lvuOiow.png"/>
</p>
<p>
Scroll down until you find the private ip address then copy it. 
</p>
<br />
Step 29:
<p>
<img src="https://i.imgur.com/uCawcds.png"/>
</p>
<p>
Next go to start menu of windows10-vm remote desktop and search for Windows Powershell and  click on the app to open.
</p>
<br />
Step 30:
<p>
<img src="https://i.imgur.com/qWnGkrT.png"/>
</p>
<p>
In this step a ping will be set in place to try and respond to the windows10-vm from the linux ubuntu virtual machine. In the command line of Powershell type in ping and paste in the private ip address of the linux ubuntu excatly as how you see it in the image. Make sure theres a space between ping and ip address. It should look like this: ping 10.0.0.5, then press enter.
</p>
<br />
Step 31:
<p>
<img src="https://i.imgur.com/g7pKpVf.png"/>
</p>
<p>
Now observe both the Wireshark and Windows Powershell Apps with the ICMP filtered traffic. You can now see the spam traffic has been filtered out and its much easier to see the Windows10-vm and linux ubuntu-vm request/reply communications passing through. Also note how the private ip addresses are alternating under the source colume in Wireshark, indicating that one private ip is sending out a request and the other one is responding. They can also be called echo pings. 
  
This here is a breif observation of ICMP traffic and conclusion of this project tutorial.
</p>
<br />

