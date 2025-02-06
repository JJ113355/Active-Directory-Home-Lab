<h1>Active DirectoryHome Lab</h1>

<h2>Description</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows Server 2022</b> 
- <b>VMware Workstation Pro</b> 

<h2>Installing Active Directory Domain from scratch:</h2>
Steps:

- <b>Install Windows Server in a virtual machine.</b>
- <b>Promote the server to a Domain Controller (DC).</b>
- <b>Create an AD Domain (e.g., example.local).</b>
- <b>Create organizational units (OUs) from different departments (e.g., IT, HR, Sales).</b>
- <b>Create user accounts and groups within these OUs.</b>
<br />
<br />
<h2>Part 1: Install Windows Server in a virtual machine. </h2>
 <p align="center">
Use the ISO download in the virtual machine: <br/>
<img src="https://i.imgur.com/VEyZKxu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select operating system (Windows Server 2022 Standard Evaluation(Desktop Experience):  <br/>
<img src="https://i.imgur.com/JCkqtY2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the custom Installation type: <br/>
<img src="https://i.imgur.com/lqOjN8K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a Password for the Administrator:  <br/>
<img src="https://i.imgur.com/YXlAfdv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run “winver” command in bottom left to check windows server setup:  <br/>
<img src="https://i.imgur.com/vQBiATq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select Add Roles and Features:  <br/>
<img src="https://i.imgur.com/z4p1HZ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select “Role-based or Feature-Based Installation”:  <br/>
<img src="https://i.imgur.com/RTS3raZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select Active Directory Domain Services <br/>
Continue and hit “Add features” <br/>
<img src="https://i.imgur.com/EC6qhFZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Click install <br/>
<img src="https://i.imgur.com/xsuIT24.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>
<h2>Part 2. Promote the server to a Domain Controller (DC).</h2>
<p align="center">
Click “Promote this server to a domain controller”.<br/>
Have to set up a domain controller because there is not one currently installed on the server.<br/>
<img src="https://i.imgur.com/3LpjEWf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>
<h2>Part 3. Creating an Active Directory Domain(e.g., example.local).</h2>
<p align="center">
Select "Add a new forest", and create Root Domain Name.<br/>
<img src="https://i.imgur.com/ugqZltW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>
