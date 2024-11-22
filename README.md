# Active_Directory
## Overview
Active Directory (AD) is the directory developed by Microsoft for network resource and device management, as well as user accounts in a centralized and secure manner. It is mainly used in Windows-based environments to make the management of large networks easier. The following are its main features and functions:

**Key Components**
- **Domain:** A logical grouping of networked computers sharing one common directory database. It acts as a boundary for security and administration.
- **Domain Controller (DC):** A server hosting the AD database and managing authentication, authorization, and directory services.
- **Organizational Units (OUs):** Containers for objects within a domain (users, computers, groups). They are used to better manage and apply policies to groups of objects.
- **Objects:** The basic building blocks of AD. Examples include users, computers, printers, and groups.
- **Forest:** A collection of one or more AD domains that share a common schema but can operate independently.

**Use Cases**
- **User Account Management:** Creation, deletion, and modification of user accounts and access privileges in a centralized manner.
- **Device Management:** Administering computers, servers, and resources present within the network.
- **Security:** Enforce standard policies on resources, enforce strict rules about passwords, and monitor user activity.
- **Application Integration:** Most enterprise applications depend on AD for user authentication and access control.

## Objective
Installation and Configuration:
- **Windows Server:** Active Directory, Promote it to Domain Controller
- **Windows PC:** Join Domain

For **Installation** check the [Virtual Lab Setup](https://github.com/raghu2301/Virtual_Lab_Setup)

Open Server Manager on Windows Server.
- Click on Manage.
  
![image](https://github.com/user-attachments/assets/d62d876a-fd71-4c41-bbd7-0025d783759b)

- Check **Active Directory Domain Services** on **Server Role**
- Start the **Install** Process
![image](https://github.com/user-attachments/assets/20ed2831-e029-4caa-ba7b-ccf0d08b8933)

After Installation is complete:
Click on Flag icon and select **Promote this server to a domain controller**

![image](https://github.com/user-attachments/assets/fff7c50e-215a-4c38-bb09-29cbc376a8b9)

Click on **Add roles and features**

![image](https://github.com/user-attachments/assets/2ba1356b-08a6-431f-998d-41a36aa27f90)


Click on **Add a new forest**

Fill **Root domain name** (root domain name should in (dot) format e.g. username.local)


![image](https://github.com/user-attachments/assets/b4c24de3-4e54-4bee-ad44-235f422d9240)

Complete the Installation process.

Restart the Server.

Click on **Tools**

Select **Active Directory Users and Computers**

<img width="471" alt="image" src="https://github.com/user-attachments/assets/8293138b-69fb-4d1d-b218-2857adb0cd9d">


- Right click on domain

![image](https://github.com/user-attachments/assets/a2128843-8dbb-41d9-9f16-33b82499c207)
 - Select **New**
 - Select **Organizational Unit**

![image](https://github.com/user-attachments/assets/9ec45431-4c6a-4fd5-94f4-a6533dd653fe)

 Name it as **IT**
 
 ![image](https://github.com/user-attachments/assets/6b5adb60-1009-4377-b006-ac98d017db13)


 Right click **New >> User**
 
 ![image](https://github.com/user-attachments/assets/07f9c2c1-55d0-4ac7-9b5e-49030ab23327)

Fill in 
- First Name : Terry
- Last Name : Smith
- User log on name : tsmith


![image](https://github.com/user-attachments/assets/f9b29eb5-4017-4df3-a73f-6c9b07c982b5)


- Right click on domain
  
![image](https://github.com/user-attachments/assets/a2128843-8dbb-41d9-9f16-33b82499c207)

 - Select **New**
 - Select **Organizational Unit**
   
![image](https://github.com/user-attachments/assets/9ec45431-4c6a-4fd5-94f4-a6533dd653fe)

 Name it as **HR**
 
 
 ![image](https://github.com/user-attachments/assets/6b5adb60-1009-4377-b006-ac98d017db13)


 Right click **New >> User**

 
 ![image](https://github.com/user-attachments/assets/07f9c2c1-55d0-4ac7-9b5e-49030ab23327)

Fill in 
- First Name : Jerry
- Last Name : Smith
- User log on name : jsmith
  
![image](https://github.com/user-attachments/assets/f9b29eb5-4017-4df3-a73f-6c9b07c982b5)


Now we have:
- 2 Organizational Unit
- 2 User

## Windows Machine
Joining the **new forest** (user.local) and authenticate using **Jerry Smith** account.

Search pc > Properties > Advanced system settings > Computer Name > change > Domain name
Change **Domain** to user.local

![image](https://github.com/user-attachments/assets/a3d75e27-78a5-447c-9300-9013cd9133d0)


Goto Internet Option > change adapter > IPv4 > Properties > Dns

![image](https://github.com/user-attachments/assets/7dae93c6-cb30-4185-8d74-a5d8c161518f)

Change DNS to Server IP (192.168.10.7)

A Pop Up window will appear

![image](https://github.com/user-attachments/assets/27fe21d9-0c97-411c-8c17-69b1196205c7)

Restart the computer

When login screen appears
Click on other user
Sign in to: (It should be directed to User e. g. for me it RAGHU)
Enter the **Username** and **Password**

![image](https://github.com/user-attachments/assets/b8212cc7-458b-4e50-979e-a3df45956db3)

# Conclusion
 Following steps can be used to create a new user, join our computer to a new domain, and login as a new user.




