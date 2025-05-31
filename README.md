<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Video Demonstration</h2>

- ### [YouTube: osTicket Post-Installation Configuration: Complete Admin Setup Tutorial](https://youtu.be/fxgP5q5EoCY)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Configure Agents
- Configure Users
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/pk8xsm7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First we need to log in to the admin portal of osTicket by going to <a href="http://localhost/osTicket/scp/login.php">HERE</a> and entering in the correct credentials the clicking the "Log In" button.
</p>
<br />

<p>
<img src="https://i.imgur.com/lgMLhHc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to be creating a new role as "Supreme Admin". Click on the "Agents" tab then select "Roles". Click "Add New Role" button on the right. Name the new role "Supreme Admin" then click on the "Permissions" tab and check all the boxes under "Tickets", "Tasks" and "Knowledgebase". Now click on "Add Role" and it should now be listed with the other roles.
</p>
<br />

<p>
<img src="https://i.imgur.com/68cy8WK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to create a new department called "SysAdmins". To do this click on the "Agents" tab then select "Departments" then click on the "Add New Department" button. In the name field type "SysAdmins" then click on the "Create Dept" button at the bottom.
</p>
<br />

<p>
<img src="https://i.imgur.com/kGql7Bw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to create a new team called "Online Banking". To do this click on the "Agents" tab then click "Teams" the click on the "Add New Team" button. In the name field type "Online Banking" then click on the "Create Team" button at the bottom. If you click on the teams tab it should display the new team created.
</p>
<br />

<p>
<img src="https://i.imgur.com/a3KjMJ1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to allow any users to be able to create tickets without having to register accounts. To do this click on the "Settings" tab then select "Users". Uncheck the box next to "Require registration and login to create tickets", it may already be unchecked but is nice to make sure that anyone can create tickets.
</p>
<br />

<p>
<img src="https://i.imgur.com/PFgKu3t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to create "Jane Doe" as an agent who's primary department will be "SysAdmins" with the "Supreme Admin" role and will be assigned to the "Online Banking" team. To do this click on the "Agents" tab at the top then click the "Add New Agent" button. For name field enter "Jane Doe". For email enter a fake email. For username enter "Jane". Now click on the "Access" tab and for "Primary Department" select "SysAdmins" and for "Role" select "Supreme Admin". Next, click on the "Teams" tab and select "Online Banking" as the team then select the "Create" button. 
</p>
<br />

<p>
<img src="https://i.imgur.com/ZVZkUsY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to create "John Doe" as an agent who's primary department will be "Support" with the "View Only" role. To do this click on the "Agents" tab again then click the "Add New Agent" button. For name field enter "John Doe". For email enter another fake email. For username enter "john". Now click on the "Access" tab and for "Primary Department" select "Support" and for the "Role" select "View Only". Now click on the "Create" button.
</p>
<br />

<p>
<img src="https://i.imgur.com/y1sMKGj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to set the passwords for the two new agents that we created "Jane Doe" and "John Doe". To do this click on the "Agents" tab and click on either of their links. Click on the "Set Password" button in the mid-right of the box. Uncheck both boxes and type "Password1" as the password then click the "Update" button. Then do the same for the other agent.
</p>
<br />

<p>
<img src="https://i.imgur.com/lRSXRg5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to create two users within the "Agent" panel name "Karen" and "Ken". To do this click on the "Agents Panel" at the top to switch over to the workers panel. Click on the "Users" tab then click on the "Add User" button. Fill in a fake email and under name type "Karen" then select the "Add User" button. Do the same steps to create another user called "Ken". 
</p>
<br />

<p>
<img src="https://i.imgur.com/fYakxr4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to be creating three new SLA's for osTicket Help Desk called Sev-A, Sev-B and Sev-C with varying grace periods and assigning a schedule for them. To do this we need to navigate back to the "Admin Panel" by clicking the link at the top of the page then clicking on the "Manage" tab selecting "SLA" and clicking on the "Add New SLA Plan" button on the right. Under the name field type "Sev-A" and enter "1" in the grace period field the select "24/7" as the schedule then click the "Add Plan" button. Click on the "Add New SLA Plan" again and under the name field type "Sev-B" and enter "4" in the grace period field and select the same schedule as before then click the "Add Plan" button. Again, click on the "Add New SLA Plan" and under the name field type "Sev-C" and enter "8" in the grace period field then select "24/5" as the schedule.
</p>
<br />

<p>
<img src="https://i.imgur.com/lRvmknN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will be creating five "Help Topics" with "Business Critical Outage", "Equipment Request", "Personal Computer Issues", "Password Reset" and "Other" for users to categorize when sending tickets. To do this click on the "Manage" tab then select "Help Topics" then click the "Add New Help Topic" button. For the first topic type "Business Critical Outage" and select "Report a Problem" as the parent topic. Then click on "Manage" then select "Help Topics" and click on the "Add New Help Topic" button. For the second topic type "Equipment Request" and select "General Inquiry" as the parent topic. Then click on "Manage" then select "Help Topics" and click on the "Add New Help Topic" button. For the third topic type "Personal Computer Issues" and select "Report a Problem" as the parent topic. Then click on "Manage" then select "Help Topics" and click on the "Add New Help Topic" button. For the fourth topic type "Password Reset" and select "Report a Problem" as the parent topic. Then click on "Manage" then select "Help Topics" and click on the "Add New Help Topic" button. For the last topic type "Other" and select "General Inquiry" as the parent topic.
</p>
<br />


<p>
This is going to conclude the post-install configuration of osTicket.
</p>
