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
