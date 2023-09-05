<p align="center">
<img src="https://i.imgur.com/KzJbWRS.png" height="50%" width="50%" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>

This demonstration outlines the post-install configuration of the open-source help desk ticketing system "osTicket".

_<b>NOTE:</b> This demonstration uses materials created in the previous demonstration, ["Prerequisites and Installation"](https://github.com/JTYKolesar/osticket-prereqs)._

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- [osTicket Documentation](https://docs.osticket.com/en/latest/index.html)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Create and Configure Roles
- Create and Configure Departments & Teams
- Create and Configure Agents (workers) & Users (clients)
- Configure SLA (Service Learning Agreements)
- Configure Help Desk Topics

<h2>Configuration Steps</h2>

<h3>&#9312; Prerequisites and Installation</h3>

_This demonstration assumes a virtual machine is established with the prerequisite files installed for working osTicket._ </br>
_Credentials and configurations that will be used in this demonstration can be found in ["Prerequisites and Installation"](https://github.com/JTYKolesar/osticket-prereqs)._ </br>
<hr>

<h3>&#9313; Admin Panel - Roles, Departments, Teams, & Agents</h3>

- On the web browser (Microsoft Edge), go to the Help Desk Login Page and sign into your osTicket Help Desk credentials (this example uses username **ostuser / ostuser@email.com**).
  - Help Desk Login Page -- http://localhost/osTicket/scp/login.php
<p align=center>
<img src="https://i.imgur.com/2NAyZo5.jpg" height="100%" width="=100%" alt="Disk Sanitization Steps"/>
</p>

- Currently at the Agent Panel, click on "Admin Panel" at the top-right of the page.
<p align=center>
<img src="https://i.imgur.com/dByQbR1.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Agents" tab > "Roles" > "Add New Role".
<p align=center>
<img src="https://i.imgur.com/mjTZZ5h.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_"Roles are the permissions granted to Agents per Department that they have access to."_
- In the Definition tab, type any Role name of your choice (this example uses **Supreme Admin**).
  - _This role will be given all permissions._
- Then, click on the Permissions tab.
<p align=center>
<img src="https://i.imgur.com/U8vxJEe.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- In the Permissions tab, under the Tickets category, checkmark ALL boxes.
  - Go through both Tasks and Knowledgebase categories and checkmark ALL boxes as well.
- Once done, click "Add Role".
<p align=center>
<img src="https://i.imgur.com/iJGy3L6.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Now we've created a Supreme Admin role with all permissions granted. Next, we'll create a Department._
- Currently in the Agents tab, click on the "Departments" category.
- Click "Add New Department".
<p align=center>
<img src="https://i.imgur.com/vdafrXs.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create a Department name of your choice (this example uses **System Administrators**).
- Skip everything else for now and click "Create Dept".
<p align=center>
<img src="https://i.imgur.com/Uoji0y5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Next, we'll move onto creating a Team._ <br>
_"Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter."_
- Currently in the Agents tab, click on the "Teams" category.
- Click "Add New Team".
<p align=center>
<img src="https://i.imgur.com/jmrWFse.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create a Team name of your choice (this example uses **Level II Support**).
- Click "Create Team".
<p align=center>
<img src="https://i.imgur.com/JyzMjkp.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Currently in the Agents tab, click "Agents" category.
<p align=center>
<img src="https://i.imgur.com/zYQu22H.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create the required credentials for this user that are in bold:
  - First Name (this example uses **Jane**).
  - Last Name (this example uses **Doe**).
  - Email Address (this example uses **jane.doe@osTicket.com**).
  - Username (this example uses **jane.doe**).
- Click "Set Password" and a windows prompt will appear:
  -   Uncheck "Send the agent a password reset email".
  -   Create a password for this user.
  -   Uncheck "Require password change at next login".
  -   Click "Set".
<p align=center>
<img src="https://i.imgur.com/LRAyfYp.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Access" tab:
  - Assign this user the Department that we created (this example uses **System Administrators**).
  - Assign this user the Role that we created (this example uses **Supreme Admin**).
- Under Extended Access, assign this user the "Support" department with the "Supreme Admin" role.
- Click "Save Changes".
<p align=center>
<img src="https://i.imgur.com/NyCTS3W.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Teams" tab:
  -  Assign this user the Team that we created (this example uses **Level II Support**).
-  Once done, click "Create".
<p align=center>
<img src="https://i.imgur.com/WeM5SEd.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Create another Agent following the steps, however assign it to a different Role and Department._</br>
_This example creates Agent **"John Doe"** | Department: **"Level I Support"** | Role: **"View only** | Extended Access: **Support"**_.
<p align=center>
<img src="https://i.imgur.com/ACl29nn.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9314; Agent Panel - Creating Users</h3>

- Click on "Agent Panel" on the top-right of the page.
<p align=center>
<img src="https://i.imgur.com/A6lRMQN.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Click on the "Users" tab.
- Click on "Add User".
- Create an Email Address and Full Name for this user (this example uses **karen@osticket.com / Karen Karen**).
- Click "Add User".
<p align=center>
<img src="https://i.imgur.com/jTIRdhl.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vn9DP8b.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Create another user of your choice (this example uses **ken@osticket.com / Ken Ken**)_
<p align=center>
<img src="https://i.imgur.com/H6Cgj0A.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9315; Admin Panel - Configuring SLA</h3>

_"SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed."_
- Return to the "Admin Panel".
  - Navigate to "Manage" tab > "SLA".
- Click "Add New SLA Plan".
<p align=center>
<img src="https://i.imgur.com/KSONgtH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create the following plans:
  - **SEV-A**
    - Grace Period: **1 hour** (_Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time._)
    - Schedule: **24/7** (_Accounted for all days of the week, even on non-business days_)
  
  - **SEV-B**
    - Grace Period: **4 hours**
    - Schedule: **24/7**

  - **SEV-C**
    - Grace Period: **8 hours**
    - Schedule: **Monday - Friday 8am - 5pm with U.S. Holidays**
- Click "Add Plan" for each.
<p align=center>
<img src="https://i.imgur.com/biqgLPr.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vLW1yZs.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9316; Configure Help Topics</h3>

_Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket._
- Currently in the Admin Pangel, navigate to "Manage" tab > "Help Topics".
- Click "Add New Help Topic".
<p align=center>
<img src="https://i.imgur.com/cYxBbIu.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Create Help Topics with the following names:
  - **Business Critical Outage**
  - **Personal Computer Issues**
  - **Equipment Request**
  - **Password Reset**
- "Internal Notes" can be written down for personal use, but not necessary.
- After that, click "Add Topic".
<p align=center>
<img src="https://i.imgur.com/8u6QJRG.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wVf8qYz.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h1><p align=center>(ﾉ^ヮ^)ﾉ*:・ﾟ✧ COMPLETE! ✧ﾟ・:*╰(^ヮ^╰)</p></h1>

<h2><p align=center>Next Demonstration:<br><a href="https://github.com/JTYKolesar/ticket-lifecycle">Ticket Lifecycle Examples</a></p></h2>

<p align=right>DELETE **EVERYTHING!** IN AZURE TO SAVE CREDITS!<br>
<p align="center">
<img src="https://i.imgur.com/KzJbWRS.png" height="50%" width="50%" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>

This demonstration outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system "osTicket".

_<b>NOTE:</b> This demonstration uses materials created in the previous demonstration, ["Post-Install Configuration"](https://github.com/JTYKolesar/post-install-config)._

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Lifecycle Stages</h2>

<h3>&#9312; Intake</h3>

_We'll start by accessing the page where tickets can be created, as if we're an external user:_
- On the web browser (Microsoft Edge), go to the End User Ticket Page (http://localhost/osTicket/).
- Click on "Open a New Ticket".
<p align=center>
<img src="https://i.imgur.com/Udla59t.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Enter an Email Address and Full Name (this example uses **karen@osticket.com / Karen Karen**)
- Select any Help Topic or one that was created in the previous demo (this example uses **Business Critical Outage**).
- Type a quick Header and a short description under Issue Sumamry (anything can be typed for demonstration purposes).
- Once done, click "Create Ticket".
<p align=center>
<img src="https://i.imgur.com/40QD7AI.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/gg905UJ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Create a few more tickets with varying importance for demonstration purposes:_ 
<p align=center>
<img src="https://i.imgur.com/gsYwMkX.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Uh85P3N.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9313; Assignment and Communication</h3>

_Tickets have been made! We'll now go into the Agent's perspective of their end:_
- On the web browser (Microsoft Edge), go to the Help Desk Login Page (http://localhost/osTicket/scp/login.php).
  - Log into the osTicket Help Desk using an Agent account (this example uses username **jane.doe / jane.doe@osticket.com**).
  - Once logged in, you should see the created tickets from the clients.
- Click on any available ticket (this example selects **entire mobile online banking is down**).
<p align=center>
<img src="https://i.imgur.com/IlBoq7U.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_As an Agent, we'll observe and configure information of this ticket._

_Having the entire mobile online banking down is something that could have a major impact on the company, resulting in losing money. The severity on this should be higher and should be assigned to the departments/teams that can be responsible to resolve this issue ASAP!_
- Set Priorty from Normal to a higher level (this example uses **Emergency**).
- Assign to a higher-tier department (this example uses **System Administrators**).
- Assign a specific person(s) the responsbility to manage this ticket (this example uses the current user, **Jane Doe**).
- Modify the SLA Plan from Normal to a higher level (this example uses **SEV-A**).
<p align=center>
<img src="https://i.imgur.com/V8WJ5GJ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/JR8XMOt.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/CvAfVuZ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Wk23cCI.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/QIbVd0K.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h3>&#9314; Working the Issue</h3>

_Observing the overview page, we can see every update happening within the Ticket Thread. As an Agent, we can communicate under Post Reply to bring status updates to anyone viewing this ticket or for conversational purposes regarding the issue at-hand._
<p align=center>
<img src="https://i.imgur.com/qtVIjs7.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Under Post Reply, type in a random message.
- Keep the Ticket Status to "Open (current)", assuming the issues isn't resolved.
- Click "Post Reply".
<p align=center>
<img src="https://i.imgur.com/P5tLSZ5.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/YvCnXJe.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Like a virtual chat or messaging system, your message will be sent and posted on the thread. The thread will constantly be updated with conversations back and forth, or status changes while working on the issue at-hand._
<hr>

<h3>&#9315; Resolution</h3>

_Let's say the issue has finally been resolved:_
- Under Post Reply, type in a random message stating a final update of the matter.
- Change the Ticket Status to "Resolved".
<p align=center>
<img src="https://i.imgur.com/e1Ac4aR.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vkOXsXv.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

_Once a ticket is resolved, it is considered "closed", so it will disappear from the Open Tickets page._<br>
_You can find it under the "Closed" tab, where you can see how many was closed at a certain time frame._
<p align=center>
<img src="https://i.imgur.com/xw9gHmX.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Continue to go through the rest of the remaining tickets and use best judgement on their Priorty, assignment to departments and teams, etc.
<p align=center>
<img src="https://i.imgur.com/N68R5Y9.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<hr>

<h1><p align=center>(ﾉ^ヮ^)ﾉ*:・ﾟ✧ COMPLETE! ✧ﾟ・:*╰(^ヮ^╰)</p></h1>

<p align=right>DELETE **EVERYTHING!** IN AZURE TO SAVE CREDITS!<br>
If you don't know how to, click <a href="https://github.com/JTYKolesar/azure-start/blob/main/README.md#bonus-delete-all-resources-in-azure">HERE</a>
</p>
