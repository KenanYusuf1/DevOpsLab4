# Installation and Configuration Report: Grafana on Azure VM

## Introduction
This report outlines the steps undertaken to install and configure Grafana on an Ubuntu Virtual Machine (VM) hosted on Microsoft Azure. The process aimed to set up Grafana for monitoring and visualization purposes, integrating it within a cloud infrastructure for enhanced data analysis and dashboarding capabilities.

## Objectives
- Deploy an Ubuntu VM on Microsoft Azure.
- Install and configure Grafana on the Ubuntu VM.
- Integrate Grafana with data sources available within the Azure environment for monitoring purposes.

## Environment Setup
- **VM Details:**
  - **Name:** cst8919lab4641_z1
  - **Network Interface:** Cst8919Lab4-vnet / default
  - **Public IP Address:** 4.206.217.248
  - **Private IP Address:** 10.0.0.4
  - **Network Security Group:** Cst8919Lab4-nsg
  - **Accelerated Networking:** Disabled

## Installation Steps
1. **VM Deployment:** Deployed an Ubuntu VM on Azure, ensuring network connectivity and security settings were in place.
2. **Grafana Installation:** Installed Grafana using the official package repository, ensuring all dependencies were resolved without issues.
3. **Service Configuration:** Enabled and started the Grafana service, confirming it was running and accessible on the VM's IP address on port 3000.
4. **Firewall Configuration:** Configured the VM's network security group to allow inbound traffic on port 3000, ensuring Grafana's web interface was accessible.

## Encountered Issue: Azure App Registration Access
- **Description:** During the process of integrating Grafana with Azure data sources, it was necessary to register Grafana as an application within Azure AD to allow it to query Azure resources. However, access to Azure App Registrations was not available, preventing the completion of Grafana's integration with Azure data sources.
- **Impact:** The inability to register Grafana as an application in Azure AD halted the integration process, limiting Grafana's functionality to local data sources or manual data input. This issue restricted the scope of monitoring and visualization capabilities that could be achieved through Grafana.
- **Resolution Attempts:**
  - **Contacted IT Support:** Reached out to the IT support team to request access to Azure App Registrations.
  - **Documentation Review:** Reviewed Azure and Grafana documentation for alternative integration methods or temporary workarounds.
- **Current Status:** Awaiting response from IT support regarding access to Azure App Registrations. The installation and basic configuration of Grafana on the VM are complete, but full integration with Azure resources remains pending.

## Conclusion
The installation and initial configuration of Grafana on an Azure-hosted Ubuntu VM were successfully completed, with Grafana accessible via the VM's public IP address. However, the project objectives were partially met due to limitations encountered with Azure App Registrations. The resolution of this access issue is crucial for the complete integration of Grafana with Azure data sources, enabling comprehensive monitoring and visualization capabilities within the Azure environment.
