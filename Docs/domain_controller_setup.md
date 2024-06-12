# Domain Controller Setup

This document provides detailed steps to set up a new domain controller named "soc.team" using Windows Server 2022 and to add users Cyril and Arjun.

## Step 1: Install Windows Server 2022

1. Download and install Windows Server 2022 on your virtual machine.
2. Complete the initial setup and configuration of the server.

## Step 2: Install Active Directory Domain Services (AD DS)

1. Open **Server Manager** from the Start menu.
2. In the Server Manager Dashboard, click on **Add roles and features**.
3. In the **Add Roles and Features Wizard**:
   - Click **Next** on the **Before you begin** page.
   - Select **Role-based or feature-based installation** and click **Next**.
   - Select the server you want to install AD DS on and click **Next**.
   - On the **Select server roles** page, check **Active Directory Domain Services**. Click **Add Features** when prompted, then click **Next**.
   - Click **Next** on the **Features** page.
   - Click **Next** on the **AD DS** page.
   - Click **Install** on the **Confirmation** page.

4. Wait for the installation to complete, then click **Close**.

## Step 3: Promote the Server to a Domain Controller

1. In the Server Manager, you will see a notification flag indicating **Post-deployment Configuration**. Click on it and select **Promote this server to a domain controller**.
2. In the **Deployment Configuration** wizard:
   - Select **Add a new forest**.
   - Enter the **Root domain name** as `soc.team` and click **Next**.
   
   ![Root domain name](https://github.com/Sanjulm10/ELK-project-/blob/c14a5fac5463c07174e296507ce2e7d058dc7aa6/screen/WhatsApp%20Image%202024-05-30%20at%2018.23.52_f921c1c0.jpg)

3. On the **Domain Controller Options** page:
   - Ensure **Domain Name System (DNS) server** and **Global Catalog (GC)** are checked.
   - Set the **Directory Services Restore Mode (DSRM) password** and click **Next**.
   
   ![Domain Controller Options](https://github.com/Sanjulm10/ELK-project-/blob/c14a5fac5463c07174e296507ce2e7d058dc7aa6/screen/WhatsApp%20Image%202024-05-30%20at%2018.23.43_ab29f111.jpg)

4. Continue through the wizard, leaving default selections where appropriate, and click **Next** until you reach the **Install** page.

   ![Install Page](https://github.com/Sanjulm10/ELK-project-/blob/c14a5fac5463c07174e296507ce2e7d058dc7aa6/screen/Screenshot%202024-05-30%20181825.png)

5. Click **Install**. The server will restart once the installation is complete.

   ![Post-Install](https://github.com/Sanjulm10/ELK-project-/blob/c14a5fac5463c07174e296507ce2e7d058dc7aa6/screen/2024-05-30%2022_49_34-AD%20%5BRunning%5D%20-%20Oracle%20VM%20VirtualBox.png).

## Step 4: Create Organizational Units and Users

1. After the server restarts, log in with the domain administrator account.
2. Open **Active Directory Users and Computers** from the Start menu.
3. In the left pane, right-click on the domain (soc.team), select **New** > **Organizational Unit**.
   - Name the OU **HR** and click **OK**.
   - Repeat to create another OU named **NOC**.

### Create Users

1. In the left pane, expand the **soc.team** domain, right-click on the **HR** OU, and select **New** > **User**.
2. Fill in the details for the user Cyril:
   - **First name**: Cyril
   - **User logon name**: cyril@soc.team
   - Click **Next**.
3. Set the password for Cyril and configure the password settings. Click **Next**, then **Finish**.
4. Repeat the process to create a user named Arjun in the **HR** OU:
   - **First name**: Arjun
   - **User logon name**: arjun@soc.team

  ![Domain Controller Setup](https://github.com/Sanjulm10/ELK-project-/blob/d04c3ab9b87338b01f8c143bb86f505fa2fbf702/screen/2024-05-30%2019_29_27-AD%20%5BRunning%5D%20-%20Oracle%20VM%20VirtualBox.png)

![Domain Controller Setup](https://github.com/Sanjulm10/ELK-project-/blob/5c5a10bd6ca3756698930534b3c89fe4759f0e2e/screen/2024-05-30%2019_30_37-AD%20%5BRunning%5D%20-%20Oracle%20VM%20VirtualBox.png)

## Screenshot



[Back to Main Page](../README.md)
