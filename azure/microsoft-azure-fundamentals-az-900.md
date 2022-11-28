---
description: certification - fundamental
---

# Microsoft Azure Fundamentals (AZ-900)

> **Microsoft Azure** is a cloud computing platform with an ever-expanding set of services to help you build solutions to meet your business goals. Azure services support everything from simple to complex. Azure has simple web services for hosting your business presence in the cloud. Azure also supports running fully virtualized computers managing your custom software solutions. Azure provides a wealth of cloud-based services like remote storage, database hosting, and centralized account management. Azure also offers new capabilities like artificial intelligence (AI) and Internet of Things (IoT) focused services.

<mark style="color:yellow;">**Describe cloud concepts 25-30%**</mark>

<mark style="color:yellow;">**Describe Azure architecture and services 35-40%**</mark>

<mark style="color:yellow;">**Describe Azure management and governance 30-35%**</mark>

{% tabs %}
{% tab title="cloud concepts" %}
### **#Describe Cloud Computing**

****

* **COULD COMPUTING** -> delivery of <mark style="color:yellow;">computing services</mark> over the internet
  * _common IT infrastructure_ -> VM, storage, DB, and networking
  * _cloud services_ ->  IoT, ML, AI
  * Pros -> <mark style="color:yellow;">not constrained by physical infrastructure</mark> -> increase/decrease
*   **SHARE RESPONSIBILITY MODEL**

    * responsibilities shared between _cloud provider_ and the _customer_

    <figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption><p>share responsibility model</p></figcaption></figure>
*   **COULD MODELS ->** the _deployment_ _type_ of cloud resources

    * <mark style="color:yellow;">availability</mark> is a key difference between public and private clouds
    * _hybrid cloud_ -> uses both public and private clouds in an inter-connected environment -> <mark style="color:yellow;">flexibility / security</mark>
    * _multi could ->_ use multiple public cloud providers -> different feature / migration                                    <mark style="color:red;">NEED TO</mark> deal with two public cloud providers / manage resources & security
    * tool manage cloud -> _Azure Arc_
    * _VM -> Azure VM ->_ run VM workloads in Azure with seamless integration & scalability

    | Basic Cloud                                                           | Private Cloud                                                      | Hybrid Cloud                                                      |
    | --------------------------------------------------------------------- | ------------------------------------------------------------------ | ----------------------------------------------------------------- |
    | No capital expenditures to scale up                                   | Organizations have complete control over resources and security    | Provides the most flexibility                                     |
    | Applications can be quickly provisioned and deprovisioned             | Data is not collocated with other organizations’ data              | Organizations determine where to run their applications           |
    | Organizations pay only for what they use                              | Hardware must be purchased for startup and maintenance             | Organizations control security, compliance, or legal requirements |
    | Organizations don’t have complete control over resources and security | Organizations are responsible for hardware maintenance and updates |                                                                   |



{% hint style="info" %}
_Capital expenditure (**CapEx**)_: a one-time, up-front expenditure to purchase or secure tangible(有形的) resources <mark style="color:yellow;">买</mark>

_Operational expenditure (**OpEx**)_: spending money on services or products over time <mark style="color:yellow;">租</mark> -> cloud computing
{% endhint %}

* **CONSUMPTION-BASED MODEL**
  * No upfront costs <mark style="color:yellow;">不预付</mark> / No need to purchase and manage costly infrastructure <mark style="color:yellow;">不买硬件</mark> / pay fo more resources when they're needed <mark style="color:yellow;">只付用的</mark> / stop paying for resources that are no longer needed <mark style="color:yellow;">不用不付</mark>&#x20;
  * Plan and manage your operating costs / Run your infrastructure more efficiently / Scale as your business needs change



### #Describe Benefits of Using Cloud



1.  **HIGH AVAILABILITY** -> uptime / downtime&#x20;

    SLA: service-level agreements as %(eg 99.9%)
2. **SCALABILITY** -> adjust resources to meet demand.
   1. vertical scaling: vertically scale up/down to add more <mark style="color:yellow;">CPUs or RAM</mark> to the VM <mark style="color:yellow;">强化一台VM</mark>
   2. horizontal scaling -> horizontal scale out/in (either automatically or manually) to add <mark style="color:yellow;">additional VMs or containers 加VM</mark>
3. **RELIABILITY** -> the ability of a system to recover from failures and continue to function
   1. cloud decentralized design -> <mark style="color:yellow;">reliable and resilient</mark> infrastructure
   2. deploy in regions around the world, always running
   3. self-designed auto shift / cloud auto shift
4. **PREDICTABILITY**:&#x20;
   1. performance predictability: predicting the <mark style="color:yellow;">resources needed to deliver a positive experience</mark> for your customers -> autoscaling, load balancing, and high availability
   2. cost predictability: predicting or forecasting the <mark style="color:yellow;">cost of the cloud spend</mark>
      1. track your resource use in real time
      2. monitor resources to ensure that you’re using them in the most efficient way
      3. apply data analytics to find patterns and trends that help better plan resource deployments
      4. predict future cost
      5. tools: Total Cost of Ownership (TCO) or Pricing Calculator
5. **GOVERNANCE AND COMPLIANCE**
   1. set templates help ensure that all your deployed resources meet corporate standards and government regulatory requirements
   2. update all your deployed resources to new standards as standards change.
   3. cloud-based auditing helps flag any resource that’s out of compliance with your corporate standards and provides mitigation strategies.
6. **SECURITY**
   1. self maximum control of security : IaaS
   2. patches and maintenance taken care auto: PaaS / SaaS
   3. cloud provider handle DDoS...
7. **MANAGEABILITY <- MAJOR BENEFIT**
   1. management of the cloud -> you can:
      * Automatically scale resource deployment based on need.
      * Deploy resources based on a preconfigured template, removing the need for manual configuration.
      * Monitor the health of resources and automatically replace failing resources.
      * Receive automatic alerts based on configured metrics, so you’re aware of performance in real time.
   2.  management in the cloud -> by using:

       * Through a web portal.
       * Using a command line interface.
       * Using APIs.
       * Using PowerShell.



### #Describe Cloud Service Types



<figure><img src="../.gitbook/assets/image (2) (2).png" alt=""><figcaption><p>shared responsibility model</p></figcaption></figure>

1. &#x20;IaaS - Infrastructure as a Service 只租硬件
   * most flexible / maximum control of your cloud resources
   * cloud provider is responsible for maintaining the <mark style="color:yellow;">hardware, network connectivity (to the internet), and physical security.</mark>
   * You’re responsible for everything else: operating system installation, configuration, and maintenance; network configuration; database and storage configuration; and so on.
   * scenarios
     * Lift-and-shift migration: on-premise -> cloud
     * Testing and development: You have established configurations for development and test environments that you need to rapidly replicate.&#x20;
2. PaaS - Platform as a Service
   * middle ground between IaaS and SaaS
   * the cloud provider maintains the physical infrastructure, physical security, and connection to the internet, <mark style="color:yellow;">operating systems, middleware, development tools, and business intelligence services that make up a cloud solution.</mark> (provide a complete development environment without the headache of maintaining all the development infrastructure.)
   * scenarios:
     * Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. Cloud features such as scalability, high-availability, and multi-tenant capability are included, reducing the amount of coding that developers must do.
     * Analytics or business intelligence: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions.
3. SaaS - Software as a Service
   * most complete cloud service model from a product perspective
   * renting or using a fully developed application. Email, financial software, messaging applications, and connectivity software are all common examples of a SaaS implementation.
   * least flexible, easiest to get up and running, requires the least amount of technical knowledge or expertise to fully employ.
   * scenarios:
     * Email and messaging.
     * Business productivity applications.
     * Finance and expense tracking.
{% endtab %}

{% tab title="Azure Architecture and Services" %}
### #Core Architectural Components of Azure

1.  **AZURE**: cloud computing platform - IaaS/ PaaS/ SaaS

    1. Virtual Machine running on the cloud - complete control
       1. create virtual machines from scratch
       2. upload your own virtual hard drive
       3. from templates Azure provides
    2. Cloud-based storage: Web and database
       1. store your application or backup data safely and securely
    3. Computing services: AI, ML, IoT
    4. Azure’s app services:
       1. provide a scalable hosting platform where developers can create web based applications using popular development frameworks
       2. easily deploy, operate, and scale your apps in a fully managed env
    5. Azure functions: event driven, serverless applications with no coding
    6. Azure container instances and Azure Kubernetes services: deploy containerized applications with fully managed services
    7. Azure offers a choice of fully managed relational and in-memory databases, spanning proprietary, and open source engines
       1. Microsoft Cosmos DB support several popular NoSQL APIs.
    8. Azure AI and ML services: building, training, and deploying machine learning models
    9. Azure regional data center: distribute your application globally
    10. Azure portal: create, configure and control all your services and resources&#x20;



    <figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>your company might use a single Azure account for your business and separate subscriptions for development, marketing, and sales departments.</p></figcaption></figure>
2. **PHYSICAL INFRASTRUCTURE**
   1. Datacenter - around the world - grouped into Azure Regions/Azure Availability Zones → resiliency and reliability
   2. Region: a geographical area on the planet contains at least one datacenter.&#x20;
      * Some services or virtual machine (VM) features are only available in certain regions, such as specific VM sizes or storage types. There are also some global Azure services that don't require you to select a particular region, such as Azure Active Directory, Azure Traffic Manager, and Azure DNS.
   3.  Availability Zones : physically separate datacenters within an Azure region, connected through high-speed, private fiber-optic networks.&#x20;

       * isolation boundary → independent power, cooling, networking
       * <mark style="color:yellow;">run mission-critical applications and build high-availability</mark> into your application architecture -> replication
       * primarily for <mark style="color:yellow;">VMs, managed disks, load balancers, and SQL databases</mark>.
       * not all Azure Regions currently support availability zones

       <figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>minimum of 3 separate AZ in AZ-enabled regions -> resiliency</p></figcaption></figure>

       * &#x20;Azure services that support availability zones fall into three categories
         * Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
         * Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
         * Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.
   4.  Region Pairs: Azure regions are paired with another regions within the same geography (such as US, Europe, or Asia) at least 300 miles away -> replication across geography

       * advantage: quick restore / minimize downtime and risk for update / data reside same geography as its pairs(except for Brazil South) for tax- and law-enforcement jurisdiction purposes.

       <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Not all Azure services automatically replicate data or automatically fall back from a failed region to cross-replicate to another enabled region. In these scenarios, recovery and replication must be configured by the customer.</p></figcaption></figure>
   5.  Sovereign Regions -> instances that isolated from the main instances -> for compliance and legal purpose

       * US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These datacenters are operated by screened U.S. personnel and include additional compliance certifications.
       * China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters.

       &#x20;instances of Azure that are isolated from the main instance of Azure.
3. **MANAGEMENT INFRASTRUCTURE**
   1. resource -> basic building block of Azure.
      1. Anything you create, provision, deploy, etc. is a resource.
      2. Virtual Machines (VMs), virtual networks, databases, cognitive services, etc. are all considered resources within Azure.
   2. resource group:
      1. resource must be created into a resource group.
      2. can only be in one resource group at a time.
      3. Some resources may be moved between resource groups, no longer be associated with the former group.
      4. can't be nested.
      5. action to a resource group, that action will apply to all the resources within the resource group. eg. grant access.
   3. subscription -> a unit of management, billing, and scale.
      1. logically organize your resource groups and facilitate billing.
      2. Azure Account -> Azure Active Directory(Azure AD) -> subscriptions -> provides you with authenticated and authorized access to Azure products and services. provision resources
      3. multi-subscription account, configure different billing models and apply different access-management policies.
      4. define boundaries around Azure products, services, and resources:
         * **Billing boundary**:  how an Azure account is billed for using Azure. different billing requirements -> separate billing reports and invoices
         * **Access control boundary**: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures. different departments -> different subscriptions&#x20;
      5. you might choose to create additional subscriptions to separate:
         * **Environments**: for development and testing, security, or to isolate data for compliance reasons -> resource access control occurs at the subscription level.
         * **Organizational structures**: reflect different organizational structures -> manage and control access to the resources that users provision within each subscription.
         * **Billing**: costs are first aggregated at the subscription level -> manage and track costs based on your needs -> one for production workloads and another subscription for your development and testing workloads.
   4. Azure management group -> a level of scope above subscriptions.
      1. efficiently manage access, policies, and compliance for those subscriptions.
      2. **Create a hierarchy that applies a policy.** All subscriptions within a management group automatically inherit the conditions applied to the management group, the same way that resource groups inherit settings from subscriptions and resources inherit from resource groups.
      3. **Provide user access to multiple subscriptions**. Enterprise-grade management at a large scale. Management groups can be nested.
      4.  Important facts about management groups:

          * 10,000 management groups can be supported in a single directory.
          * A management group tree can support up to six levels of depth. This limit doesn't include the root level or the subscription level.
          * Each management group and subscription can support only one parent.



          <figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
4. Create Virtual Machine

{% hint style="info" %}
Azure Portal -> create a resource -> compute -> virtual Machine -> create
{% endhint %}



### #Azure Compute and Networking Services

1. AVM
   1. AVM → IaaS virtualized server
      * Total control over the operating system (OS).
      * Run custom software.
      * Use custom hosting configurations.
      * configure, update, and maintain the software that runs on the VM.
      * create or use an already created image to rapidly provision VMs
        * An image is a template used to create a VM and may already include an OS and other software, like development tools or web hosting environments.
   2. Scale VMs -> group VMs together to provide high availability, scalability, and redundancy -> scale sets and availability sets.
      1. VM scale sets&#x20;
         * centrally manage, configure, and update a large number of VMs in minutes.
         * the number of VM instances can automatically increase or decrease in response to demand, or you can set it to scale based on a defined schedule.&#x20;
         * VMSS also automatically deploy a load balancer to make sure that your resources are being used efficiently.&#x20;
         * compute, big data, and container workloads.
      2. VM availability sets : **build a more resilient, highly available environment -->** designed to ensure that VMs stagger updates 错开更新 and have varied power and network connectivity 不同的电源和网络, preventing you from losing all your VMs with a single network or power failure.
         * **Update domain**: The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates while knowing that only one update domain grouping will be offline at a time. All of the machines in one update domain will be updated. An update group going through the update process is given a <mark style="color:yellow;">30-minute time to recover</mark> before maintenance on the next update domain starts.
         * **Fault domain**: The fault domain groups your VMs by common power source and network switch. By default, an availability set will split your VMs across up to <mark style="color:yellow;">three fault domains</mark>. This helps protect against a physical power or networking failure by having VMs in different fault domains (thus being connected to different power and networking resources).
         * no additional cost for configuring an availability set
   3. when to use VM
      * During testing and development
      * When running applications in the cloud
      * When extending your datacenter to the cloud
      * During disaster recovery
      * move to the cloud with VMs -> create image of pysical server and host
   4. VM resources:
      * Size (purpose, number of processor cores, and amount of RAM)
      * Storage disks (hard disk drives, solid state drives, etc.)
      * Networking (virtual network, public IP address, and port configuration)
2. AVD&#x20;
   1. AVD
      * a desktop and application virtualization service that runs on the cloud
      * a cloud-hosted version of Windows
      * works across devices and operating systems (Win ->remote desktop connection), and works with apps that you can use to access remote desktops or most modern browsers
      * provides centralized security management for users' desktops with Azure Active Directory. You can enable multifactor authentication to secure user sign-ins. You can also secure access to data by assigning granular role-based access controls (RBACs) to users.
   2. enhance security
      * confidential data being left on a personal device is reduced
      * user sessions are isolated in both single and multi-session environments
   3. Multi-session Win10 Win 11 deployment ->multiple concurrent users on a single VM / more consist
3. Azure Containers
   1.

### #Azure Storage Services

### #Azure Identity, Access, and Security





```bash
#powerShell CLI
pwsh
#bash CLI
bash

az version
az upgrade
#enter interactive mode - Azure CLI
az interactive
version
upgrade
exit

#------VM--------#
#create VM
az vm create \
  --resource-group learn-b4cabd12-4bf9-4343-8b12-a0838fe78ea7 \
  --name my-vm \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys

#use the Custom Script Extension to run a Bash script on your VM. 
az vm extension set \
  --resource-group learn-b4cabd12-4bf9-4343-8b12-a0838fe78ea7 \
  --vm-name my-vm \
  --name customScript \
  --publisher Microsoft.Azure.Extensions \
  --version 2.1 \
  --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' \
  --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
  
#------VM--------#


```
{% endtab %}
{% endtabs %}
