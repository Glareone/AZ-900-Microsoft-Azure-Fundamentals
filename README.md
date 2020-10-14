# AZ-900-Microsoft-Fundamentals
Materials come from AZ-900 Microsoft Fundamentals Bootcamp

# Skills measured
Describe cloud concepts (15-20%)  
Describe core Azure services (30-35%)  
Describe security, privacy, compliance, and trust (25-30%)  
Describe Azure pricing Service Level Agreements, and Lifecycles (20-25%)  

<details>
<summary>Section 2: Cloud Deployment models. Private and Public clouds.</summary>

[basis](images/1-cloud-computing/1-cloud-computing.png)
[basis](images/1-cloud-computing/2-difference.png)
[basis](images/1-cloud-computing/3-azure-public-cloud-advantages.png)
[basis](images/1-cloud-computing/4-azure-public-cloud-disadvantages.png)
[basis](images/1-cloud-computing/5-azure-private-cloud-advantages.png)
[basis](images/1-cloud-computing/6-azure-hybrid-cloud-advantages.png)

</details>

# Cloud Computing Models
[Cloud Computing Models](pdf-files/section-2/2.4+Cloud+Computing+Models.pdf)
* Cloud Advantages against other solutions:
[Cloud Computing Models](pdf-files/section-2/2.5+Advantages+of+Microsoft+Azure+Cloud+Computing.pdf)

# Economies of Scale. CapEx (Capital Expenditure) vs OpEx (Operational Expenditure)
[Economies](pdf-files/section-2/2.6+Understanding+CapEx+versus+OpEx.+Economies+of+Scale..pdf)
* Upfront investments - buying taxis. And after upfront investments the value reduces over time.  
* If you go on your own in your business - then you will pay more. You will pay less with Azure.  

# Regions, Availability Zones (AZ)
[Regions and AZ](pdf-files/section-2/2.7+Azure+Global+Infrastructure+-+Regions+and+Availability+Zones.pdf)
[Some additional information via link](https://heranonazure.wordpress.com/2019/02/12/azure-infrastructure-geographies-regions-zones-datacenters/)

* Region us a part of one Geography + Specific service availability.  
Example of Geographies: In America there are 4 geographies: United States, Azure Government, Canada, Brazil.  

* AZ - physically separate datacenters withing Azure Region.   
Example: In West Europe Region there are 3 different AZ zones - AZ-1, AZ-2, AZ-3. They are interconnected by low-latency links.  
Required for mission-critical applications.

* Region Pairs - For disaster compliance.  When the entire Azure Region goes down - you can recover your app using another Region which is in a pair with yours.  

# Azure Management Interfaces
[Azure Management](pdf-files/section-2/2.8+Azure+Management+Interfaces+-+How+to+Interact+with+Azure+Cloud+Platform.pdf)
* Azure Portal

* Azure CLI (Command Line Interface) - console for Windows\Mac\Linux
* Azure PowerShell module - mostly the same as a CLI option. Also, it is a console with additional command line abilities.  
Allow you to use scripts and make some automations.  

* Azure Cloud Shell
Browser-accessible pre-configured virtual machine (all required applications is already installed)  
1. Accessible from Azure Portal, from shell.azure.com and from Azure Mobile App.  

* Azure SDK
Collections of libraries for developers.

* Azure Mobile App
Monitoring the health and servers statuses, Run commands, diagnose and fix issues.