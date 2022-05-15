<h1>I-setup-Azure-Sentinel-SIEM-and-connect-it-to-a-live-virtual-machine-acting-as-a-honey-pot</h1>

 ### [YouTube Demonstration](https://youtube.com)

<h2>Description</h2>
I'm going to create a free Azure subscription with Microsoft. Next, I will create a virtual machine (VM) in Azure and turn the external firewall off for that VM, as well as the windows firewall. Next I will create a log repository in Azure called Log Analytics Workspace which will be used to ingest the logs from the VM. Then I will setup Azure Sentinel (SIEM) within Azure, which is essentially Microsoft's native could SIEM. I will use it to create a map that maps all the different attacker data. I will also use PowerShell to extract the IP address from the winows log and send it to a third party API which will derive the location and send it back to the VM, which I'll use to create a custom log with geographic data.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python 3.10 (64-bit)</b> 
- <b>PyCharm Community Edition 2022.1</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Template"/>
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
