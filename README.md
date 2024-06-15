# Azure Hybrid Active Directory Home Lab

## Overview
This project demonstrates the setup and configuration of a hybrid Active Directory (AD) environment integrating on-premises infrastructure with Azure. The lab environment consists of a VMWare virtual home lab running a Windows Server 2019 domain controller and Windows 10 clients, configured to sync with Azure for hybrid identity management and seamless single sign-on (SSO).

## Project Goals
- Set up a VMWare virtual home lab with a Windows Server 2019 domain and Windows 10 clients.
- Configure domain settings, server name, TCP/IP settings, and remote desktop.
- Modify Active Directory templates and create/link Group Policy Objects (GPOs) for user accounts.
- Implement Azure Connect Sync for hybrid Entra ID join and SSO using password hash synchronization.

## Lab Setup

### 1. VMWare Virtual Home Lab
- **Environment**: VMWare Workstation/Fusion
- **Domain Controller**: Windows Server 2019
- **Clients**: Windows 10

### 2. Windows Server 2019 Configuration
- **Domain Settings**: Define domain name, server name, and configure TCP/IP settings.
- **Remote Desktop**: Enable and configure remote desktop for remote management.

### 3. Active Directory Configuration
- **AD Templates**: Modify default templates to meet lab requirements.
- **Group Policy Objects (GPOs)**: Create and link GPOs to manage user and computer settings within the domain.

### 4. Azure Integration
- **Azure AD Connect**: Install and configure Azure AD Connect to synchronize on-premises AD with Azure AD.
- **Hybrid Entra ID Join**: Enable hybrid Azure AD join for seamless SSO.
- **Password Hash Synchronization**: Configure password hash synchronization for secure user authentication across environments.

## Detailed Steps

### Assembling the VMWare Virtual Home Lab
1. **Install VMWare**: Set up VMWare Workstation/Fusion on your host machine.
2. **Create Virtual Machines**: Create virtual machines for Windows Server 2019 and Windows 10 clients.
3. **Install Operating Systems**: Install Windows Server 2019 on the domain controller VM and Windows 10 on the client VMs.

### Configuring Windows Server 2019
1. **Define Domain Settings**:
    - Open Server Manager and select 'Add roles and features'.
    - Install the Active Directory Domain Services (AD DS) role.
    - Promote the server to a domain controller, setting the desired domain name.
2. **Configure TCP/IP Settings**:
    - Assign a static IP address to the server.
    - Configure DNS settings to point to the domain controller’s IP.
3. **Enable Remote Desktop**:
    - Open System Properties and enable remote desktop.
    - Configure firewall settings to allow remote desktop connections.

### Modifying Active Directory and GPOs
1. **Modify AD Templates**:
    - Use Active Directory Users and Computers to modify default templates.
2. **Create and Link GPOs**:
    - Open Group Policy Management.
    - Create new GPOs for desired policies and link them to the appropriate Organizational Units (OUs).

### Implementing Azure AD Connect Sync
1. **Install Azure AD Connect**:
    - Download and install Azure AD Connect on the domain controller.
    - Configure synchronization settings to sync on-premises AD with Azure AD.
2. **Enable Hybrid Azure AD Join**:
    - Configure device options in Azure AD Connect to enable hybrid Azure AD join.
3. **Configure Password Hash Synchronization**:
    - Enable password hash synchronization during the Azure AD Connect setup.

## Conclusion
This project showcases a comprehensive approach to integrating on-premises Active Directory with Azure, providing a robust hybrid identity solution. By following the steps outlined, you can achieve seamless SSO and secure user authentication across your hybrid environment. This setup is ideal for demonstrating practical knowledge of AD, Azure integration, and hybrid identity management to potential employers.
