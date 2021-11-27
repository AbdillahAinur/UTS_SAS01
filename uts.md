# UTS Sistem Administrasi Server
***
Abdillah Ainur Ridla (1202190060) IT 02-01
***


A. Download ISO Installer windows server 2022

    https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022

- Open VirtualBox and click new

        Enter the name of the machine and type of system to use
            
    ![](Gambar\1.png)
    - Define ram, create the disk defining type and size

    ![](Gambar/2.png)

    ![](Gambar/3.png)

    ![](Gambar/4.png)
    - Go to the machine configuration and in the “Network” section set “Bridge adapter”

    ![](Gambar/5.png)
    - Click on “Start” and select the ISO downloaded

    ![](Gambar/6.png)
    - Click on “Start” and the Windows Server 2022 installation wizard will load

    ![](Gambar/7.png)
    - Click on “Install now"

    ![](Gambar/8.png)
    - Enter the license (if you have on) and then define the edition to use, Accept the license and then proceed with the installation of Windows Server 2022

    ![](Gambar/9.png)

    ![](Gambar/10.png)

    ![](Gambar/11.png)

    ![](Gambar/12.png)
    - The system will reboot to complete the process

    ![](Gambar/13.png)

    ![](Gambar/14.png)
    - Enter the administrator password

    ![](Gambar/15.png)
    - Access the menu “Input – Keyboard – Insert Ctrl + Alt + Del”. Enter the password created and wait for the configuration to load

    ![](Gambar/16.png)

    ![](Gambar/17.png)
    - Run “winver” to validate the installed edition of Windows Server

    ![](Gambar/18.png)

    ![](Gambar/19.png)
B. Instalasi Active Directory Domain Services

    - Before doing the installation, we change the computer name first by going to windows powershell. Then type "rename-computer -Newname Server2022"

         - Open powershell

    ![](Gambar/20.png)
    - Go to the "Server Manager" menu. Then select the “Manage:” option, followed by clicking “Add Roles and Features”. Then click "Next"

    ![](Gambar/21.png)

    ![](Gambar/22.png)
    - Pilih opsi “Role-based or feature-based installation”. Lalu “Next”

    ![](Gambar/23.png)
    - Click Select a server from the server pool to select a local storage directory. Then Next

    ![](Gambar/24.png)
    - Next, put a check mark in the Active Directory Domain Services box. When you check the box, on the right appears a brief description of ADDS and how it works. Then click "Add Features"

    ![](Gambar/26.png)
C. Instalasi DNS server

    - We need to install and configure the Active Directory role and DNS server to work together. Checklist DNS Servers then add features

    ![](Gambar/27.png)
D. Instalasi Net Framework 3.5

    - Checklist ".NET Framework 3.5 features"

    ![](Gambar/28.png)
    - Click Next

    ![](Gambar/29.png)
    - Click Next again

    ![](Gambar/30.png)
    - Select Install

    ![](Gambar/31.png)
    - Install sucsess

    ![](Gambar/32.png)
E. Promote Server to a Domain Controller

    - Setting to static ip using cmd, type sconfig

    ![](Gambar/33.png)

    ![](Gambar/34.png)

    ![](Gambar/36.png)
    - Setting the IP Address Server-ADDS and pointing the DNS to the static IP address used

    ![](Gambar/37.png)
    - Click “Promote this server to a domain controller for ADDS configuration

    ![](Gambar/39.png)
    - Select “Add a new forest” and enter the domain name that will be used in the Root Domain Name. For example here I use the domain "Adi.com"

    ![](Gambar/38.png)
    - Select “Windows Server 2016” at the functional level, put a check mark on “Domain Name System (DNS) server” and “Global Catalog (GC)”. And fill in the Directory Services Restore Mode password with strong password criteria

    ![](Gambar/40.png)
    - Skip the DNS Options section, then click “Next”

    ![](Gambar/41.png)
    - Fill in “The NetBIOS domain name” according to the domain name used

    ![](Gambar/42.png)
    - Skip the Paths section, click “Next”

    ![](Gambar/43.png)
    - Check the configuration specified in the Review Options, if it's ok. Click "Next"

    ![](Gambar/44.png)
    - If there is already written All prerequisite checks passed successfully. Click "Install" to apply the specified configuration

    ![](Gambar/45.png)
    - Wait until the installation process is complete

    ![](Gambar/46.png)
    - After the installation is complete, the laptop will restart automatically. Then login using administrator password

    ![](Gambar/47.png)
    - To check the configuration results, open cmd and type "netdom query fsmo"

    ![](Gambar/48.png)
    - Yuuhuuu sucsess








    

 

    



    

    

        

    
















