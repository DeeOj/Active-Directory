# PROJECT: ACTIVE DIRECTORY

## LINKS TO RESOURCES
- [VMWare Workstation Pro](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html)
- [window Server 2022 ISO](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)
- [Window 11 ISO](https://www.microsoft.com/software-download/windows11)
- [Create Account Script](https://shorturl.at/buBuR)

## OVERVIEW OF TASK
This project involved setting up an Active Directory environment. Key tasks included installing and configuring Windows Server, deploying Active Directory Domain Services, and promoting the server. Additionally, I joined a Windows 11 Pro client was to the domain, and employed a PowerShell script to automate the creation of 1,000 user accounts. Successful domain integration was demonstrated by logging into the client machine with newly created user credentials.

## PROCEDURE

### INSTALLING WINDOWS SERVER 

<p align="center">
<img src="https://imgur.com/wTLzDHX.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/hSUaWSQ.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/xqPJnsE.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/mYHfOLW.jpg" height="90%", width="90%">
</p>

- Power On the VM

<p align="center">
<img src="https://imgur.com/CmvSlJX.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/61V1fU5.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/FgJWaP0.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/ZLe9ndq.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/owZ6ROI.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/Tv7mvVX.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/mHVrpgF.jpg" height="90%", width="90%">
</p>

- Install VMware Tools <br/>
  This will help in the scaling and resolution of the machine.
  
<p align="center">
<img src="https://imgur.com/NxOa4Ak.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/WTk06p3.jpg" height="90%", width="90%">
</p>

- Rename the PC

<p align="center">
<img src="https://imgur.com/5lbVDtY.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/YjEGbfC.jpg" height="90%", width="90%">
</p>

- Setup Static IP Address <br/>
  I am going to be pointing the client computer towards the domain controller for DNS services as it will also be acting as the DNS server. Thus, the need to set the IP static. Will utilize
  it's current addressing setup for this.
  
<p align="center">
<img src="https://imgur.com/HYCEEwN.jpg" height="90%", width="90%">
</p>

<p align="center">
<img src="https://imgur.com/m8BYLH4.jpg" height="90%", width="90%">
</p>

- Restart
  
<p align="center">
<img src="https://imgur.com/wUfdkxm.jpg" height="90%", width="90%">
</p>

### INSTALLING ACTIVE DIRECTORY DOMAIN SERVICES

- Add Roles and Features
<p align="center">
<img src="https://imgur.com/EKHeepU.jpg" height="90%", width="90%">
</p>

- Select server
<p align="center">
<img src="https://imgur.com/tNo2QdK.jpg" height="90%", width="90%">
</p>

- Select Active Directory Domain Services and add features
<p align="center">
<img src="https://imgur.com/6vnpg5G.jpg" height="90%", width="90%">
</p>

- Install
<p align="center">
<img src="https://imgur.com/diwONgK.jpg" height="90%", width="90%">
</p>

### PROMOTING SERVER TO DOMAIN CONTROLLER

<p align="center">
<img src="https://imgur.com/Tx8ek2N.jpg" height="90%", width="90%">
</p>

- Add new forest and create(insert) a domain name
<p align="center">
<img src="https://imgur.com/5YPNDYP.jpg" height="90%", width="90%">
</p>

- Set password
<p align="center">
<img src="https://imgur.com/gngmO2n.jpg" height="90%", width="90%">
</p>

- Install and Restart
<p align="center">
<img src="https://imgur.com/9PBzl5J.jpg" height="90%", width="90%">
</p>

We now see the domain is created, and I'm still signing into the domain with the built in administrator account
<p align="center">
<img src="https://imgur.com/VNI4LBP.jpg" height="90%", width="90%">
</p>

- Create Dedicated Admin Account
 At this point, I will be creating a dedicated account for the administrator. So, as to stop using the built in administrator account.

<p align="center">
<img src="https://imgur.com/UWkkNuA.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/ADuw9fE.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/brCsHg3.jpg" height="90%", width="90%">
</p>

Account created.
<p align="center">
<img src="https://imgur.com/09aVDSZ.jpg" height="90%", width="90%">
</p>

Make a user domain admin:
<p align="center">
<img src="https://imgur.com/wRL9zWA.jpg" height="90%", width="90%">
</p>

### WINDOWS 11

- The configuration of the client computer:
<p align="center">
<img src="https://imgur.com/Y5p4ws8.jpg" height="90%", width="90%">
</p>

- I configured the network settings to point to domain controller for DNS services, by using the Domain Controllers IP address for the DNS server for this client computer.
<p align="center">
<img src="https://imgur.com/9ucgALk.jpg" height="90%", width="90%">
</p>

- Resolving and confirming domain from client computer
<p align="center">
<img src="https://imgur.com/9ucgALk.jpg" height="90%", width="90%">
</p>

- Joining Client to Domain
  
<p align="center">
<img src="https://imgur.com/eCCvcX4.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/aMqZ2aQ.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/AwxIO2Y.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/BEtoseh.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/DdV1bg6.jpg" height="90%", width="90%">
</p>

The windows 11 client is successfully joined to the domain "DeeOj-Ltd.com" I created earlier, from which any user can use their credentials to log into their accounts.

<p align="center">
<img src="https://imgur.com/RAYMS2n.jpg" height="90%", width="90%">
</p>

- Computer appears to be Joined
<p align="center">
<img src="https://imgur.com/SSYrq7t.jpg" height="90%", width="90%">
</p>

### CREATION OF A THOUSAND USER ACCOUNTS
Before now, I demonstrated the creation of a user account manually. Now, employing a script, I will create a thousand user accounts and put them in an organizational unit, named "NEW_USERS".

- Run Powershell ISE as administrator
<p align="center">
<img src="https://imgur.com/7RDp3HW.jpg" height="90%", width="90%">
</p>

- Open script
<p align="center">
<img src="https://imgur.com/M9v4SIY.jpg" height="90%", width="90%">
</p>

- Enable Execution of all scripts.
<p align="center">
<img src="https://imgur.com/f3FxYSl.jpg" height="90%", width="90%">
</p>

- Yes to all
<p align="center">
<img src="https://imgur.com/4kmDrjK.jpg" height="90%", width="90%">
</p>

- Navigate to the directory storing the "names" text file.
<p align="center">
<img src="https://imgur.com/VXrjFk0.jpg" height="90%", width="90%">
</p>

- Edit Script
<p align="center">
<img src="https://imgur.com/H8HmPcB.jpg" height="90%", width="90%">
</p>

- Run the script
<p align="center">
<img src="https://imgur.com/JS4t2WP.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/dqSK5b1.jpg" height="90%", width="90%">
</p>

- NEW_USERS organizational unit successfully created
<p align="center">
<img src="https://imgur.com/rWqkiBd.jpg" height="90%", width="90%">
</p>

- A thousand accounts created.
<p align="center">
<img src="https://imgur.com/MxGtv02.jpg" height="90%", width="90%">
</p>

- Login into one of the newly created user accounts.
<p align="center">
<img src="https://imgur.com/MxGtv02.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/b2zMK7F.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/M0LZEPt.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/qp8j4l3.jpg" height="90%", width="90%">
</p>


<p align="center">
<img src="https://imgur.com/dYyXiQ0.jpg" height="90%", width="90%">
</p>


