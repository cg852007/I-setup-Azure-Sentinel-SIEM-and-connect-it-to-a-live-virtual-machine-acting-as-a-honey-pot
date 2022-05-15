<h1>I-setup-Azure-Sentinel-SIEM-and-connect-it-to-a-live-virtual-machine-acting-as-a-honey-pot</h1>

 ### [YouTube Demonstration](https://youtube.com)

<h2>Description</h2>
I'm going to create a free Azure subscription with Microsoft. Next, I will create a virtual machine (VM) in Azure and turn the external firewall off for that VM, as well as the windows firewall. Next I will create a log repository in Azure called Log Analytics Workspace which will be used to ingest the logs from the VM. Then I will setup Azure Sentinel (SIEM) within Azure, which is essentially Microsoft's native could SIEM. I will use it to create a map that maps all the different attacker data. I will also use PowerShell to extract the IP address from the winows log and send it to a third party API which will derive the location and send it back to the VM, which I'll use to create a custom log with geographic data.
! When you're totally done with everything delete the resource group in Azure, otherwise it will up the cost.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Microsoft Azure</b> 
- <b>P</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Setup Microsoft Azure account. Mine was pay as you go https://azure.microsoft.com/en-us/free/ <br/>
<img src="https://imgur.com/cjJ5u6P.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Go to https://portal.azure.com/#home  <br/>
<img src="https://imgur.com/7yiMVtD.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
First thing we will do is create a VM. This will be the machine that sits out on the internet exposed to everyone and attackers are going to attack it, AKA our honey pot. <br/>
<img src="https://imgur.com/JB3VsEC.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Create your VM  <br/>
<img src="https://imgur.com/JmInhVW.png" height="80%" width="80%" alt="Template"/>
<br />
<br />
Create a new resource group "Honeypotlab".  <br/>
<img src="https://imgur.com/E3YXiJJ.png" height="80%" width="80%" alt="Template"/>
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
