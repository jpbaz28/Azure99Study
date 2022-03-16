# Azure 99 Study Guide

## Cloud Computing

- Delivery of computing services over the internet
  - Storage, databases, networking, software, analytics, and intelligence
- Benefits
  - Innovation
  - Economies of Scale
  - Typically Cheaper
    - pay as you go
    - a way to rent compute power and storage from someone else's data center
    - billed only for what you use
    - only used for time you need them
  - Works well with agile development methodologies
    - current trend is to release features in smaller batches
    - days/weeks time instead of months/years
  - Cloud provides on demand access
    - nearly limitless pool of raw compute, storage, and networking components
    - speech recognition and other cognitive services that help make your application stand out
    - analytics services that deliver telemetry data from your software and devices
  - High Availability
    - depending on the service-level agreement (SLA) that you choose, your cloud-based apps can provide a continuous user experience with no apparent downtime, even when things go wrong
  - Scalability
    - scale vertically to increase compute capacity by adding RAM or CPUs to a virtual machine
    - scaling horizontally increases compute capacity by adding instances of resources, such as adding VMs to the configuration
  - Elasticity
    - you can configure cloud-based apps to take advantage of autoscaling, so your apps always have the resources they need
  - Agility
    - deploy and configure cloud-based resources quickly as your app requirements change
  - Geo-distribution
    - datacenters around the globe, your customers always have the best performance in their region
  - Disaster Recovery
    - cloud-based backup services, data replication, and geo-distribution
  - Consumption-based model
    - No upfront costs
    - No need to purchase and manage costly infrastructure that users might not use to its fullest
    - The ability to pay for additional resources when they are needed
    - The ability to stop paying for resources that are no longer needed

### **Capital expenses vs. operating expenses**

- Capital Expenditure (CapEx) is the up-front spending of money on physical infrastructure, and then deducting that up-front expense over time. The up-front cost from CapEx has a value that reduces over time
- Operational Expenditure (OpEx) is spending money on services or products now, and being billed for them now. You can deduct this expense in the same year you spend it. There is no up-front cost, as you pay for a service or product as you use it
- On Premises equipment is categorized as CapEx, because a capital investment was made
- Cloud services, on the other hand, are categorized as an OpEx, because of their consumption model
  - the cloud service provider (Azure) manages the costs that are associated with the purchase and lifespan of the physical equipment

## Different Cloud Service Models

1. Public Cloud
   - Services are offered over the public internet and available to anyone who wants to purchase them
   - Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet
   - No capital expenditures to scale up
   - Applications can be quickly provisioned and deprovisioned
   - Organizations pay only for what they use
2. Private Cloud
   - Consists of computing resources used exclusively by users from one business or organization
   - Physically located at your organization's on-premises datacenter, or it can be hosted by a third-party service provider
   - Hardware must be purchased for start-up and maintenance
   - Organizations have complete control over resources and security
   - Organizations are responsible for hardware maintenance and updates
3. Hybrid Cloud
   - A computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them
   - Provides the most flexibility
   - Organizations determine where to run their applications
   - Organizations control security, compliance, or legal requirements## Different Cloud Models

### **Cloud Service Model Acronyms**

#### _These models define the different levels of shared responsibility that a cloud provider and cloud tenant are responsible for_

1. **IaaS - Infrastructure-as-a-Service**

   - closest to managing physical servers
   - cloud provider will keep the hardware up-to-date, but operating system maintenance and network configuration is up to the cloud tenant
     - I.E. Azure virtual machines are fully operational virtual compute devices running in Microsoft datacenters.

   #### **Advantages:**

   - Most flexible category of cloud services
     - Instead of buying hardware, with IaaS, you rent it
     - you have control to configure and manage the hardware running your application
   - No CapEx. Users have no up-front costs
   - Agility. Applications can be made accessible quickly, and deprovisioned whenever needed
   - Management
     - the user manages and maintains the services they have provisioned, and the cloud provider manages and maintains the cloud infrastructure
   - Consumption-based model
     - Organizations pay only for what they use and operate under an Operational Expenditure (OpEx) model
   - Skills. No deep technical skills are required to deploy, use, and gain the benefits of a public cloud
   - Cloud benefits. Organizations can use the skills and expertise of the cloud provider to ensure workloads are made secure and highly available

2. **PaaS - Platform-as-a-Service**
   - a managed hosting environment
   - focus on application development
   - cloud provider manages the virtual machines and networking resources, and the cloud tenant deploys their applications into the managed hosting environment
     - I.E. Azure App Services provides a managed hosting environment where developers can upload their web applications, without having to worry about the physical hardware and software requirements
   #### **Advantages**
   - No CapEx. Users have no up-front costs
   - Agility. PaaS is more agile than IaaS, and users don't need to configure servers for running applications
   - Consumption-based model. Users pay only for what they use, and operate under an OpEx model
   - Skills. No deep technical skills are required to deploy, use, and gain the benefits of PaaS
   - Cloud benefits. Users can take advantage of the skills and expertise of the cloud provider to ensure that their workloads are made secure and highly available
     - In addition, users can gain access to more cutting-edge development tools. They can then apply these tools across an application's lifecycle
   - Productivity. Users can focus on application development only, because the cloud provider handles all platform management
     - Working with distributed teams as services is easier because the platform is accessed over the internet
   #### **Disadvantage**
   - Platform limitations. There can be some limitations to a cloud platform that might affect how an application runs
     - When evaluating which PaaS platform is best suited for a workload, consider any limitations in this area
3. **SaaS - Software-as-a-Service**
   - software that's centrally hosted and managed for you and your users or customers
   - cloud provider manages all aspects of the application environment, such as virtual machines, networking resources, data storage, and applications
   - cloud tenant only needs to provide their data to the application managed by the cloud provider
     - I.E. Microsoft Office 365 provides a fully working version of Microsoft Office that runs in the cloud
     - All you need to do is create your content, and Office 365 takes care of everything else
   #### **Advantages**
   - No CapEx. Users have no up-front costs
   - Agility. Users can provide staff with access to the latest software quickly and easily
   - Pay-as-you-go pricing model. Users pay for the software they use on a subscription model, typically monthly or yearly, regardless of how much they use the software
   - Skills. No deep technical skills are required to deploy, use, and gain the benefits of SaaS
   - Flexibility. Users can access the same application data from anywhere
   #### **Disadvantage**
   - Software limitations. There can be some limitations to a software application that might affect how users work
     - when using as-is software, you don't have direct control of features
     - when evaluating which SaaS platform is best suited for a workload, consider any business needs and software limitations

- ![iaas-paas-saas example](screenshots\iaas-paas-saas-575a09e9.png)
- ![iaas-paas-saas differences](screenshots\shared-responsibility-76efbc1e.png)

## Serverless Computing

- Like PaaS, serverless computing enables developers to build applications faster by eliminating the need for them to manage infrastructure
- With serverless applications, the cloud service provider automatically provisions, scales, and manages the infrastructure required to run the code
- Serverless architectures are highly scalable and event-driven, only using resources when a specific function or trigger occurs
- Important to note that servers are still running the code
- "Serverless" name comes from the fact that the tasks associated with infrastructure provisioning and management are invisible to the developer
  - Approach enables developers to increase their focus on the business logic, and deliver more value to the core of the business

## Azure

- What is Azure?
  - A continually expanding set of cloud services
  - build, manage, and deploy apps on a massive global network using your favorite tools and frameworks
- What does Azure offer?
  - Future-proofing
    - Continuous innovation from Microsoft supports your development today and your product visions for tomorrow
  - Flexible builds gives many options for deployment
    - commitment to open source, and support for all languages and frameworks
  - Hybrid Cloud integration
    - tools and services designed for a hybrid cloud solution included
  - Security features
  - Azure provides more than 100 services
    - running your existing applications on virtual machines
    - exploring new software paradigms, such as intelligent bots and mixed reality
    - AI and machine-learning services
    - storage solutions

## Azure Portal

- Web-based, unified console that provides an alternative to command-line tools
  - Build, manage, and monitor everything from simple web apps to complex cloud deployments
  - Create custom dashboards for an organized view of resources
  - Configure accessibility options for an optimal experience
- Designed for resiliency and continuous availability
  - maintains a presence in every Azure datacenter
  - updates continuously and requires no downtime for maintenance activities
  - resiliency to individual datacenter failures
  - avoids network slowdowns by being geographically close to users

## Azure Marketplace

- Azure Marketplace customers can find, try, purchase, and provision applications and services from hundreds of leading service providers
  - Microsoft partners, independent software vendors, and startups
  - solutions and services are certified to run on Azure

## Tour of Azure Services

- 10 Major categories
  1. Compute
     - VMs
     - Functions
     - container instances
     - Kubernetes Service
  2. Networking
     - Virtual Network
     - DNS
     - DDOS Protectiom
     - Content Delivery Network
     - Firewall
     - VPNs
     - Load Balancers
  3. Storage
     - Queue
     - Table
     - File
     - Blob
  4. Mobile
     - Mobile backend services
       - iOS, Android, and Windows
     - Offline data synchronization
     - Broadcast push notifications
     - Connectivity to on-premises data
       -Autoscaling to match business needs
  5. Databases
     - CosmosDB
     - MySQL
     - Postgres
     - SQL Server on Azure VM
     - DB Migration Service
     - MariaDB
  6. Web
     - App Service
     - API Management
     - Notification Hubs
  7. Internet of Things (IoT)
     - IoT Central
     - IoT Hub
     - IoT Edge
  8. Big Data
     - Open source cluster services
     - Help run analytics at massive scale
     - Synapse Analytics
     - HDInsight
     - Databricks
  9. AI
     - Machine Learning Service
     - ML Studio
     - Cognitive Services
       - Vision
       - Speech
       - Knowledge Mapping
       - Bing Search
       - Natural Language Processing
  10. DevOps
      - Automating software delivery to users
      - Continuous Integration
      - Continuous Deployment
      - Continuous Delivery
      - Az DevOps
      - Az DevTest Labs

## Create and Use Azure Account/Subscription

- Purchase Azure access directly from Microsoft by signing up on the Azure website or through a Microsoft representative
- Azure Free Account
  - Free access to popular Azure products for 12 months
  - A credit to spend for the first 30 days
  - Access to more than 25 products that are always free
  - To sign up, you need a phone number, a credit card, and a Microsoft or GitHub account
  - You won't be charged for any services until you upgrade to a paid subscription
- Azure free student account
  - Free access to certain Azure services for 12 months
  - A credit to use in the first 12 months
  - Free access to certain software developer tools
  - gives $100 credit and free developer tools
  - you can sign up without a credit card
- Learn Sandbox
  - many of the Learn exercises use a technology called the sandbox
    - creates a temporary subscription that's added to your Azure account
    - temporary subscription allows you to create Azure resources for the duration of a Learn module
    - When completing a Learn module, you're welcome to use your personal subscription to complete the exercises in a module
    - sandbox is preferred though because you can create and test Azure resources at no cost

## Differences between Subscriptions, Management groups, and Resources

- Resources
  - instances of services that you create, like virtual machines, storage, or SQL databases
- Resource Groups
  - logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed
- Subscriptions
  - groups together user accounts and the resources that have been created by those user accounts
  - for each subscription, there are limits or quotas on the amount of resources that you can create and use
  - organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects
- Management Groups
  - help you manage access, policy, and compliance for multiple subscriptions
  - all subscriptions in a management group automatically inherit the conditions applied to the management group
- ![subs, m groups, resources hierarchy](screenshots\hierarchy-372fef74.png)

## Azure regions, availability zones, and region pairs

- Resources are created in regions, which are different geographical locations around the globe that contain Azure datacenters

  - Azure is made up of datacenters located around the globe.
  - When you use a service or create a resource such as a SQL database or virtual machine (VM), you're using physical equipment in one or more of these locations

- **Region**
  - geographical area on the planet that contains at least one but potentially multiple datacenters that are nearby and networked together with a low-latency network
  - when you deploy a resource in Azure, you'll often need to choose the region where you want your resource deployed
    - examples of regions are West US, Canada Central, West Europe, Australia East, and Japan West
  - _Advantages_
    - regions give you the flexibility to bring applications closer to your users no matter where they are
    - global regions provide better scalability and redundancy. They also preserve data residency for your services
  - _Special Azure Regions_
    - US DoD Central, US Gov Virginia, US Gov Iowa and more
      - these regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners
      - these datacenters are operated by screened U.S. personnel and include additional compliance certifications
    - China East, China North, and more
      - These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters
- **Availability Zones**
  - _Not every region has support for availability zones_
  - when you host your infrastructure, setting up your own redundancy requires that you create duplicate hardware environments
  - Azure can help make your app highly available through availability zones
  - Availability zones are physically separate datacenters within an Azure region
    - each one is made up of one or more datacenters equipped with independent power, cooling, and networking
    - set up to be an isolation boundary. If one zone goes down, the other continues working
    - connected through high-speed, private fiber-optic networks
  - build high-availability into your application architecture by co-locating your compute, storage, networking, and data resources within a zone and replicating in other zones
  - primarily for VMs, managed disks, load balancers, and SQL databases
  - services that support availability zones fall into three categories
    1. zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses)
    2. zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database)
    3. non-regional services: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages
- **Azure Region Pairs**
  - each Azure region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away
  - allows for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect both regions at once
    - if a region in a pair was affected by a natural disaster, for instance, services would automatically failover to the other region in its region pair.
    - examples of region pairs in Azure are West US paired with East US and SouthEast Asia paired with East Asia
  - _Additional Advantages_
    - if an extensive Azure outage occurs, one region out of every pair is prioritized to make sure at least one is restored as quickly as possible for applications hosted in that region pair
    - planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage
    - data continues to reside within the same geography as its pair (except for Brazil South) for tax- and law-enforcement jurisdiction purposes
  ## Azure Resources and Resource Manager
  - Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for resources deployed on Azure
  - All resources must be in a resource group, and a resource can only be a member of a single resource group
  - Many resources can be moved between resource groups with some services having specific limitations or requirements to move
  - Resource groups can't be nested. Before any resource can be provisioned, you need a resource group for it to be placed in
  - **Logical Grouping**
    - placing resources of similar usage, type, or location in a resource group, you can provide order and organization to resources you create in Azure
  - **Life Cycle**
    - If you delete a resource group, all resources contained within it are also deleted
    - Organizing resources by life cycle can be useful in nonproduction environments, where you might try an experiment and then dispose of it
    - Resource groups make it easy to remove a set of resources all at once
  - **Authorization**
    - Resource groups are also a scope for applying role-based access control (RBAC) permissions
    - By applying RBAC permissions to a resource group, you can ease administration and limit access to allow only what's needed
  - **Azure Resource Manager**
    - Azure Resource Manager is the deployment and management service for Azure
    - Provides a management layer that enables you to create, update, and delete resources in your Azure account
    - use management features like access control, locks, and tags to secure and organize your resources after deployment
    - _Benefits of using Resource Manager_
      - Manage your infrastructure through declarative templates rather than scripts. A Resource Manager template is a JSON file that defines what you want to deploy to Azure
      - Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually
      - Redeploy your solution throughout the development life cycle and have confidence your resources are deployed in a consistent state
      - Define the dependencies between resources so they're deployed in the correct order
      - Apply access control to all services because RBAC is natively integrated into the management platform
      - Apply tags to resources to logically organize all the resources in your subscription
      - Clarify your organization's billing by viewing costs for a group of resources that share the same tag
- ![Resource Manager](screenshots\consistent-management-layer-feef9259.png)

## Azure subscriptions and management groups

- Azure requires an Azure subscription
- subscription provides you with authenticated and authorized access to Azure products and services
- Azure subscription is a logical unit of Azure services that links to an Azure account, which is an identity in Azure Active Directory (Azure AD) or in a directory that Azure AD trusts
- account can have one subscription or multiple subscriptions that have different billing models and to which you apply different access-management policies
- There are two types of subscription boundaries that you can use
  1. _Billing boundary_: This subscription type determines how an Azure account is billed for using Azure. You can create multiple subscriptions for different types of billing requirements
  - Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs
  2. _Access control boundary_: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures
  - This billing model allows you to manage and control access to the resources that users provision with specific subscriptions
- _Customize billing to meet your needs_
  - If you have multiple subscriptions, you can organize them into invoice sections
  - Each invoice section is a line item on the invoice that shows the charges incurred that month
  - Depending on your needs, you can set up multiple invoices within the same billing account
- **Azure Management Groups**
  - If your organization has many subscriptions, you might need a way to efficiently manage access, policies, and compliance for those subscriptions
  - You organize subscriptions into containers called management groups and apply your governance conditions to the management groups
  - All subscriptions within a management group automatically inherit the conditions applied to the management group
- **Hierarchy of management groups and subscriptions**
  - You can build a flexible structure of management groups and subscriptions to organize your resources into a hierarchy for unified policy and access management
    - For example, you could limit VM locations to the US West Region in a group called Production
    - This policy will inherit onto all the Enterprise Agreement subscriptions that are descendants of that management group and will apply to all VMs under those subscriptions
    - This security policy can't be altered by the resource or subscription owner, which allows for improved governance.
    - Another scenario where you would use management groups is to provide user access to multiple subscriptions
- **Important facts about management groups**
  - 10,000 management groups can be supported in a single directory
  - A management group tree can support up to six levels of depth. This limit doesn't include the root level or the subscription level
  - Each management group and subscription can support only one parent
  - Each management group can have many children
  - All subscriptions and management groups are within a single hierarchy in each directory

## Azure Databases and Analytics Services

- **Azure Cosmos DB**
  - globally distributed, multi-model database service
  - you can elastically and independently scale throughput and storage across any number of Azure regions worldwide
  - Azure Cosmos DB provides comprehensive service level agreements for throughput, latency, availability, and consistency guarantees
  - supports schema-less data, which lets you build highly responsive and "Always On" applications to support constantly changing data
  - at the lowest level, Azure Cosmos DB stores data in atom-record-sequence (ARS) format
  - data is then abstracted and projected as an API, which you specify when you're creating your database
    - choices include SQL, MongoDB, Cassandra, Tables, and Gremlin
  - as you migrate your company's databases to Azure Cosmos DB, your developers can stick with the API that they're the most comfortable with
- **Azure SQL DB**
  - relational database based on the latest stable version of the Microsoft SQL Server database engine
  - high-performance, reliable, fully managed, and secure database
  - platform as a service (PaaS) database engine
  - handles most of the database management functions, such as upgrading, patching, backups, and monitoring, without user involvement
  - provides 99.99 percent availability
  - Microsoft handles all updates to the SQL and operating system code
  - enables you to process both relational data and non-relational structures, such as graphs, JSON, spatial, and XML
  - can use advanced query processing features, such as high-performance, in-memory technologies and intelligent query processing
  - _Migration from onPrem_
    - migrate your existing SQL Server databases with minimal downtime by using the Azure Database Migration Service
    - Microsoft Data Migration Assistant can generate assessment reports that provide recommendations to help guide you through required changes prior to performing a migration
    - The Azure Database Migration Service performs all of the required steps. You just change the connection string in your apps
- **_Create a SQL DB_**
  1. Sign in to the Azure portal
  2. Select Create a resource > Databases > SQL database. The Create SQL Database pane appears
  3. Select Subscription and Resource Group
  4. Add DB Name to field
  5. Server: Select create new
  6. The Create SQL Database Server pane appears
  7. enter globally unique name for server name
  8. Select location
  9. Select authentication method(Use SQL Authentication is a good default choice)
  10. Enter server admin login and password
  11. Select OK
  12. Complete remaining fields for create SQL DB
  - ![Create SQL DB](screenshots\server-pane-df80b536.png)
  13. Select Next:Networking
  14. Connectivity method: Public endpoint
  15. Fill out remaining relevant options
  - ![Networking SQL DB](screenshots\tab-8a36cd61.png)
  16. Select Next : Security, and for Enable Azure Defender for SQL, choose Not now. Leave the remaining settings as default (not configured)
  - ![Security SQL DB](screenshots\security-tab-a15c3422.png)
  17. Select Next : Additional settings
  18. Fill out relevant fields, select existing data if migrating
  - ![Additional Settings](screenshots\additional-settings-tab-5e601100.png)
  19. Select Review + create to validate configuration entries
  20. Select Create to deploy the server and database. It can take approximately two to five minutes to create the server and deploy the sample database. The deployment pane shows the status, with updates for each resource that is created
  21. When deployment is complete, select Go to resource. The db1 SQL database Overview pane shows the essentials of the newly deployed database
  22. In the command bar, select Set server firewall. The Firewall settings page appears
  23. Set Allow Azure services and resources to access this server to Yes, leaving other settings as default
  24. In the command bar, select Save to update firewall settings, and then close the Firewall settings pane
- **Azure DB for MySQL**
  - Azure Database for MySQL is a relational database service in the cloud, and it's based on the MySQL Community Edition database engine, versions 5.6, 5.7, and 8.0
  - 99.99 percent availability service level agreement from Azure, powered by a global network of Microsoft-managed datacenters
  - built-in security, fault tolerance, and data protection that you would otherwise have to buy or design, build, and manage
  - you can use point-in-time restore to recover a server to an earlier state, as far back as 35 days
  - Scale as needed, within seconds
  - Automatic backups
  - Enterprise-grade security and compliance
  - Predictable performance and inclusive, pay-as-you-go pricing
  - Built-in high availability with no additional cost
  - you can migrate your existing MySQL databases with minimal downtime by using the Azure Database Migration Service
  - Azure Database for MySQL offers several service tiers, and each tier provides different performance and capabilities to support lightweight to heavyweight database workloads
- **Azure DB for PostgresSQL**
  - Azure Database for PostgreSQL is a relational database service in the cloud
  - based on the community version of the open-source PostgreSQL database engine
  - Built-in high availability compared to on-premises resources. There's no additional configuration, replication, or cost required to make sure your applications are always available
  - Simple and flexible pricing. You have predictable performance based on a selected pricing tier choice that includes software patching, automatic backups, monitoring, and security
  - Scale up or down as needed, within seconds. You can scale compute or storage independently as needed, to make sure you adapt your service to match usage
  - Adjustable automatic backups and point-in-time-restore for up to 35 days
  - Enterprise-grade security and compliance to protect sensitive data at-rest and in-motion. This security covers data encryption on disk and SSL encryption between client and server communication
  - two deployment options:
    - _Single Server_
      - Built-in high availability with no additional cost (99.99 percent SLA)
      - Predictable performance and inclusive, pay-as-you-go pricing
      - Vertical scale as needed, within seconds
      - Monitoring and alerting to assess your server
      - Automatic backups and point-in-time-restore for up to 35 days
      - Ability to protect sensitive data at-rest and in-motion
      - capabilities require almost no administration, and all are provided at no additional cost
      - The Single Server deployment option offers three pricing tiers: Basic, General Purpose, and Memory Optimized
    - _Hyperscale (Citus)_
      - horizontally scales queries across multiple machines by using sharding
      - query engine parallelizes incoming SQL queries across these servers for faster responses on large datasets
      - serves applications that require greater scale and performance, generally workloads that are approaching, or already exceed, 100 GB of data
      - supports multi-tenant applications, real-time operational analytics, and high throughput transactional workloads
- **Azure SQL Managed Instance**
  - scalable cloud data service that provides the broadest SQL Server database engine compatibility with all the benefits of a fully managed platform as a service
  - Azure SQL Database and Azure SQL Managed Instance offer many of the same features
  - however, Azure SQL Managed Instance provides several options that might not be available to Azure SQL Database
  - if databases use Cyrillic characters for collation, migrate their databases to an Azure SQL Managed Instance, since Azure SQL Database only uses the default SQL_Latin1_General_CP1_CI_AS server collation.
  - _Migration_
    - assess which on-premises SQL Server instances you can migrate to Azure SQL Managed Instance to see if you have any blocking issue
    - Once you have resolved any issues, you can migrate your data, then cutover from your on-premises SQL Server to your Azure SQL Managed Instance by changing the connection string in your applications
- **Big Data and Analytics**
  - _Azure Synapse Analytics (formerly Azure SQL Data Warehouse)_
    - limitless analytics service that brings together enterprise data warehousing and big data analytics
    - query data on your terms by using either serverless or provisioned resources at scale
    - unified experience to ingest, prepare, manage, and serve data for immediate business intelligence and machine learning needs
  - _Azure HDInsight_
    - cloud service that makes it easier, faster, and more cost-effective to process massive amounts of dat
    - run popular open-source frameworks and create cluster types such as Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services
    - supports a broad range of scenarios such as extraction, transformation, and loading (ETL), data warehousing, machine learning, and IoT
  - _Azure Databricks_
    - unlock insights from all your data and build artificial intelligence solutions
    - set up your Apache Spark environment in minutes, and then autoscale and collaborate on shared projects in an interactive workspace
    - supports Python, Scala, R, Java, and SQL, as well as data science frameworks and libraries including TensorFlow, PyTorch, and scikit-learn
  - _Azure Data Lake Analytics_
    - on-demand analytics job service that simplifies big data
    - instead of deploying, configuring, and tuning hardware, you write queries to transform your data and extract valuable insights
    - analytics service can handle jobs of any scale instantly by setting the dial for how much power you need

## Azure Compute Services

- **Virtual Machines**
  - software emulations of physical computers
  - include a virtual processor, memory, storage, and networking resources
  - host an operating system, and you can install and run software just like a physical computer.
  - using a remote desktop client, you can use and control the VM as if you were sitting in front of it
  - provides infrastructure as a service (IaaS) and can be used in different ways
  - When you need total control over an operating system and environment, VMs are an ideal choice
  - you can customize all the software running on the VM
- **Virtual machine scale sets**
  - compute resource that you can use to deploy and manage a set of identical VMs
  - With all VMs configured the same, virtual machine scale sets are designed to support true autoscale
  - this makes it easier to build large-scale services targeting big compute, big data, and containerized workloads
  - As demand goes up, more VM instances can be added. As demand goes down, VM instances can be removed
  - process can be manual, automated, or a combination of both
- **Containers and Kubernetes**
  - compute resources that you can use to deploy and manage containers
  - Containers are lightweight, virtualized application environments. They're designed to be quickly created, scaled out, and stopped dynamically
  - can run multiple instances of a containerized application on a single host machine
- **App Service**
  - quickly build, deploy, and scale enterprise-grade web, mobile, and API apps running on any platform
  - meet rigorous performance, scalability, security, and compliance requirements while using a fully managed platform to perform infrastructure maintenance
  - App Service is a platform as a service (PaaS) offering
- **Azure Functions**
  - ideal when you're concerned only about the code running your service and not the underlying platform or infrastructure
  - commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less

### When to use Azure Virtual Machines

1. During testing and development

   - VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them

2. When running applications in the cloud

   - ability to run certain applications in the public cloud as opposed to creating a traditional infrastructure to run them can provide substantial economic benefits
   - Shutting down VMs when you don't need them or quickly starting them up to meet a sudden increase in demand means you pay only for the resources you use

3. When extending your datacenter to the cloud

   - organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network
   - Applications like SharePoint can then run on an Azure VM instead of running locally
     - This arrangement makes it easier or less expensive to deploy than in an on-premises environment

4. During disaster recovery

   - As with running certain types of applications in the cloud and extending an on-premises network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery
   - If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again

- **Move to the cloud with VMs**
  - VMs are also an excellent choice when you move from a physical server to the cloud (also known as lift and shift)
  - You can create an image of the physical server and host it within a VM with little or no changes
  - Just like a physical on-premises server, you must maintain the VM. You update the installed OS and the software it runs
- **Scale VMs in Azure**
  - you can group VMs together to provide high availability, scalability, and redundancy
  - No matter what your uptime requirements are, Azure has several features that can meet them
    1. Virtual machine scale sets
    2. Azure Batch
- **Virtual machine scale sets**
  - let you create and manage a group of identical, load-balanced VMs.
  - allow you to centrally manage, configure, and update a large number of VMs in minutes to provide highly available applications
  - number of VM instances can automatically increase or decrease in response to demand or a defined schedule
  - build large-scale services for areas such as compute, big data, and container workloads
- **Azure Batch**
  - enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs
  - When you're ready to run a job, Batch does the following
    1. Starts a pool of compute VMs for you
    2. Installs applications and staging data
    3. Runs jobs with as many tasks as you have
    4. Identifies failures
    5. Requeues work
    6. Scales down the pool as work completes

### When to use Azure App Service

- enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure
- offers automatic scaling and high availability
- supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model
- platform as a service (PaaS) environment allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications
- **App Service Costs**
  - pay for the Azure compute resources your app uses while it processes requests based on the App Service plan you choose
  - App Service plan determines how much hardware is devoted to your host
  - plan determines whether it's dedicated or shared hardware and how much memory is reserved for it
  - There's a free tier you can use to host small, low-traffic sites
- **Types of App Service**
  - host most common app service styles like
    1. Web apps
    - full support for hosting web apps by using ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python
    - choose either Windows or Linux as the host operating system
    2. API apps
    - like hosting a website, you can build REST-based web APIs by using your choice of language and framework
    - get full Swagger support and the ability to package and publish your API in Azure Marketplace
    - produced apps can be consumed from any HTTP- or HTTPS-based clien
    3. WebJobs
    - use the WebJobs feature to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app
    - can be scheduled or run by a trigger
    - often used to run background tasks as part of your application logic
    4. Mobile apps
    - quickly build a back end for iOS and Android apps
    - Store mobile app data in a cloud-based SQL database
    - Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook
    - Send push notifications
    - Execute custom back-end logic in C# or Node.js
    - On the mobile app side, there's SDK support for native iOS and Android, Xamarin, and React native apps
  - handles most of the infrastructure decisions you deal with in hosting web-accessible apps
    - Deployment and management are integrated into the platform
    - Endpoints can be secured
    - Sites can be scaled quickly to handle high traffic loads
    - The built-in load balancing and traffic manager provide high availability
  - flexibility makes App Service the ideal choice to host web-oriented applications

### When to use Azure Container Instances or Azure Kubernetes Service

- If you want to run multiple instances of an application on a single host machine, containers are an excellent choice
- **What are containers?**
  - a virtualization environment
  - like running multiple virtual machines on a single physical host, you can run multiple containers on a single physical or virtual host
  - unlike virtual machines, you don't manage the operating system for a container
  - Virtual machines appear to be an instance of an operating system that you can connect to and manage, but containers are lightweight and designed to be created, scaled out, and stopped dynamically
  - containers are designed to allow you to respond to changes on demand
  - you can quickly restart in case of a crash or hardware interruption
- **Manage containers**
  - _Azure Container Instances_
    - the fastest and simplest way to run a container in Azure without having to manage any virtual machines or adopt any additional services
    - platform as a service (PaaS) offering that allows you to upload your containers, which it runs for you.
  - _Azure Kubernetes Service_
    - a complete orchestration service for containers with distributed architectures and large volumes of containers.
    - task of automating, managing, and interacting with a large number of containers is known as orchestration
- **Use containers in your solutions**
  - often used to create solutions by using a microservice architecture
    - where you break solutions into smaller, independent pieces
    - I.E. you might split a website into a container hosting your front end, another hosting your back end, and a third for storage
    - allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently
  - Imagine your website back-end has reached capacity but the front end and storage aren't being stressed. You could:
    - Scale the back end separately to improve performance
    - Decide to use a different storage service
    - Replace the storage container without affecting the rest of the application

### Serverless Computing(Azure Functions/ Azure Logic Apps)

- Serverless computing is the abstraction of servers, infrastructure, and operating systems
  - Azure takes care of managing the server infrastructure and the allocation and deallocation of resources based on demand
- Azure has two implementations of serverless compute:
  1. Azure Functions: Functions can execute code in almost any modern language
  2. Azure Logic Apps: Logic apps are designed in a web-based designer and can execute logic triggered by Azure services without writing any code
- Infrastructure isn't your responsibility. Scaling and performance are handled automatically
- Serverless computing includes the abstraction of servers, an event-driven scale, and micro-billing
  - **Abstraction of servers**
    1. Serverless computing abstracts the servers you run on
    2. You never explicitly reserve server instances. The platform manages that for you
    3. Each function execution can run on a different compute instance. This execution context is transparent to the code
    4. you deploy your code, which then runs with high availability
  - **Event-driven scale**: Serverless computing is an excellent fit for workloads that respond to incoming events. Events include triggers by
    1. Timers, for example, if a function needs to run every day at 10:00 AM UTC
    2. HTTP, for example, API and webhook scenarios
    3. Queues, for example, with order processing
    4. Instead of writing an entire application, the developer authors a function, which contains both code and metadata about its triggers and bindings
    5. The platform automatically schedules the function to run and scales the number of compute instances based on the rate of incoming events
    6. Triggers define how a function is invoked
    7. Bindings provide a declarative way to connect to services from within the code
  - **Micro-billing**
    1. Traditional computing bills for a block of time like paying a monthly or annual rate for website hosting
    2. With serverless computing, they pay only for the time their code runs
    3. If no active function executions occur, they're not charged.

### When to use Azure Functions

- When you're concerned only about the code running your service, and not the underlying platform or infrastructure, using Azure Functions is ideal
- Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less
- Functions scale automatically based on demand, so they're a solid choice when demand is variable
- Functions can be either stateless or stateful
  - stateless (the default): they behave as if they're restarted every time they respond to an event
  - stateful (called Durable Functions): a context is passed through the function to track prior activity
- Functions are a key component of serverless computing. They're also a general compute platform for running any type of code
- This flexibility allows you to manage scaling, run on virtual networks, and even completely isolate the functions

### When to use Azure Logic Apps

- Logic apps are similar to functions. Both enable you to trigger logic based on an event
- logic apps execute workflows that are designed to automate business scenarios and are built from predefined logic blocks instead of code
- Azure logic app workflow starts with a trigger, which fires when a specific event happens or when newly available data meets specific criteria
- Many triggers include basic scheduling capabilities, so developers can specify how regularly their workloads will run
- Each time the trigger fires, the Logic Apps engine creates a logic app instance that runs the actions in the workflow
  - actions can also include data conversions and flow controls, such as conditional statements, switch statements, loops, and branching
- You create logic app workflows by using a visual designer on the Azure portal or in Visual Studio. The workflows are persisted as a JSON file with a known workflow schema
- Azure provides more than 200 different connectors and processing blocks to interact with different services
  - These resources include the most popular enterprise apps. You can also build custom connectors and workflow steps if the service you need to interact with isn't covered
  - You then use the visual designer to link connectors and blocks together. You pass data through the workflow to do custom processing, often all without writing any code
- ideal for a business analyst role

### Differences between Functions and Logic Apps

[comment]: <> (prettier-ignore)
| Property | Functions | Logic Apps |
|---|---|---|
| State | Normally stateless, but Durable Functions provide state. | Stateful |
| Development | Code first(imperative) | Designer-first(declarative) |
| Connectivity | About a dozen built-in binding types. Write code for custom bindings | Large collection of connectors. Enterprise Integration Pack for B2B scenarios. Build custom connectors |
| Actions | Each activity is an Azure function. Write code for activity functions | Large collection of ready-made actions |
| Monitoring | Azure Application Insights | Azure portal, Log Analytics |
| Management | REST API, PowerShell, Visual Studio | Azure portal, REST API, PowerShell, Visual Studio |
| Execution Context | Can run locally or in the cloud | Runs only in the cloud |

### Azure Virtual Desktop

- Azure Virtual Desktop is a desktop and application virtualization service that runs on the cloud
- enables your users to use a cloud-hosted version of Windows from any location
- works across devices like Windows, Mac, iOS, Android, and Linux

### When to use Azure Virtual Desktop

- Good user experience
  - You can make sure your session host virtual machines (VMs) run near apps and services that connect to your datacenter or the cloud. This way your users stay productive and don't encounter long load times
  - Users have the freedom to connect to Azure Virtual Desktop with any device over the internet. They use a Azure Virtual Desktop client to connect to their published Windows desktop and applications
  - You can provide individual ownership through personal (persistent) desktops. Then they can add or remove programs without impacting other users on that remote desktop
- Enhance Security
  - Azure Virtual Desktop provides centralized security management for users' desktops with Azure Active Directory (Azure AD). You can enable multifactor authentication to secure user sign-ins. You can also secure access to data by assigning granular role-based access controls (RBACs) to users
  - With Azure Virtual Desktop, the data and apps are separated from the local hardware. Azure Virtual Desktop runs them instead on a remote server. The risk of confidential data being left on a personal device is reduced
  - User sessions are isolated in both single and multi-session environments
  - Azure Virtual Desktop also improves security by using reverse connect technology. This connection type is more secure than the Remote Desktop Protocol

### Key features of Azure Virtual Desktop

- **Simplified management**
  - use Azure AD and RBACs to manage access to resources
  - you also get tools to automate VM deployments, manage VM updates, and provide disaster recovery
  - Azure Virtual Desktop uses Azure Monitor for monitoring and alerts. This standardization lets admins identify issues through a single interface
- **Performance management**
  - gives you options to load balance users on your VM host pools
  - Host pools are collections of VMs with the same configuration assigned to multiple users
  - For the best performance, you can configure load balancing to occur as users sign in (breadth mode)
  - With breadth mode, users are sequentially allocated across the host pool for your workload
  - to save costs, you can configure your VMs for depth mode load balancing where users are fully allocated on one VM before moving to the next
- **Multi-session Windows 10 deployment**
  - Azure Virtual Desktop lets you use Windows 10 Enterprise multi-session, the only Windows client-based operating system that enables multiple concurrent users on a single VM
  - provides a more consistent experience with broader application support compared to Windows Server-based operating systems

### How to reduce costs with Azure Virtual Desktop

- available to you at no additional cost if you have an eligible Microsoft 365 license. Just pay for the Azure resources used by Azure Virtual Desktop
- Bring your eligible Windows or Microsoft 365 license to get Windows 10 Enterprise and Windows 7 Enterprise desktops and apps at no additional cost
- If you're an eligible Microsoft Remote Desktop Services Client Access License customer, Windows Server Remote Desktop Services desktops and apps are available at no additional cost
- Save on compute costs
  - Buy one-year or three-year Azure Reserved Virtual Machine Instances to save you up to 72 percent versus pay-as-you-go pricing
  - You can pay for a reservation up front or monthly. Reservations provide a billing discount and don't affect the runtime state of your resources
