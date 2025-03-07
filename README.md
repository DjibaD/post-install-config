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

- Log In to the Admin Panel :
After installation, you should be able to access the osTicket admin panel by going to the URL where you installed osTicket (e.g., http://yourdomain.com/scp).
The default admin username is admin and the password is what you set during installation.

- Set Up Email Settings :
osTicket uses email to create tickets and notify users and agents. You'll need to configure the email settings.
Go to the Admin Panel → Emails → Email Settings.
You'll need to configure:
Mail Fetching: This is where osTicket will check for new emails and automatically create tickets from them.
Outgoing Emails: Set up the email address that will be used to send notifications (like ticket updates).
Make sure to use correct SMTP settings based on your mail server or use third-party email services like Gmail, Mailgun, etc.

- Create Departments :
Departments help organize tickets and agents. You can create departments that match your organization's structure or ticket categories.
Navigate to Admin Panel → Manage → Departments → Add New Department.

- Create Ticket Forms and Fields :
osTicket allows you to customize the ticket submission form to collect the necessary information.
Go to Admin Panel → Manage → Forms to customize fields like subject, priority, custom fields, etc.

- Set Up Help Topics :
Help topics allow users to select the type of issue they’re submitting, making it easier for your team to categorize tickets.
Go to Admin Panel → Manage → Help Topics and create topics that fit your organization's needs (e.g., technical support, billing, etc.).

- Set Up Agents and Permissions :
Create agent accounts and assign them to departments.
Navigate to Admin Panel → Manage → Agents → Add New Agent.
You can assign roles (Admin, Agent, etc.) and give them permissions according to what tasks they need to perform.

- Set Up SLA (Service Level Agreements) :
If you need to ensure tickets are addressed within certain time frames, you can set up SLAs.
Go to Admin Panel → Manage → SLA Plans → Add New SLA Plan.

- Customize Email Templates :
osTicket comes with default email templates for ticket notifications (like ticket creation, updates, etc.).
You can customize these email templates by going to Admin Panel → Emails → Templates.

- Test the System :
Submit a test ticket from the user portal and check if the ticket is properly created and notifications are sent.
Try responding to the ticket and ensure that both users and agents receive the appropriate updates.

- Optional - Install Plugins :
You can enhance the functionality of osTicket by installing plugins. For example, integrations with Slack, Google Drive, etc.
Go to Admin Panel → Manage → Plugins to install additional features.

- Security Considerations :
Make sure to change the default admin password and ensure all user credentials are secure.
Consider enabling two-factor authentication (2FA) if it's supported, or use secure passwords for users and agents.
  
<h2>Configuration Steps</h2>

<p>
Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php 

End Users osTicket URL:
http://localhost/osTicket 

</p>
<br />
<p>
<img src="https://i.imgur.com/pto1owG.jpeg" />
</p>
<p>
Configure Roles (for grouping permissions)
Admin Panel -> Agents -> Roles
Supreme Admin

</p>
<br />

<p>
<img src="https://i.imgur.com/tAWEx7I.jpeg" />
</p>
<p>
Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
Admin Panel -> Agents -> Departments
SysAdmins

</p>
<br />

<p>
<img src="https://i.imgur.com/HkPwabz.jpeg" />
</p>
<p>
Configure Teams
Admin Panel -> Agents -> Teams (Pull Agents from different Departments)
Online Banking

Allow anyone to create tickets
Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create tickets)
Registration Required: Require registration and login to create tickets 

</p>
<br />

<p>
<img src="https://i.imgur.com/zwN33W1.jpeg" />
</p>
<p>
Configure Agents (workers)
Admin Panel -> Agents -> Add New
Jane (Dept: SysAdmins)
John (Dept: Support)
  
</p>
<br />

<p>
<img src="https://i.imgur.com/xqzTCqZ.jpeg" />
</p>
<p>
Configure Users (customers)
Agent Panel -> Users -> Add New
Karen
Ken
  
</p>
<br />

<p>
<img src="https://i.imgur.com/EIjFf4W.jpeg" />
</p>
<p>
Configure SLA
Admin Panel -> Manage -> SLA
Sev-A (Grace Period: 1 hour, Schedule: 24/7)
Sev-B (Grace Period: 4 hours, Schedule: 24/7)
Sev-C (Grace Period: 8 hours, Business Hours)

</p>
<br />

<p>
<img src="https://i.imgur.com/ZQSS2LW.jpeg" />
</p>
<p>
Configure Help Topics (For when users create a ticket)
Admin Panel -> Manage -> Help Topics
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
Other

</p>
<br />
