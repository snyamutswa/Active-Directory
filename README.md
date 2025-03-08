# Active-Directory

## Objective
The purpose of this Active Directory project was aimed to explore and practice Active Directory configurations without disrupting real-world systems.  The focus is to understand Active Directory concepts like user, administrator, group management, organizational unit (OU) structures and group policy objects.

### Skills Learned

- **User and Group Management**: Creating, modifying, and managing user accounts and groups, including setting permissions and managing group memberships. 
- **Group Policy Configuration**: Creating and applying Group Policy Objects to enforce security settings, and manage user environments. 
- **DNS Integration**: Understanding how DNS supports Active Directory and learn to configuring DNS settings for seamless Active Directory functionality.
  
### Tools Used

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- 2 Windows 10 [Iso](https://www.microsoft.com/en-us/software-download/windows10)
- Windows server [Iso](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)

## Step 1: Creating a network diagram


## Step 2: Download and Install Applications and Virtual Machines

* Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* Download [Windows Server 2022 ISO](https://info.microsoft.com/ww-landing-windows-server-2022.html)
* Download [Windows 10 ISO](https://www.microsoft.com/en-us/software-download/windows10)

## step 3 Settings for the Domain Controller
Setting the network to NAT Network for the project

Adding all the machines to this NAT Network

## Step 4: Install Active Directory Domain Services
* From the Server Manager, select Add Roles and Features and add the reason why RAS/NAT needs to be installed is so that the Windows 10 client can be on the private virtual 
  network but still be able to access the internet through the domain controller.
* The Add Roles and Features tab allows access to the AD DS
* After choosing Active Directory Domain Services this will pop up

## Adding computers to the domain.
  Open the file explorer and right click on this pc and select properties, scroll down and find rename this pc. Click on it and select change on rename this pc, Change the 
  computer name to and click on domain and write the name … and click ak
  
  After it will ask for the admin credentials, enter them and click ok.

## Creating Organizationl Units (OU), Groups and Users.
  Open active directory users and computers. Click on the domain …
  First create 2 Geographical OU’s USA and AFRICA.
  Under each Geogrphical OU create 2 OU’s which are computers and user’s OU’s.
  Under the users OU’s create create 2 user groups IT and HR and make the groupnscope global and the group type security 

## Creating GPO’s
  From the windows server open the GPM console. Under the forest company.local right clock on the domain and click on create a GPO in this domain.
  
  The first GPO was the password policy.
  Open the GPM editor and under computer configuarations select policies, then windows settings then navigate to security and select password policy.
  
  The second GPO was Disable USB storage.
  Open the GPM editor and under computer configuarations select policies, then administrative templates then navigate to system and find removable storage.
  
  The third GPO was the account lockout policy.
  Open the GPM editor and under computer configuarations select policies, then windows settings then navigate to security and select account lockout policy.










