# AZ-900-Microsoft-Fundamentals
Materials come from AZ-900 Microsoft Fundamentals Bootcamp

# Skills measured
Describe cloud concepts (15-20%)  
Describe core Azure services (30-35%)  
Describe security, privacy, compliance, and trust (25-30%)  
Describe Azure pricing Service Level Agreements, and Lifecycles (20-25%)  

# Section: 2. Basis. Cloud Computing Models. Regions, AZ, Management Infrastructure

<details>
<summary>Section 2: Cloud Deployment models. Private and Public clouds.</summary>

![basis](images/1-cloud-computing/1-cloud-computing.png)
![basis](images/1-cloud-computing/2-difference.png)
![basis](images/1-cloud-computing/3-azure-public-cloud-advantages.png)
![basis](images/1-cloud-computing/4-azure-public-cloud-disadvantages.png)
![basis](images/1-cloud-computing/5-azure-private-cloud-advantages.png)
![basis](images/1-cloud-computing/6-azure-hybrid-cloud-advantages.png)

</details>

## Cloud Computing Models. IaaS (rent a car), PaaS (take a taxi), SaaS (use the bus).
[Cloud Computing Models PDF](pdf-files/section-2/2.4+Cloud+Computing+Models.pdf)
1. SaaS works on a subscription based model - pay annually or monthly.  

* Cloud Advantages against other solutions:  
[Advantages of Cloud Computing PDF](pdf-files/section-2/2.5+Advantages+of+Microsoft+Azure+Cloud+Computing.pdf)

## Economies of Scale. CapEx (Capital Expenditure) vs OpEx (Operational Expenditure)
[Economies](pdf-files/section-2/2.6+Understanding+CapEx+versus+OpEx.+Economies+of+Scale..pdf)
* Upfront investments - buying taxis. And, after upfront investments, the value reduces over time.  
* If you go on your own in your business - then you will pay more. You will pay less with Azure.  

## Regions, Availability Zones (AZ), Availability Sets
[Regions and AZ PDF](pdf-files/section-2/2.7+Azure+Global+Infrastructure+-+Regions+and+Availability+Zones.pdf)
[Some additional information via link PDF](https://heranonazure.wordpress.com/2019/02/12/azure-infrastructure-geographies-regions-zones-datacenters/)

* Region us a part of one Geography + Specific service availability.  
Example of Geographies: In America there are 4 geographies: United States, Azure Government, Canada, Brazil.  

* AZ - physically separate datacenters withing Azure Region, with independent power, network and cooling.   
Example: In West Europe Region there are 3 different AZ zones - AZ-1, AZ-2, AZ-3. They are interconnected by low-latency links.  
Required for mission-critical applications.

![Availability Zone](images/1-cloud-computing/7-az.png)

* Availability Sets - is a logical grouping of two or more VMs within a DataCenter that allows Azure to understand
 how your App is build to provide redundancy and availability.
1. With Availability Sets, Azure will split your pool of VMs on different racks of servers which called "Fault Domains"
 to prevent app outage in case of unplanned maintenance events (power, hw failure, etc). Racks is really different in the datacenter.
2. The main idea - if Azure need to update the hardware or software in Fault Domain 1 - your site still be available.
![Availability Sets](images/1-cloud-computing/8-availability-sets.png)

* Region Pairs - For disaster compliance.  When the entire Azure Region goes down - you can recover your app using another Region which is in a pair with yours.  

## Azure Management Interfaces
[Azure Management PDF](pdf-files/section-2/2.8+Azure+Management+Interfaces+-+How+to+Interact+with+Azure+Cloud+Platform.pdf)  
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

## Section 2 Exam Hints
[exam hints PDF](pdf-files/section-2/2.9+Module+Completion+&+Exam+Hints.pdf)

# Section 3. Azure Core Services. Virtual Machines. Azure Managed Disks.

## Virtual Machines. (Availability sets described above)
[Virtual Machines PDF](pdf-files/section-3/3.4+Introduction+to+Azure+Virtual+Machines.pdf)
* Azure Virtual Machines represent **IaaS** Computing Model.  
The most flexible option.
Types:
1. General Purpose - (Balanced CPU and Memory)  
2. Compute Optimized - (High CPU, lower memory)  
3. Memory Optimized - (High memory, lower CPU)  
4. Storage Optimized - (High disk throughput and IOPS)  
5. GPU - (Heave rendering traffic)  
6. High Performance Compute - (Most Powerful CPUs)  

[More information about sizes link](https://docs.microsoft.com/en-us/azure/virtual-machines/sizes-general)

## Virtual Machines Networking, VMs High Availability. Vnet.
[Virtual Networking, VM, High Availability. PDF](pdf-files/section-3/3.5+Azure+VMs+Networking+and+High+Availability+Fundamentals+101.pdf)
* vNET - Azure Virtual Networks. Enable to communicate between VMs and over the internet with you on-prem machines.
* vNET - is equivalent of **VPC** in AWS Cloud.
* Allow you using SSH to connect to your Virtual Machines throw Public IP address inside your vNET.
![Vnet pic](images/3-virtual-machines/vNets.png)

* Virtual Machine Scale Sets - group of idential VMs under Load Balancer.
 The number of instances can be automatically increase and decrease according network load.
![VM scale sets](images/3-virtual-machines/2-virtual-machines-scale-set.png)
##### Bear in mind! They can be stored in a same AZ


* Azure Batch - large-scale job scheduler. Let you make huge jobs, creating and managing tens\hundreds\thousands of VMs (pools of VMs) under the hood.
![VM Batch](images/3-virtual-machines/3-Azure-batch.png)

## Azure Managed Disks.
* Azure managed disks are block-level storage volumes that are managed by Azure and used with Azure Virtual Machines.  
Managed disks are like a physical disk in an on-premises server but, virtualized.
**Azure will provision the disk on their own, you just specify the size of your virtual disk**
[More information about disks link](https://docs.microsoft.com/en-us/azure/virtual-machines/managed-disks-overview)
* 4 disk types to aim the specific customer scenarios:
1. Ultra disk (IO-intensive: SQL, Oracle and other transaction-heavy workloads)
2. Premium SSD (Production)
3. Standard SSD (Web services, lightly enterprise apps)
4. Standard HDD  (Backups, non-critical apps)
