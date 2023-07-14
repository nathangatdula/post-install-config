<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Create a Supreme Admin role
- Add a Department for System Administrators and a Team for Level II Support
- Allow anyone to create tickets
- Create Agents (workers) and Users (customers)
- Configure SLA with different severities
- Create new Help Topics

<h2>Configuration Steps</h2>

<p> 
</p>

<p>
<img src="https://i.imgur.com/EBqpoA3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After logging into osTicket, click on "Admin Panel" on the top right, to switch from the Agent Panel to the Admin Panel.
</p>
<br />

<p>
<img src="https://i.imgur.com/THm0qxH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First of all, we will create a Supreme Admin role that will be able to manage anything, so click on Agents -> Roles -> Add New Role. The name of the role will be Supreme Admin, and in the permissions tab, select everything.
</p>
<img src="https://i.imgur.com/PgNcZrh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/ohszqCM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/Klmimti.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<img src="https://i.imgur.com/9sMMlPo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Now that the Supreme Admin role is created, let's make the System Administrators department. Again, in the Admin Panel go to Agents -> Departments -> Add New Department. Name the new department System Administrators
<p>
<img src="https://i.imgur.com/IHh7Crm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/QkuQ3ZO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Once the System Administrators department is created, we will now add a new team in the Teams tab under Agents -> Teams -> Add New Team. Name the Team Level II Support.
</p>
<img src="https://i.imgur.com/csLlz3r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
Next, in the osTicket settings, we shall allow anyone to create tickets. Navigate to the user settings through, Admin Panel -> Settings ->  Users -> uncheck "Require registration and login to create tickets". 
<p>
<img src="https://i.imgur.com/VVwBGS9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
Let's create the new Agents and Users now! First, in the Admin Panel, go to Agents -> Agents (next to teams) -> Add New Agent 
<p>
<img src="https://i.imgur.com/2uY4qth.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Fill out the New Agent for Jane Doe as shown. Press Set Password and deselect BOTH boxes. You may use a password like Password1 or something easier that you can remember.
</p>
<img src="https://i.imgur.com/d7pmED9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
<img src="https://i.imgur.com/URefKUL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
In the access tab, put Jane under the System Administrators department and the Supreme Admin role. 
</p>
<img src="https://i.imgur.com/WTHIpVj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For the second Agent, go back to the Agents tab, Add New Agent, and fill out the same requirements for John Doe as shown:
</p>
<img src="https://i.imgur.com/1Z4OeFg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
As the same with Jane, Set John's password as Password1 or whatever you prefer, and uncheck both of the boxes.
</p>
<img src="https://i.imgur.com/URefKUL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
In the access tab, set John's department to Support and the role to View only.
</p>
<img src="https://i.imgur.com/wJKTryo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<p>
To begin adding users, navigate to the Agent Panel on the top right, then click Users -> Add User.
<p>
<img src="https://i.imgur.com/NKS1PaJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://i.imgur.com/xYMerk7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
For the first user, the email can be karen@osticket.com and the full name being Karen Karen as shown (or whatever you prefer).
</p>
<img src="https://i.imgur.com/axeRUtN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
As for the second user, the email will be ken@osticket.com and the full name Ken Ken as shown (or whatever you prefer). 
<p>
<img src="https://i.imgur.com/mHZq9AD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Navigate back to the Admin Panel.
<p>
<img src="https://i.imgur.com/bgpds8e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Go to Manage -> SLA -> Add New SLA Plan
<p>
<img src="https://i.imgur.com/DkY2PgE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
We'll add some SLAs with different severities: 
<p>
  
  - Sev-A
    - (1 hour, 24/7)
  - Sev-B
    - (4 hours, 24/7)
  - Sev-C
    - (8 hours, business hours)

<p>

</p>
</p>
<img src="https://i.imgur.com/SMPynlU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
You may add any notes to each SLA if needed to explain the SLAs.
</p>
<p>
Once all SLAs added, we can move on to adding new Help Topics in the Admin Panel under Manage -> Help Topics -> Add New Help Topic
</p>
<img src="https://i.imgur.com/iISqtsV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
The four Help Topics we will add are:

  - Business Critical Outage
  - Personal Computer Issues
  - Equipment Request
  - Password Reset


</p>
<p>
<img src="https://i.imgur.com/WvtkvrF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Again, you may add any notes to explain the topics.
</p>
<p>
<img src="https://i.imgur.com/WZOTWWB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Congrats! You have completed the osTicket Post-Installation Configuration!
</p>
