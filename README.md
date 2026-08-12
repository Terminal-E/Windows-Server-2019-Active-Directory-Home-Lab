# Windows-Server-2019-Active-Directory-Home-Lab
A hands-on lab building a Windows Server 2019 domain controller with Active Directory Domain Services (AD DS), then creating an organizational structure with Organizational Units (OUs), users, and groups.
Objective

**Set up a functioning Active Directory environment from scratch and use it to manage users and groups the way an IT administrator would in a real organization.** Specifically:

Install and promote a Windows Server 2019 machine to a domain controller
Create a new Active Directory forest and domain
Build an organizational structure using OUs
Create user accounts and security groups
Assign users to groups and apply a basic access structure

*Lab Environment*

Hypervisor	(VMware Workstation / VirtualBox / Hyper-V)
Server OS	Windows Server 2019
Domain name	(Your Domain Name)
Server role	Active Directory Domain Services (AD DS)
RAM / CPU	( 4 GB RAM, 2 vCPU)

*Step 1: Prepare the Server*

Set a static IP address and rename the server to something meaningful before promoting it, since the name is locked in once it becomes a domain controller.
Assigned a static IP address
Renamed the server (CHANGE SERVER NAME)
Confirmed network connectivity

<img width="1915" height="1075" alt="Win2019Server" src="https://github.com/user-attachments/assets/da7b1521-e4b2-43dc-ac92-15df13fe10be" />

<img width="1026" height="867" alt="Hostname change2" src="https://github.com/user-attachments/assets/cd357f0d-d290-4181-b8cd-c3ab50cc9724" />

<img width="1918" height="1077" alt="StaticIPDFGWDNS" src="https://github.com/user-attachments/assets/02d151cd-5c59-4b4a-8cbe-64684c646981" />

<img width="1022" height="861" alt="hostname change1" src="https://github.com/user-attachments/assets/272b70d3-840d-41d7-9fa6-ac3222d992b3" />




*Step 2: Install the AD DS Role*

Used Server Manager > Add Roles and Features to install Active Directory Domain Services.
Opened Server Manager
Added the AD DS role
Completed the role installation












****INSERT SCREENSHOTS HERE*****



*Step 3: Promote the Server to a Domain Controller*

After the role installed, promoted the server and created a brand new forest.
Selected "Add a new forest"
Set the root domain name (YOUR ROOT DOMAIN NAME)
Set the Directory Services Restore Mode (DSRM) password
Completed promotion and restarted






****INSERT SCREENSHOTS HERE*****








*Step 4: Verify Active Directory and DNS*

Confirmed the domain controller came up healthy after reboot.
Opened Active Directory Users and Computers (ADUC)
Confirmed the domain appears correctly
Checked that the DNS role installed alongside AD









****INSERT SCREENSHOTS HERE*****





*Step 5: Create Organizational Units (OUs)*

Build an OU structure to organize objects logically, the way a real company would by department.

Example structure:

corp.lab.local
├── Departments
│   ├── IT
│   ├── HR
│   ├── Finance
│   └── Sales
Created a top-level "Departments" OU
Created department OUs beneath it


****INSERT SCREENSHOTS HERE*****










*Step 6: Create User Accounts*

Created user accounts inside the appropriate department OUs.
Created several test users (ex. jsmith in HR, mgarcia in Finance)
Set initial passwords and account options
Placed each user in the correct OU


****INSERT SCREENSHOTS HERE*****








*Step 7: Create Security Groups*

Created security groups to manage permissions by role rather than one user at a time.
Created groups (ex. HR-Staff, Finance-Staff, IT-Admins)
Used the appropriate group scope (ex. Global security groups)


****INSERT SCREENSHOTS HERE*****









*Step 8: Add Users to Groups*

Assigned each user to the group matching their department and role.
Added users to their department groups
Verified membership on the group's Members tab


****INSERT SCREENSHOTS HERE*****








