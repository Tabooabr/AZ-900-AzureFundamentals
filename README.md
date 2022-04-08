# AzureFundamentals
Readme with Important notes about azure
---

- [AzureFundamentals](#azurefundamentals)
  - [Readme with Important notes about azure](#readme-with-important-notes-about-azure)
- [What is Azure?](#what-is-azure)
    - [How does it work?](#how-does-it-work)
  - [What is the Azure portal?](#what-is-the-azure-portal)
  - [Azure services](#azure-services)
  - [Azure accounts:](#azure-accounts)
- [Azure fundamental concepts](#azure-fundamental-concepts)
  - [What are public, private, and hybrid clouds?](#what-are-public-private-and-hybrid-clouds)
  - [Cloud model comparison](#cloud-model-comparison)
  - [What are Cloud Service models?](#what-are-cloud-service-models)
  - [Azure Resources and Manager](#azure-resources-and-manager)
    - [Azure resource groups](#azure-resource-groups)
    - [Logical grouping](#logical-grouping)
  - [Billing and subscriptions](#billing-and-subscriptions)
- [Azure Compute Services](#azure-compute-services)
    - [VMs](#vms)
      - [Examples of when to use VMs](#examples-of-when-to-use-vms)
      - [Move to the cloud with VMs](#move-to-the-cloud-with-vms)
      - [Scale VMs in Azure](#scale-vms-in-azure)
      - [What are virtual machine scale sets?](#what-are-virtual-machine-scale-sets)
      - [What is Azure Batch?](#what-is-azure-batch)
  - [Decide when to use azure app service](#decide-when-to-use-azure-app-service)
    - [Costs](#costs)
    - [Types of app services](#types-of-app-services)
  - [Decide when to use Azure Container instances or Azure Kubernetes service](#decide-when-to-use-azure-container-instances-or-azure-kubernetes-service)
    - [Manage containers](#manage-containers)
  - [When to use Azure Functions](#when-to-use-azure-functions)
    - [What is serverless computing?](#what-is-serverless-computing)
    - [Azure functions:](#azure-functions)
    - [Azure logic apps](#azure-logic-apps)
  - [When to use Azure Virtual Desktop](#when-to-use-azure-virtual-desktop)
    - [What is it?](#what-is-it)
    - [Why?](#why)
  - [Summary:](#summary)
  - [Networking Services](#networking-services)

# What is Azure?

Azure is microsoft Cloud computing platform.

Azure supports platform softare and infrastructure as service.

- Azure container and Kubernetes is a thing.

- Be ready for the future: Continuous innovation from Microsoft supports your development today and your product visions for tomorrow.

- Build on your terms: You have choices. With a commitment to open source, and support for all languages and frameworks, you can build how you want and deploy where you want to.

- Operate hybrid seamlessly: On-premises, in the cloud, and at the edge--we'll meet you where you are. Integrate and manage your environments with tools and services designed for a hybrid cloud solution.

- Trust your cloud: Get security from the ground up, backed by a team of experts, and proactive compliance trusted by enterprises, governments, and startups.

### How does it work?

It uses virtualization to decouple OS from hardware, through a Hypervisor.

- it emulates an os inside the VM and tightens the components toghether. can run multiple VMs in it. each server in a data center has a hypervisor.

## What is the Azure portal?
The Azure portal is a web-based, unified console that provides an alternative to command-line tools. With the Azure portal, you can manage your Azure subscription by using a graphical user interface. You can:

Build, manage, and monitor everything from simple web apps to complex cloud deployments.
Create custom dashboards for an organized view of resources.
Configure accessibility options for an optimal experience.

---

## Azure services

most commonly used services:

Let's take a closer look at the most commonly used categories:

- Compute
- Networking
- Storage
- Mobile
- Databases
- Web
- Internet of Things (IoT)
- Big data
- AI
- DevOps

further info: https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/tour-of-azure-services

## Azure accounts: 

![scope-levels-12669ee1](https://user-images.githubusercontent.com/34945430/162189279-3713484c-7c16-4a66-aae3-4defff7c6132.png)


---

# Azure fundamental concepts

## What are public, private, and hybrid clouds?

There are three deployment models for cloud computing: public cloud, private cloud, and hybrid cloud. Each deployment model has different aspects that you should consider as you migrate to the cloud.

| Deployment model  |         Description |
|-------------------|---------------|
|Public cloud       |Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.|
|Private cloud       | A private cloud consists of computing resources used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site (on-premises) datacenter, or it can be hosted by a third-party service provider. |
|Hybrid cloud|A hybrid cloud is a computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them. |

## Cloud model comparison

- Public cloud:
  
  - No capital expenditures to scale up.
  - Applications can be quickly provisioned and deprovisioned.
  - Organizations pay only for what they use.

- Private cloud:
  
  - Hardware must be purchased for start-up and maintenance.
  - Organizations have complete control over resources and security.
  - Organizations are responsible for hardware maintenance and updates.
- Hybrid cloud:
  
  - Provides the most flexibility.
  - Organizations determine where to run their applications.
  - Organizations control security, compliance, or legal      requirements.

## What are Cloud Service models?

see here: https://docs.microsoft.com/en-gb/learn/modules/fundamental-azure-concepts/categories-of-cloud-services


## Azure Resources and Manager

### Azure resource groups

Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for resources deployed on Azure. These resources are anything you create in an Azure subscription like VMs, Azure Application Gateway instances, and Azure Cosmos DB instances. All resources must be in a resource group, and a resource can only be a member of a single resource group. Many resources can be moved between resource groups with some services having specific limitations or requirements to move. Resource groups can't be nested. Before any resource can be provisioned, you need a resource group for it to be placed in.

### Logical grouping

Resource groups exist to help manage and organize your Azure resources. By placing resources of similar usage, type, or location in a resource group, you can provide order and organization to resources you create in Azure. Logical grouping is the aspect that you're most interested in here, because there's a lot of disorder among our resources.

https://docs.microsoft.com/en-gb/learn/modules/azure-architecture-fundamentals/resources-resource-manager


## Billing and subscriptions

https://docs.microsoft.com/en-gb/learn/modules/azure-architecture-fundamentals/management-groups-subscriptions

I think on subs the documentation explains it very well and cannot be summarized, so refer to the original docmentation.

---

# Azure Compute Services

- Azure Virtual Machines
- Azure Container Instances
- Azure App Service
- Azure Functions (or serverless computing)

You have:

- Virtual machine scale sets
- Containers and kubernetes
- app services
- functions

### VMs

#### Examples of when to use VMs
- During testing and development. VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them.

- When running applications in the cloud. The ability to run certain applications in the public cloud as opposed to creating a traditional infrastructure to run them can provide substantial economic benefits. For example, an application might need to handle fluctuations in demand. Shutting down VMs when you don't need them or quickly starting them up to meet a sudden increase in demand means you pay only for the resources you use.
- When extending your datacenter to the cloud. An organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network. Applications like SharePoint can then run on an Azure VM instead of running locally. This arrangement makes it easier or less expensive to deploy than in an on-premises environment.
- During disaster recovery. As with running certain types of applications in the cloud and extending an on-premises network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery. If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again.

#### Move to the cloud with VMs

VMs are also an excellent choice when you move from a physical server to the cloud (also known as lift and shift). You can create an image of the physical server and host it within a VM with little or no changes. Just like a physical on-premises server, you must maintain the VM. You update the installed OS and the software it runs.

#### Scale VMs in Azure

You can run single VMs for testing, development, or minor tasks. Or you can group VMs together to provide high availability, scalability, and redundancy. No matter what your uptime requirements are, Azure has several features that can meet them. These features include:

- Virtual machine scale sets
- Azure Batch

#### What are virtual machine scale sets?

Virtual machine scale sets let you create and manage a group of identical, load-balanced VMs.

#### What is Azure Batch?

Azure Batch enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs.

When you're ready to run a job, Batch does the following:

- Starts a pool of compute VMs for you.
- Installs applications and staging data.
- Runs jobs with as many tasks as you have.
- Identifies failures.
- Requeues work.
- Scales down the pool as work completes.

## Decide when to use azure app service

App Service enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure. It offers automatic scaling and high availability.

App Service supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.

### Costs

The App Service plan determines how much hardware is devoted to your host. For example, the plan determines whether it's dedicated or shared hardware and how much memory is reserved for it. 

### Types of app services

With App Service, you can host most common app service styles like:

- Web apps
- API apps
- WebJobs
- Mobile apps

App Service handles most of the infrastructure decisions you deal with in hosting web-accessible apps:

- Deployment and management are integrated into the platform.
- Endpoints can be secured.
- Sites can be scaled quickly to handle high traffic loads.
- The built-in load balancing and traffic manager provide high availability.

See more: https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-app-services

## Decide when to use Azure Container instances or Azure Kubernetes service

### Manage containers

Containers are managed through a container orchestrator, which can start, stop, and scale out application instances as needed. There are two ways to manage both Docker and Microsoft-based containers in Azure: Azure Container Instances and Azure Kubernetes Service (AKS).

- Azure container instances
- Azure Kubernetes Service

Use contanerisation to split your app in multiple containers that can be accessed and managed separately, for example front end back end and data (3 containers).

See further: https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-container-services

MICROSERVICES!!!

## When to use Azure Functions

Serverless computing includes the abstraction of servers, an event-driven scale, and micro-billing:

- Abstraction of servers: Serverless computing abstracts the servers you run on. You never explicitly reserve server instances. The platform manages that for you. Each function execution can run on a different compute instance. This execution context is transparent to the code. With serverless architecture, you deploy your code, which then runs with high availability.

- Event-driven scale: Serverless computing is an excellent fit for workloads that respond to incoming events. Events include triggers by:

  - Timers, for example, if a function needs to run every day at 10:00 AM UTC.
  - HTTP, for example, API and webhook scenarios.
  -  Queues, for example, with order processing.
  - And much more.

Instead of writing an entire application, the developer authors a function, which contains both code and metadata about its triggers and bindings. The platform automatically schedules the function to run and scales the number of compute instances based on the rate of incoming events. Triggers define how a function is invoked. Bindings provide a declarative way to connect to services from within the code.

- Micro-billing: Traditional computing bills for a block of time like paying a monthly or annual rate for website hosting. This method of billing is convenient but isn't always cost effective. Even if a customer's website gets only one hit a day, they still pay for a full day's worth of availability. With serverless computing, they pay only for the time their code runs. If no active function executions occur, they're not charged. For example, if the code runs once a day for two minutes, they're charged for one execution and two minutes of computing time.

### What is serverless computing?

The goal is to take care of management tasks and automate them.

Azure has two implementations of serverless compute:

- Azure Functions: Functions can execute code in almost any modern language.
- Azure Logic Apps: Logic apps are designed in a web-based designer and can execute logic triggered by Azure services without writing any code.

Benefits:

- No infrastructure management
- Scalability
- Pay as you use

### Azure functions:

When you're concerned only about the code running your service, and not the underlying platform or infrastructure, using Azure Functions is ideal. Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less

### Azure logic apps

Logic apps are similar to functions. Both enable you to trigger logic based on an event. Where functions execute code, logic apps execute workflows that are designed to automate business scenarios and are built from predefined logic blocks.

Every Azure logic app workflow starts with a trigger, which fires when a specific event happens or when newly available data meets specific criteria. Many triggers include basic scheduling capabilities, so developers can specify how regularly their workloads will run. Each time the trigger fires, the Logic Apps engine creates a logic app instance that runs the actions in the workflow. These actions can also include data conversions and flow controls, such as conditional statements, switch statements, loops, and branching.

You create logic app workflows by using a visual designer on the Azure portal or in Visual Studio. The workflows are persisted as a JSON file with a known workflow schema.

see more: 
https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-functions

## When to use Azure Virtual Desktop

### What is it?

Azure Virtual Desktop is a desktop and application virtualization service that runs on the cloud. It enables your users to use a cloud-hosted version of Windows from any location. Azure Virtual Desktop works across devices like Windows, Mac, iOS, Android, and Linux. It works with apps that you can use to access remote desktops and apps. You can also use most modern browsers to access Azure Virtual Desktop-hosted experiences.

### Why? 

- Provide the best user experience
- Enhance security
- Simplified management
- Performance management
- Multi session W10 deployment

## Summary: 

In this module, you learned how you can help Tailwind Traders resolve its application demand challenges through the use of Azure virtualization services like Azure Virtual Machines, Azure Container Instances, and Azure Kubernetes Service. You also learned how you can use:

- Azure App Service to create your website front-ends.

- Azure Functions to create event-driven application logic that only runs when you need it.

- Azure Virtual Desktop to quickly provide a customized operating system and software environment for your remote workers.

Further reading: 
https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/summary

---

## Networking Services

- Virtual networks
- Service endpoints

On prem: 

- Points to site vrtual private networks
- Site to site VPN
- Azure ExpressRoute

Route network traffic:

- Route table
- Border Gateway Protocol

Filter traffic: 

- Network Security Groupd
- Network virtual appliance

Connect virtual networks:

You can link virtual networks together by using virtual network peering. Peering enables resources in each virtual network to communicate with each other. These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.

User-defined routes (UDR) are a significant update to Azure’s Virtual Networks that allows for greater control over network traffic flow. This method allows network administrators to control the routing tables between subnets within a VNet, as well as between VNets.

![image](https://user-images.githubusercontent.com/34945430/162455203-035f1973-f0ee-4612-bc22-21fcea3a4708.png)


## Azure VPN fundamentals

VPNs use an encrypted tunnel within another network. They're typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet). Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks.

### Vpn gateways
A VPN gateway is a type of virtual network gateway. Azure VPN Gateway instances are deployed in a dedicated subnet of the virtual network and enable the following connectivity:

- Connect on-premises datacenters to virtual networks through a site-to-site connection.
- Connect individual devices to virtual networks through a point-to-site connection.
- Connect virtual networks to other virtual networks through a network-to-network connection.

Types: 

- Policy based VPN
- Route-Based VPN

![image](https://user-images.githubusercontent.com/34945430/162458555-728cc79f-823e-497c-8910-1c39d8c7cd39.png)

## VPN gateway sizes:

![image](https://user-images.githubusercontent.com/34945430/162458680-e0844098-f867-409b-831e-21ed19894087.png)

## Deploying the VPN:

![image](https://user-images.githubusercontent.com/34945430/162458809-5a0fd227-7e16-435b-b8b9-e174fc92af01.png)

See more about VPNS here:

https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/azure-vpn-gateway-fundamentals

## Azure Express Fundamentals:

![image](https://user-images.githubusercontent.com/34945430/162459508-54cc2fdb-2e91-4e86-bd14-344b24a74441.png)

### Features and benefits of ExpressRoute
There are several benefits to using ExpressRoute as the connection service between Azure and on-premises networks.

- Layer 3 connectivity between your on-premises network and the Microsoft Cloud through a connectivity provider. Connectivity can be from an any-to-any (IPVPN) network, a point-to-point Ethernet connection, or through a virtual cross-connection via an Ethernet exchange.
- Connectivity to Microsoft cloud services across all regions in the geopolitical region.
- Global connectivity to Microsoft services across all regions with the ExpressRoute premium add-on.
- Dynamic routing between your network and Microsoft via BGP.
- Built-in redundancy in every peering location for higher reliability.
- Connection uptime SLA.
- QoS support for Skype for Business.

https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/express-route-fundamentals

---
