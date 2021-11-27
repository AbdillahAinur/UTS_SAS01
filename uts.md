# UTS Sistem Administrasi Server
***
Abdillah Ainur Ridla (1202190060) IT 02-01
***


A. Download ISO Installer windows server 2022

    https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022

- Open VirtualBox and click new

        Enter the name of the machine and type of system to use
            
    ![](Gambar/1.PNG)
    - Define ram, create the disk defining type and size

    ![](Gambar/2.PNG)

    ![](Gambar/3.PNG)

    ![](Gambar/4.PNG)
    - Go to the machine configuration and in the “Network” section set “Bridge adapter”

    ![](Gambar/5.PNG)
    - Click on “Start” and select the ISO downloaded

    ![](Gambar/6.PNG)
    - Click on “Start” and the Windows Server 2022 installation wizard will load

    ![](Gambar/7.PNG)
    - Click on “Install now"

    ![](Gambar/8.PNG)
    - Enter the license (if you have on) and then define the edition to use, Accept the license and then proceed with the installation of Windows Server 2022

    ![](Gambar/9.PNG)

    ![](Gambar/10.PNG)

    ![](Gambar/11.PNG)

    ![](Gambar/12.PNG)
    - The system will reboot to complete the process

    ![](Gambar/13.PNG)

    ![](Gambar/14.PNG)
    - Enter the administrator password

    ![](Gambar/15.PNG)
    - Access the menu “Input – Keyboard – Insert Ctrl + Alt + Del”. Enter the password created and wait for the configuration to load

    ![](Gambar/16.PNG)

    ![](Gambar/17.PNG)
    - Run “winver” to validate the installed edition of Windows Server

    ![](Gambar/18.PNG)

    ![](Gambar/19.PNG)
B. Instalasi Active Directory Domain Services

    - Before doing the installation, we change the computer name first by going to windows powershell. Then type "rename-computer -Newname Server2022"

         - Open powershell

    ![](Gambar/20.PNG)
    - Go to the "Server Manager" menu. Then select the “Manage:” option, followed by clicking “Add Roles and Features”. Then click "Next"

    ![](Gambar/21.PNG)

    ![](Gambar/22.PNG)
    - Pilih opsi “Role-based or feature-based installation”. Lalu “Next”

    ![](Gambar/23.PNG)
    - Click Select a server from the server pool to select a local storage directory. Then Next

    ![](Gambar/24.PNG)
    - Next, put a check mark in the Active Directory Domain Services box. When you check the box, on the right appears a brief description of ADDS and how it works. Then click "Add Features"

    ![](Gambar/26.PNG)
C. Instalasi DNS server

    - We need to install and configure the Active Directory role and DNS server to work together. Checklist DNS Servers then add features

    ![](Gambar/27.PNG)
D. Instalasi Net Framework 3.5

    - Checklist ".NET Framework 3.5 features"

    ![](Gambar/28.PNG)
    - Click Next

    ![](Gambar/29.PNG)
    - Click Next again

    ![](Gambar/30.PNG)
    - Select Install

    ![](Gambar/31.PNG)
    - Install sucsess

    ![](Gambar/32.PNG)
E. Promote Server to a Domain Controller

    - Setting to static ip using cmd, type sconfig

    ![](Gambar/33.PNG)

    ![](Gambar/34.PNG)

    ![](Gambar/36.PNG)
    - Setting the IP Address Server-ADDS and pointing the DNS to the static IP address used

    ![](Gambar/37.PNG)
    - Click “Promote this server to a domain controller for ADDS configuration

    ![](Gambar/39.PNG)
    - Select “Add a new forest” and enter the domain name that will be used in the Root Domain Name. For example here I use the domain "Adi.com"

    ![](Gambar/38.PNG)
    - Select “Windows Server 2016” at the functional level, put a check mark on “Domain Name System (DNS) server” and “Global Catalog (GC)”. And fill in the Directory Services Restore Mode password with strong password criteria

    ![](Gambar/40.PNG)
    - Skip the DNS Options section, then click “Next”

    ![](Gambar/41.PNG)
    - Fill in “The NetBIOS domain name” according to the domain name used

    ![](Gambar/42.PNG)
    - Skip the Paths section, click “Next”

    ![](Gambar/43.PNG)
    - Check the configuration specified in the Review Options, if it's ok. Click "Next"

    ![](Gambar/44.PNG)
    - If there is already written All prerequisite checks passed successfully. Click "Install" to apply the specified configuration

    ![](Gambar/45.PNG)
    - Wait until the installation process is complete

    ![](Gambar/46.PNG)
    - After the installation is complete, the laptop will restart automatically. Then login using administrator password

    ![](Gambar/47.PNG)
    - To check the configuration results, open cmd and type "netdom query fsmo"

    ![](Gambar/48.PNG)
    - Yuuhuuu sucsess








    

 

    



    

    

        

    
















