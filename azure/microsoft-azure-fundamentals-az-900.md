---
description: certification - fundamental
---

# Microsoft Azure Fundamentals (AZ-900)

> **Microsoft Azure** is a cloud computing platform with an ever-expanding set of services to help you build solutions to meet your business goals. Azure services support everything from simple to complex. Azure has simple web services for hosting your business presence in the cloud. Azure also supports running fully virtualized computers managing your custom software solutions. Azure provides a wealth of cloud-based services like remote storage, database hosting, and centralized account management. Azure also offers new capabilities like artificial intelligence (AI) and Internet of Things (IoT) focused services.

<mark style="color:yellow;">**Describe cloud concepts 25-30%**</mark>

<mark style="color:yellow;">**Describe Azure architecture and services 35-40%**</mark>

<mark style="color:yellow;">**Describe Azure management and governance 30-35%**</mark>

{% tabs %}
{% tab title="Cloud Concepts" %}
### **#Describe Cloud Computing**

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

{% tab title="Core Architectural Components" %}
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
{% endtab %}

{% tab title="Compute & Networking" %}
### #Azure Compute and Networking Services

1. AVM&#x20;
   1. AVM → IaaS virtualized server (hardware level virtualization)
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
3. Azure Containers  -> OS level virtualization -> protabilibly and performance
   1. container -> virtualization environment -> run multiple containers on a single physical or virtual host ->&#x20;
      * lightweight and designed to be created , scaled out, and stopped dynamically -> more agile
      * don't manage the operating system for a container
      * most popular container engines is Docker, supported by Azure
   2. Azure Container Instances -> PaaS
   3. Use ->microservice architecture -> break solutions into smaller, independent pieces
      * For example, you might split a website into a container hosting your front end, another hosting your back end, and a third for storage. This split allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.
4.  Azure Functions ->an event-driven, serverless compute option -> no VM/C

    benefits:

    * only concerned about the code running your service and not about the underlying platform or infrastructure
    * Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.
    * Functions scale automatically based on demand, so they may be a good choice when demand is variable.
    * Functions can be either stateless or stateful.&#x20;
      * stateless (the default), restarted every time they respond to an event
      * stateful (called Durable Functions), a context is passed through the function to track prior activity.
    * Functions are a key component of serverless computing. They're also a general compute platform for running any type of code. This flexibility allows you to manage scaling, run on virtual networks, and even completely isolate the functions.
5. Application Hosting Options -> VM or C
   1. Azure App Service&#x20;
      * enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure&#x20;
      * automatic scaling and high availability
      * supports Windows and Linux
      * automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.
   2. App Service handles most of the infrastructure decisions you deal with in hosting web-accessible apps:
      * Deployment and management are integrated into the platform.
      * Endpoints can be secured.
      * Sites can be scaled quickly to handle high traffic loads.
      * The built-in load balancing and traffic manager provide high availability.
   3. type:&#x20;
      * **Web Apps** -> App Service includes full support for hosting web apps by using ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python. You can choose either Windows or Linux as the host operating system.
      * **API apps** -> you can build REST-based web APIs by using your choice of language and framework. You get full Swagger support and the ability to package and publish your API in Azure Marketplace. The produced apps can be consumed from any HTTP- or HTTPS-based client.
      * **WebJobs** -> You can use the WebJobs feature to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app. They can be scheduled or run by a trigger. WebJobs are often used to run background tasks as part of your application logic.
      *   **Mobile apps** -> quickly build a back end for iOS and Android apps. With just a few actions in the Azure portal, you can:

          * Store mobile app data in a cloud-based SQL database.
          * Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook.
          * Send push notifications.
          * Execute custom back-end logic in C# or Node.js.

          \-> there's SDK support for native iOS and Android, Xamarin, and React native apps.
6. Azure Virtual Networking
   1. Azure virtual networks and virtual subnets enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers.
   2. Azure virtual networks provide the following key networking capabilities:
      * Isolation and segmentation&#x20;
        * allows you to create multiple isolated virtual networks.&#x20;
        * When you set up a virtual network, you define a private IP address space by using either public or private IP address ranges. The IP range only exists within the virtual network and isn't internet routable. You can divide that IP address space into subnets and allocate part of the defined address space to each named subnet.
        * For name resolution, you can use the name resolution service that's built into Azure. You also can configure the virtual network to use either an internal or an external DNS server.
      * Internet communications -> enable incoming connections from the internet by assigning a public IP address to an Azure resource, or putting the resource behind a public load balancer
      * Communicate between Azure resources
        * Virtual networks can connect not only VMs but other Azure resources, such as the App Service Environment for Power Apps, Azure Kubernetes Service, and Azure virtual machine scale sets.
        * Service endpoints can connect to other Azure resource types, such as Azure SQL databases and storage accounts. This approach enables you to link multiple Azure resources to virtual networks to improve security and provide optimal routing between resources.
      *   Communicate with on-premises resources

          you can create a network that spans both your local and cloud environments. There are three mechanisms for you to achieve this connectivity:

          * **Point-to-site virtual private network** connections are from a computer outside your organization back into your corporate network. In this case, the client computer initiates an encrypted VPN connection to connect to the Azure virtual network.
          * **Site-to-site virtual private networks** link your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network. In effect, the devices in Azure can appear as being on the local network. The connection is encrypted and works over the internet.
          * **Azure ExpressRoute** provides a dedicated private connectivity to Azure that doesn't travel over the internet. ExpressRoute is useful for environments where you need greater bandwidth and even higher levels of security.
      * Route network traffic
        * Route tables allow you to define rules about how traffic should be directed. You can create custom route tables that control how packets are routed between subnets.
        * Border Gateway Protocol (BGP) works with Azure VPN gateways, Azure Route Server, or Azure ExpressRoute to propagate on-premises BGP routes to Azure virtual networks.
      * Filter network traffic
        * **Network security groups** are Azure resources that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol.
        * **Network virtual appliances** are specialized VMs that can be compared to a hardened network appliance. A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization.
      * Connect virtual networks
        * You can link virtual networks together by using virtual network peering
        * Peering allows two virtual networks to connect directly to each other.&#x20;
        * Network traffic between peered networks is private, and travels on the Microsoft backbone network, never entering the public internet.&#x20;
        * Peering enables resources in each virtual network to communicate with each other.&#x20;
        * These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.
        * User-defined routes (UDR) allow you to control the routing tables between subnets within a virtual network or between virtual networks. This allows for greater control over network traffic flow.
   3. supports both public and private endpoints to enable communication between external or internal resources with other internal resources.
7. Azure Virtual Private Networks&#x20;
   1. VPN
      1. uses an encrypted tunnel within another network
      2. VPNs are typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet).&#x20;
      3. Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks.&#x20;
      4. VPNs can enable networks to safely and securely share sensitive information.
   2. VPN gateway -> virtual network gateway.&#x20;
      * Azure VPN Gateway instances are deployed in a dedicated subnet of the virtual network and enable the following connectivity:
        * Connect on-premises datacenters to virtual networks through a **site-to-site** connection.
        * Connect individual devices to virtual networks through a **point-to-site** connection.
        * Connect virtual networks to other virtual networks through a **network-to-network** connection.
      * only one VPN gateway in each virtual network, use one gateway to connect to multiple locations, which includes other virtual networks or on-premises datacenters.
   3. VPN type ->how traffic to be encrypted is specifie
      1. Policy-based VPN gateways specify statically the IP address of packets that should be encrypted through each tunnel. This type of device evaluates every data packet against those sets of IP addresses to choose the tunnel where that packet is going to be sent through.
      2. In Route-based gateways
         * IPSec tunnels are modeled as a network interface or virtual tunnel interface. IP routing (either static routes or dynamic routing protocols) decides which one of these tunnel interfaces to use when sending each packet. Route-based VPNs are the preferred connection method for on-premises devices. They're more resilient to topology changes such as the creation of new subnets.
         * Use a route-based VPN gateway if you need any of the following types of connectivity:
           * Connections between virtual networks
           * Point-to-site connections
           * Multisite connections
           * Coexistence with an Azure ExpressRoute gateway
   4. High-availability and fault tolerant VPN configuration -> maximize the resiliency
      * active / standby: VPN gateways are deployed as two instances in an active/standby configuration. When planned maintenance or unplanned disruption affects the active instance, the standby instance automatically assumes responsibility for connections without any user intervention. Connections are interrupted during this failover, but they're typically restored within a few seconds for planned maintenance and within 90 seconds for unplanned disruptions.
      * active / active: With the introduction of support for the BGP routing protocol, In this configuration, you assign a unique public IP address to each instance. You then create separate tunnels from the on-premises device to each IP address. You can extend the high availability by deploying an additional VPN device on-premises.
      * ExpressRoute failover: configure a VPN gateway as a secure failover path for ExpressRoute connections**.** ExpressRoute circuits have resiliency built in. 仍会因physical problems断连, you can also provision a VPN gateway that uses the internet as an alternative method of connectivity
      * Zone-Redundant gateways: In regions that support availability zones, VPN gateways and ExpressRoute gateways can be deployed in a zone-redundant configuration. resiliency, scalability, and higher availability. protecting your on-premises network connectivity to Azure from zone-level failures. These gateways require different gateway SKUs and use Standard public IP addresses instead of Basic public IP addresses.
8. Azure ExpressRoute -> extend your on-premises networks into the Microsoft cloud over a private connection -> help connectivity provider -> establish connections to Microsoft cloud services, such as Microsoft Azure and Microsoft 365. connect offices, datacenters, or other facilities to the Microsoft cloud. Each location would have its own ExpressRoute circuit.
   1. benefits using ExpressRoute as the connection service between Azure and on-premises networks.
      * Connectivity to Microsoft cloud services across all regions in the geopolitical region.
      * Global connectivity to Microsoft services across all regions with the ExpressRoute Global Reach.
      * Dynamic routing between your network and Microsoft via Border Gateway Protocol (BGP).
      * Built-in redundancy in every peering location for higher reliability.
   2. connectivity:
      * Microsoft Office 365
      * Microsoft Dynamics 365
      * Azure compute services, such as Azure Virtual Machines
      * Azure cloud services, such as Azure Cosmos DB and Azure Storage
9.
10. Azure DNS
{% endtab %}

{% tab title="Storage Services" %}
### #Azure Storage Services

1. **STORAGE ACCOUNTS**
2. **STORAGE REDUNDANCY**
3. **STORAGE SERVICES**
4. **IDENTIFY AZURE DATA MIGRATION OPTIONS**
5. **IDENTIFY AZURE FILE MOVEMENT OPTIONS**
6. ****
7.
{% endtab %}

{% tab title="Identity, Access & Security" %}
### #Azure Identity, Access and Secuirty

1. **AZURE DIRECTORY SERVICES**
2. **AZURE AUTHENTICATION METHODS**
3. **AZURE EXTERNAL IDENTITIES**
4. **AZURE CONDITIONAL  ACCESS**
5. **AZURE ROLE-BASED ACCESS CONTROL**
6. **ZERO TRUST MODEL**
7. **DEFENSE-IN-DEPTH**
8. **MICROSOFT DEFENDER FOR CLOUD**
9. ****
10.
{% endtab %}

{% tab title="Azure Management and Governance" %}
### #Cost Management

1. **FACTORS THAT CAN AFFECT COSTS IN AZURE**
2. **COMPARE THE PRICING AND TOTAL COST OF OWNERSHIP CALCULATORS**
3. **AZURE COST MANAGEMENT TOOL**
4. **THE PURPOSE OF TAGS**

### #Features and Tools for Governance and Compliance

1. **AZURE BLUEPRINTS**
2. **AZURE POLICY**
3. **RESCOURCE LOCKS**
4. **SERVICE TRUST PORTAL**

### #Features and Tools for Managing and Deploying Azure Resources

1. **TOOLS FOR INTERACTING WITH AZURE**
2. **PURPOSE OF AZURE ARC**
3. **AZURE RESOURCE MANAGER AND AZURE ARM TEMPLATES**

### #Monitoring Tools

1. **PURPOSE OF AZURE ADVISOR**
2. **AZURE SERVICE HEALTH**
3. **AZURE MONITOR**
{% endtab %}
{% endtabs %}

{% code overflow="wrap" lineNumbers="true" %}
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
  
#Configure network access
#get ip address
az vm list-ip-addresses
#store the result as a Bash variable:
IPADDRESS="$(az vm list-ip-addresses \
  --resource-group learn-586543ae-5ede-4079-a9e3-00c534ce1240 \
  --name my-vm \
  --query "[].virtualMachine.network.publicIpAddresses[*].ipAddress" \
  --output tsv)"
#connect
curl --connect-timeout 5 http://$IPADDRESS
#list network security groups
az network nsg list \
  --resource-group learn-586543ae-5ede-4079-a9e3-00c534ce1240 \
  --query '[].name' \
  --output tsv
#list the rules associated with the NSG named my-vmNSG:
az network nsg rule list \
  --resource-group learn-586543ae-5ede-4079-a9e3-00c534ce1240 \
  --nsg-name my-vmNSG
#use --query argument to retrieve only the name, priority, affected ports, and access (Allow or Deny) for each rule
az network nsg rule list \
  --resource-group learn-586543ae-5ede-4079-a9e3-00c534ce1240 \
  --nsg-name my-vmNSG \
  --query '[].{Name:name, Priority:priority, Port:destinationPortRange, Access:access}' \
  --output table
# create network security rule port 80
az network nsg rule create \
  --resource-group learn-586543ae-5ede-4079-a9e3-00c534ce1240 \
  --nsg-name my-vmNSG \
  --name allow-http \
  --protocol tcp \
  --priority 100 \
  --destination-port-range 80 \
  --access Allow 


```
{% endcode %}

