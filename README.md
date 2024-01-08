<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket. We will simulate a real-world environment in which users can create tickets to be resolved by the help desk staff.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Understand the difference between admin and agent roles
- Configure agent roles (help desk staff) as an admin
- Create user accounts as an agent
- Understand SLA (service level agreements) when resolving tickets
- Configure ticket categories (PC issues, password resets, etc)

<h2>Admin Panel - Roles, Departments, and Teams</h2>

<p>

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/7b8bc52c-1ec2-4d95-b294-50614d7b5648)

</p>
<p>
Add a role called "Supreme Admin". Ensure that under the "permissions" tab, you grant all permissions. This role will simulate a SysAdmin and oversee all operations of the help desk staff.
</p>
<br />


![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/80cefc7a-c5d6-4d88-bd9b-3562f4b03d2a)

<p>
Next, we will configure a new department called "System Administrators". For simplicity, we will maintain all of the default settings. We will assign help desk agents to this department.
</p>
<br />

<p>

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/721e8c43-4e1e-4379-a47b-67579ea0b3e0)

</p>
<p>
After configuring a department, we must now set up a team. The purpose of a team in osTicket is to pull agents from various departments together to handle a specific issue. In this way, different departments can work together to provide end-user support. 
</p>
<br />


<p>

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/1f13d1b4-2c20-4861-8921-13ff4408a66b)

</p>
<p>
We must now create help desk agents. You can assign them thier username, password, access controls, permissions, and teams. In my example, I am assigning a user called "Jane Doe" the Supreme Admin role for my System Administrator's department under the "Access" panel. I have also assigned her to a team called "Level II Support". 
</p>
<br />


<h2>Agent Panel</h2>

<p>

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/893d15de-649b-47d5-919f-baac098c3ce9)

</p>
<p>
We will configure users. Users act as customers, they are the non-technical employees in a business making the requests for help desk agents to resolve using the ticketing software. In the agent panel, navigate to Users > Add New. 
</p>
<br />

<h2>Admin Panel - Service Level Agreements and Ticket Categories</h2>

<p>

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/f41de0ec-2cf6-4de0-a364-966b0b015e61)

</p>
<p>
A Service Level Agreement (SLA) is a way of prioritizing a ticket submitted by an end-user based on its severity. Depending on this, help desk agents are required to resolve tickets within an alloted amount of time agreed upon in the SLA.
</p>
<br />

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/c8595e07-4ad6-4a10-a8cd-395dd029b9f2)

<br />

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/52848dfa-0cdb-42ff-9382-416b3bd3a756)


<p>
In the admin panel, manage the SLA by navigating to Manage > SLA > Add New. I set 3 SLA's, with the highest priority allowing for a grace period for 1 hour 24/7, and the lowest severity allowing for 8 hours during normal business hours.
</p>
<br />

![image](https://github.com/SergioRodriguez33/post-install-config/assets/99108184/4253f571-1ca4-45e9-9221-816b4c5e812f)

<p>
Here, we are creating help topics. You can think of help topics as categories for which users request assistance with their technical issues. These help topics can also be assigned to a specific SLA. For example, in the image above, we can assign our "Business Critical Outage" to our SEV-A SLA because we would realistically prioritize this issue being resolved.
</p>
