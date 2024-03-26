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

# Conclusion 2

## Initial Challenges and Switching Subscriptions

...successfully overcame the initial hurdles. After encountering persistent issues with the client secret and permissions within my primary Azure subscription, which hindered the Grafana integration with Azure services, I decided to switch to a different Azure subscription. This move proved to be pivotal.

## Creating New App Registrations

Upon switching, I promptly initiated the process of creating new App Registrations within Azure Active Directory. The experience gained from previous attempts enabled a smoother and more informed setup. With the new App Registration in place, I generated a fresh client secret, carefully ensuring its correct implementation within the Grafana configuration.

## Assigning Roles to Service Principal

The next crucial step was to assign the necessary role to the `grafana-azure` service principal. This involved granting it the "Reader" role at the subscription level, thereby ensuring it had sufficient permissions to retrieve data from Azure Monitor, Log Analytics, and the Resource Graph. This role assignment was a key element that facilitated the successful integration between Grafana and Azure services.

## Grafana Dashboard Configuration

Finally, with all configurations correctly in place and permissions adequately assigned, I ventured into Grafana to begin the creation of dashboards. To my satisfaction, I was able to connect to the Azure data sources without any of the previous authentication issues. The graphs began to populate, reflecting the Azure resources and metrics I intended to monitor. This not only marked the resolution of the challenges faced but also the beginning of a comprehensive monitoring setup that leveraged Grafana's powerful visualization capabilities.

## Reflecting on the Journey

In conclusion, the shift to a different Azure subscription and the subsequent steps taken to rectify the initial obstacles underscored the importance of proper access permissions and the correct configuration of service principals in Azure. This experience highlighted the intricate relationship between cloud resources and third-party tools and the need for a thorough understanding of their integration mechanisms. It was a reminder of the resilience required in the face of technical challenges and the satisfaction of achieving a fully functional monitoring solution that leverages the best of Azure and Grafana's capabilities.

