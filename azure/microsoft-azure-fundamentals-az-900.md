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
### **#DescribeCloudComputing**

****

* **COULD COMPUTING** -> delivery of <mark style="color:yellow;">computing services</mark> over the internet
  * _common IT infrastructure_ -> VM, storage, DB, and networking
  * _cloud services_ ->  IoT, ML, AI
  * Pros -> <mark style="color:yellow;">not constrained by physical infrastructure</mark> -> increase/decrease
*   **SHARE RESPONSIBILITY MODEL**

    * responsibilities shared between _cloud provider_ and the _customer_

    __

    <figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>
*   **COULD MODELS ->** the _deployment_ _type_ of cloud resources

    * <mark style="color:yellow;">availability</mark> is a key difference between public and private clouds
    * _hybrid cloud_ -> uses both public and private clouds in an inter-connected environment           <mark style="color:yellow;">flexibility / security</mark>
    * _multi could ->_ use multiple public cloud providers -> different feature / migration                                    <mark style="color:red;">NEED TO</mark> deal with tow public cloud providers / manage resources & security
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



### #DescribeBenefitsUsingCloud



1.  **HIGH AVAILABILITY** -> uptime / downtime&#x20;

    SLA: service-level agreements as %(eg 99.9%)
2. **SCALABILITY** -> adjust resources to meet demand.
   1. vertical scaling: vertically scale up/down to add more <mark style="color:yellow;">CPUs or RAM</mark> to the VM <mark style="color:yellow;">强化一台VM</mark>
   2. horizontal scaling -> horizontal scale out/in (either automatically or manually) to add <mark style="color:yellow;">additional VMs or containers 加VM</mark>
3. **RELIABILITY** -> the ability of a system to recover from failures and continue to function
   1. cloud decentralized design -> <mark style="color:yellow;">reliable and resilient</mark>(弹性的) infrastructure
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
   2. management in the cloud -> by using:
      * Through a web portal.
      * Using a command line interface.
      * Using APIs.
      * Using PowerShell.

###

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### #DescribeCloudServiceTypes



1. &#x20;IaaS - Infrastructure as a Service 只租硬件
   * most flexible / maximum control of your cloud resources
   * cloud provider is responsible for maintaining the hardware, network connectivity (to the internet), and physical security.
   * You’re responsible for everything else: operating system installation, configuration, and maintenance; network configuration; database and storage configuration; and so on.
   * scenarios
     * Lift-and-shift migration: You’re standing up cloud resources similar to your on-premise datacenter, and then simply moving the things running on-premise to running on the IaaS infrastructure.
     * Testing and development: You have established configurations for development and test environments that you need to rapidly replicate. You can stand up or shut down the different environments rapidly with an IaaS structure, while maintaining complete control.
2. PaaS - Platform as a Service
   * middle ground between IaaS and SaaS
   * the cloud provider maintains the physical infrastructure, physical security, and connection to the internet, <mark style="color:yellow;">operating systems, middleware, development tools, and business intelligence services that make up a cloud solution.</mark> (provide a complete development environment without the headache of maintaining all the development infrastructure.)
   * scenarios:
     * Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. Similar to the way you create an Excel macro, PaaS lets developers create applications using built-in software components. Cloud features such as scalability, high-availability, and multi-tenant capability are included, reducing the amount of coding that developers must do.
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

{% endtab %}
{% endtabs %}

###

## Azure

1.  Azure: cloud computing platform - IaaS/ PaaS/ SaaS

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
    6. Azure container instances and Azure Kubemetes services: deploy containerized applications with fully managed services
    7. Azure offers a choice of fully managed relational and in-memory databases, spanning proprietary, and open source engines
       1. Microsoft Cosmos DB support several popular NoSQL APIs.
    8. Azure AI and ML services: building, training, and deploying machine learning models
    9. Azure regional data center: distribute your application globally
    10. Azure portal: create, configure and control all your services and resources

    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/889b393a-faad-4a9b-b320-8b6aca7999c1/Untitled.png)

    your company might use a single Azure account for your business and separate subscriptions for development, marketing, and sales departments.

## Architecture and services

1. physical infrastructure
   1. data center - around the world - individual aren’t directly accessible
   2. grouped into Azure Regions/Azure Availability Zones → resiliency and reliability
      1. region: Some services or virtual machine (VM) features are only available in certain regions, such as specific VM sizes or storage types. There are also some global Azure services that don't require you to select a particular region, such as Azure Active Directory, Azure Traffic Manager, and Azure DNS.
      2. Availability zones : physically separate datacenters within an Azure region. → isolation boundary → If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.
   3. You can use availability zones to run mission-critical applications and build high-availability into your application architecture by co-locating your compute, storage, networking, and data resources within an availability zone and replicating in other availability zones
   4. Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure services that support availability zones fall into three categories
      * Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
      * Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).
      * Non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.
   5.  region pairs: Most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away

       1. allows for the replication of resources across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect an entire region.
       2. advantage:
          * If an extensive Azure outage occurs, one region out of every pair is prioritized to make sure at least one is restored as quickly as possible for applications hosted in that region pair.
          * Planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage.
          * Data continues to reside within the same geography as its pair (except for Brazil South) for tax- and law-enforcement jurisdiction purposes.

       ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9c29919b-8ef7-4cf7-8245-798d4267a669/Untitled.png)
   6. **Sovereign Regions:** instances of Azure that are isolated from the main instance of Azure.
      * US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These datacenters are operated by screened U.S. personnel and include additional compliance certifications.
      * China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters.
2. management infrastructure
   1. resource:
      1. basic building block of Azure.
      2. Anything you create, provision, deploy, etc. is a resource.
      3. Virtual Machines (VMs), virtual networks, databases, cognitive services, etc. are all considered resources within Azure.
   2. resource group:
      1. groupings of resources.
      2. When you create a resource, you’re required to place it into a resource group.
      3. a single resource can only be in one resource group at a time.
      4. Some resources may be moved between resource groups, but when you move a resource to a new group, it will no longer be associated with the former group.
      5. resource groups can't be nested
      6. action to a resource group, that action will apply to all the resources within the resource group
      7.
   3.  subscription:

       1. subscriptions are a unit of management, billing, and scale.
       2. logically organize your resource groups and facilitate billing.
       3. A subscription provides you with authenticated and authorized access to Azure products and services. provision resources
       4. links to an Azure account, which is an identity in Azure Active Directory (Azure AD) or in a directory that Azure AD trusts.
       5. An account can have multiple subscriptions,
       6. configure different billing models and apply different access-management policies.
       7. define boundraies
          * **Billing boundary**: This subscription type determines how an Azure account is billed for using Azure. You can create multiple subscriptions for different types of billing requirements. Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs.
          * **Access control boundary**: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures. An example is that within a business, you have different departments to which you apply distinct Azure subscription policies. This billing model allows you to manage and control access to the resources that users provision with specific subscriptions.
       8. you might choose to create additional subscriptions to separate:
          * **Environments**: You can choose to create subscriptions to set up separate environments for development and testing, security, or to isolate data for compliance reasons. This design is particularly useful because resource access control occurs at the subscription level.
          * **Organizational structures**: You can create subscriptions to reflect different organizational structures. For example, you could limit one team to lower-cost resources, while allowing the IT department a full range. This design allows you to manage and control access to the resources that users provision within each subscription.
          * **Billing**: You can create additional subscriptions for billing purposes. Because costs are first aggregated at the subscription level, you might want to create subscriptions to manage and track costs based on your needs. For instance, you might want to create one subscription for your production workloads and another subscription for your development and testing workloads.

       ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3a4a565e-bf84-48d6-b706-5c515e365cdf/Untitled.png)
   4. Azure managment group
      1. Azure management groups provide a level of scope above subscriptions.
      2. efficiently manage access, policies, and compliance for those subscriptions.
      3. All subscriptions within a management group automatically inherit the conditions applied to the management group, the same way that resource groups inherit settings from subscriptions and resources inherit from resource groups.
      4. enterprise-grade management at a large scale,
      5. Management groups can be nested.
      6. Important facts about management groups:
         * 10,000 management groups can be supported in a single directory.
         * A management group tree can support up to six levels of depth. This limit doesn't include the root level or the subscription level.
         * Each management group and subscription can support only one parent.
3. VM → IaaS virtual server
   1. 什么时候选：
      * Total control over the operating system (OS).
      * The ability to run custom software.
      * To use custom hosting configurations.
   2. configure, update, and maintain the software that runs on the VM.
   3. created image to rapidly provision VMs。 provision a VM in minutes when you select a preconfigured VM image
      * An image is a template used to create a VM and may already include an OS and other software, like development tools or web hosting environments.
   4. scale
      1. single VMs for testing, development, or minor tasks.
      2.  group VMs together to provide high availability, scalability, and redundancy. Azure can also manage the grouping of VMs for you with features such as scale sets and availability sets.

          1. VM scale sets:
             1. Azure can also manage the grouping of VMs for you with features such as scale sets and availability sets.
             2. Scale sets allow you to centrally manage, configure, and update a large number of VMs in minutes
          2. VM availability sets : **build a more resilient, highly available environment.**
          3. **Update domain**: The update domain groups VMs that can be rebooted at the same time. This allows you to apply updates while knowing that only one update domain grouping will be offline at a time. All of the machines in one update domain will be updated. An update group going through the update process is given a 30-minute time to recover before maintenance on the next update domain starts.
          4. **Fault domain**: The fault domain groups your VMs by common power source and network switch. By default, an availability set will split your VMs across up to three fault domains. This helps protect against a physical power or networking failure by having VMs in different fault domains (thus being connected to different power and networking resources).

          c. when to use VM

          * **During testing and development**. VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them.
          * **When running applications in the cloud**. The ability to run certain applications in the public cloud as opposed to creating a traditional infrastructure to run them can provide substantial economic benefits. For example, an application might need to handle fluctuations in demand. Shutting down VMs when you don't need them or quickly starting them up to meet a sudden increase in demand means you pay only for the resources you use.
          * **When extending your datacenter to the cloud**: An organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network. Applications like SharePoint can then run on an Azure VM instead of running locally. This arrangement makes it easier or less expensive to deploy than in an on-premises environment.
          * **During disaster recovery**: As with running certain types of applications in the cloud and extending an on-premises network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery. If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again.
4.
