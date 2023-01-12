# Qualys VM Deploy Patch
Qualys VMDR Deployment of Patch Job

<h2>Description</h2>
The project involves using Qualys, a vulnerability management and compliance solution, to scan the organization's infrastructure for potential security vulnerabilities. Once identified, the Qualys platform is used to deploy the necessary patches and updates to remediate the vulnerabilities and improve the overall security of the environment. This process is automated and can be integrated with the organization's existing IT systems to ensure that vulnerabilities are identified and addressed in a timely manner. The end goal is to help the organization achieve compliance with industry regulations and standards and reduce the risk of a security breach. I will provide brief screen shots on the steps taken to deploy patches to a daily patch schedule for the vulnerabilites found using Qualys.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Qualys VMDR Lab Enviroment</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 

<h2>Program walk-through:</h2>

<p align="center">
We will first start off at the VMDR Dash Board. Here we will click on "Vulnerabilities" at the top next to "Dashboard": <br/>
<img src="https://imgur.com/Yn3EOdO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
On the vulnerabilites screen we can see list of all detected vulnerabilites from our recent scan. Here you can also filter the view between vulnerabilities and assets:  <br/>
<img src="https://imgur.com/l8GnOQK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
For this lab in particular we will narrow the scope of list by conducting search for only patchable vulnerabilities. To do this we will enter "vulnerabilities.vulnerability.qualysPatchable: TRUE" in the search bar: <br/>
<img src="https://imgur.com/zXC6l0c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
As a result, our search brings up vulnerabilities that have patches available through the Qualys Patch Catalog:  <br/>
<img src="https://imgur.com/h4HrR6C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To receive patches, hosts will have to be running Qualys Patch Management and Cloud Agent activated. We can add both of these modules by clicking on the "+" sign next to the search bar. Once we click on that, we will see an additional box labeled asset, where we can enter the tag names. We will go ahead and enter tags.name:"cloud Agent' and activatedForModules:PM :  <br/>
<img src="https://imgur.com/4ONzhMu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We will now click the check box next to actions and right below the search bar to select all the vulnerabilites:  <br/>
<img src="https://imgur.com/WYVTm7n.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we will click on the actions button and click "View Missing Patches". This will pull up the Patch Summary page that lists patches for both Linux and Windows OS. By clicking on "View Missing Patches" for either of the OS, it will take us to the Patch Catalog.:  <br/>
<img src="https://imgur.com/sHwntYv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
After clicking on "View Missing Patches" for Linux, we are now on the Patch Catalog and will then click on Actions->Add to Existing Job". This will take us to the "Existing Deployment Jobs" screen where we can then click on "add". This will add the patches to the "daily patch deployment job". The Patch Job will deploy the next time the job is scheduled to run:  <br/>
<img src="https://imgur.com/aPUrmBR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
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
