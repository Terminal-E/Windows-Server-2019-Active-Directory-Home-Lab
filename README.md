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
<img width="926" height="908" alt="Server Roles AD DS" src="https://github.com/user-attachments/assets/0baa6ec6-7272-44b2-a3bd-e53bbc9840b3" />

<img width="925" height="907" alt="ad ds2" src="https://github.com/user-attachments/assets/c6acefb0-7d6c-4224-a654-b5154a1d30b3" />




*Step 3: Promote the Server to a Domain Controller*

After the role installed, promoted the server and created a brand new forest.
Selected "Add a new forest"
Set the root domain name (YOUR ROOT DOMAIN NAME)
Set the Directory Services Restore Mode (DSRM) password
Completed promotion and restarted

<img width="933" height="913" alt="Promote server to domain ctl 1" src="https://github.com/user-attachments/assets/47511052-fc1e-4dee-9344-1dacd80a5e79" />
<img width="927" height="907" alt="server to dc 2" src="https://github.com/user-attachments/assets/4745415f-2d56-475d-af95-4a9f06549730" />
<img width="1002" height="912" alt="ad ds3" src="https://github.com/user-attachments/assets/ad1501fe-56b0-48a0-9b59-bc9e33a4c6ae" />
<img width="1011" height="912" alt="server to dc2" src="https://github.com/user-attachments/assets/15a426da-666e-44a6-98f3-d3ffa82bbab1" />


*Step 4: Verify Active Directory and DNS*

Confirmed the domain controller came up healthy after reboot.
Opened Active Directory Users and Computers (ADUC)
Confirmed the domain appears correctly
Checked that the DNS role installed alongside AD
<img width="1012" height="915" alt="DChealth check" src="https://github.com/user-attachments/assets/ffd5609f-e7ea-4d7c-a781-191d3afc4e04" />
<img width="1018" height="910" alt="DNS SHOWS UP" src="https://github.com/user-attachments/assets/71e83246-242c-4777-b9b6-d2e4e29eff65" />
<img width="1020" height="917" alt="DC SHOWS UP" src="https://github.com/user-attachments/assets/f9fac8e1-d84b-408f-8fae-fed0ce2639e4" />
<img width="960" height="913" alt="Dns4" src="https://github.com/user-attachments/assets/eda0f75d-ac17-4af4-b925-3d347399441a" />




*Step 5: Create Organizational Units (OUs)*

Build an OU structure to organize objects logically, the way a real company would by department.

Created a top-level "Departments" OU
Created department OUs beneath it
<img width="961" height="1017" alt="OU&#39;s 1" src="https://github.com/user-attachments/assets/3d07183f-fcf0-4b0f-a945-217dbc569476" />








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








