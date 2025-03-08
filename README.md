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
<img width="629" alt="Image" src="https://github.com/user-attachments/assets/d910ac1c-4c3f-44cc-83e7-5d22297f6c68" />

## Step 2: Download and Install Applications and Virtual Machines

* Download [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* Download [Windows Server 2022 ISO](https://info.microsoft.com/ww-landing-windows-server-2022.html)
* Download [Windows 10 ISO](https://www.microsoft.com/en-us/software-download/windows10)

## step 3 Settings for the Domain Controller
Setting the network to NAT Network for the project
![Image](https://github.com/user-attachments/assets/e58eb0bb-3e99-4f2a-bade-c84a90d691b4)

Adding all the machines to this NAT Network
![Image](https://github.com/user-attachments/assets/3349fe97-1a1e-4ced-91b3-f104ca75c00a)

![Image](https://github.com/user-attachments/assets/78ff12b2-2238-4148-a7e5-19451bc804b6)


## Step 4: Install Active Directory Domain Services
* From the Server Manager, select Add Roles and Features and add the reason why RAS/NAT needs to be installed is so that the Windows 10 client can be on the private virtual.

![Image](https://github.com/user-attachments/assets/5f80d2ca-5417-42cc-979b-0858919d7531)

![Image](https://github.com/user-attachments/assets/7901259f-d47f-4763-a0e6-6ed85e793f13)

![Image](https://github.com/user-attachments/assets/537b427b-6b39-43d5-8f08-14beff1a3f65)


* A post-deployment configuration is needed because the domain wasn't 
  created before installing AD DS.

 ![Image](https://github.com/user-attachments/assets/85ed6b61-dec3-4b47-8fec-e05d13f06b47)

 * Configure admin password
 ![Image](https://github.com/user-attachments/assets/7bad7de3-b1a7-4dda-9b58-a7c10ac25333)

## Adding computers to the domain.
  Open the file explorer and right click on this pc and select properties, scroll down and find rename this pc. Click on it and select change on rename this pc, Change the 
  computer name to and click on domain and write the name … and click ak
  ![Image](https://github.com/user-attachments/assets/974e1784-e31a-497f-a311-b6078656b0c1)
  
  After it will ask for the admin credentials, enter them and click ok.

## Creating Organizationl Units (OU), Groups and Users.
  Open active directory users and computers. Click on the domain …
  First create 2 Geographical OU’s USA and AFRICA.
  Under each Geogrphical OU create 2 OU’s which are computers and user’s OU’s.
  
  ![Image](https://github.com/user-attachments/assets/204db705-1a56-4504-ab57-42db0d93e239)
  
  Under the users OU’s create create 2 user groups IT and HR and make the groupnscope global and the group type security 

## Creating GPO’s
  From the windows server open the GPM console. Under the forest company.local right clock on the domain and click on create a GPO in this domain.
  
  The first GPO was the password policy.
  Open the GPM editor and under computer configuarations select policies, then windows settings then navigate to security and select password policy.
  
  ![Image](https://github.com/user-attachments/assets/4629c307-2108-4998-b4c0-210efa10f9db)
  
  The second GPO was Disable USB storage.
  Open the GPM editor and under computer configuarations select policies, then administrative templates then navigate to system and find removable storage.

  ![Image](https://github.com/user-attachments/assets/998dbf0e-87c4-423b-9732-4ffe8c19984b)
  
  The third GPO was the account lockout policy.
  Open the GPM editor and under computer configuarations select policies, then windows settings then navigate to security and select account lockout policy.

  ![Image](https://github.com/user-attachments/assets/fb49a56e-71f4-4d24-8265-988da17ee05c)










