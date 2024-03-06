In this module, you'll be introduced to general cloud concepts. You'll start with an introduction to cloud in general. Then you'll dive into concepts like shared responsibility, different cloud models, and explore the unique pricing method for the cloud.

## Learning Objectives
after completing this module, you'll be able to:
 - Define cloud computing
 - Describe the shared responsibility model
 - Define cloud models, including public, private, and hybrid
 - Describe the consumption-based model
 - Compare cloud pricing models

--- 
## What is Cloud computing

- it is the delivery of computing services over the internet. 
	- Computing services include common IT infrastructure such as virtual machines, databases, and networking. 
	- Cloud Services also expand the traditional IT offerings to include things like Internet of Things (IoT), Machine Learning (ML), and Artificial Intelligence (AI).
- It is not constrained by a physical infrastructure the same way that a traditional datacenter is. 
	- That means if you need to increase your IT infrastructure rapidly, you don't have to wait to build a new datacenter, - you can use the cloud to rapidly expand your IT footprint.
	
---
## Describe the [Shared Responsibility Model](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)
❗❗❗***Note:***   ==very important concept, especially to security-type services | Cloud Provider Agnostic == 

> **Scenario:** 
	Start with a traditional corporate datacenter. The company is responsible for maintaining the physical space, ensuring security, and maintaining or replacing the servers if anything happens. The IT department is responsible for maintaining all the infrastructure and software needed to keep the datacenter up and running. They’re also likely to be responsible for keeping all systems patched and on the correct version.

With the [**Shared Responsibility Model**](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility), these responsibilities get shared between the ***cloud provider*** and the ***consumer***.

The Following Table highlights how the Shared Responsibility Model informs who is responsible for what, depending on the cloud service type:

> ***Note:***
> x = Microsoft
> xx = Customer
> xxx = Shared

|                                                | Responsibility                        | SaaS | PaaS | IaaS | On Prem |
| ---------------------------------------------- | ------------------------------------- | ---- | ---- | ---- | ------- |
| Responsibility always retained by the customer | information and data                  | xx   | xx   | xx   | xx      |
|                                                | Devices (Mobile and PCs)              | xx   | xx   | xx   | xx      |
|                                                | Accounts and Identities               | xx   | xx   | xx   | xx      |
| Responsibilities varies by type                | Identity and directory Infrastructure | xxx  | xxx  | xx   | xx      |
|                                                | Applications                          | x    | xxx  | xx   | xx      |
|                                                | Network Controls                      | x    | xxx  | xx   | xx      |
|                                                | Operating System                      | x    | x    | xx   | xx      |
| Responsibility transfers to cloud providers    | Physical hosts                        | x    | x    | x    | xx      |
|                                                | Physical networks                     | X    | x    | x    | xx      |
|                                                | Physical datacenters                  | x    | x    | x    | xx      |
**You**, as a **customer**, is always responsible for:
- The information and data stored in the cloud
- Devices that are allowed to connect to your cloud (cell phones, computers, etc.)
- The accounts and identities of the people, services, and devices, within your organization.

The **Cloud Provider** is always responsible for:
- The physical datacenter
- the physical network
- the physical hosts

Your service model with determine responsibility for things like:
- Operating Systems
- Networking Controls
- Applications
- Identity and infrastructure
---
## Define cloud models
- This defines the deployment type of cloud resources. There are three main cloud models:
### Private Cloud
- A private cloud is, in some ways, the natural evolution from a corporate datacenter.
- it is a cloud (delivering IT services over the internet) that's used by a single entity.
- provides much greater control for the company and its IT department.
- Greater cost and fewer benefits of a public cloud deployment
- may hosted from your on site datacenter, may also be ho9sted in a dedicated datacenter offsite, potentially even by a third party that has dedicated that datacenter to your company.
### Public Cloud
- Built, controlled, and maintained by a third-party cloud provider.
- anyone that wants to purchase cloud services can access and use resources.
- The general public availability is a key difference between public and private cloud

### Hybrid Cloud
- a computing environment that uses both public and private clouds in an inter-connected environment. 
- can be used to allow a private cloud to surge for increased, temporary demand by deploying public cloud resources. 
- can be used to provide an extra layer of security

The following table highlights a few key comparative aspects between the cloud models:

| **Public cloud**                                                      | **Private cloud**                                                  | **Hybrid cloud**                                                  |
| --------------------------------------------------------------------- | ------------------------------------------------------------------ | ----------------------------------------------------------------- |
| No capital expenditures to scale up                                   | Organizations have complete control over resources and security    | Provides the most flexibility                                     |
| Applications can be quickly provisioned and deprovisioned             | Data is not collocated with other organizations’ data              | Organizations determine where to run their applications           |
| Organizations pay only for what they use                              | Hardware must be purchased for startup and maintenance             | Organizations control security, compliance, or legal requirements |
| Organizations don’t have complete control over resources and security | Organizations are responsible for hardware maintenance and updates |                                                                   |
### Optional: Multi-Cloud
- an increasingly likely scenario
- you use multiple public cloud providers
- or maybe you use different features from different cloud providers
- or maybe you star4ted your cloud journey with on provider and are in the process of migrating to a different provider.
- regardless, in a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments.

### [Azure Arc ](https://azure.microsoft.com/en-au/products/azure-arc#:~:text=Azure%20Arc%20is%20a%20bridge,%2C%20operations%2C%20and%20security%20model.)
- it is a set of technologies that helps manage your cloud environment.
- can help manage your cloud environment, whenever it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid config, or even a multi-cloud environment running on multiple cloud providers at once.

### [Azure VMWare Solution](https://azure.microsoft.com/en-au/products/azure-vmware#:~:text=Seamlessly%move%VMware-based%workloads%from,%that&runs%on%Azure%infrastructure.)
- What if you're already established with VMWare in a private cloud environment but want to migrate to a public or hybrid cloud? 
- Azure VMWare Solution lets you run your VMWare workloads in Azure with seamless integration and Scalability
---
## Describe the Consumption-Based Model

There are **two types of expenses** to consider when comparing IT Infrastructure Models:
- Capital Expenditure (CapEx)
	- A One-time, up-front expenditure to purchase or secure tangible resources.
	- A new building, repaving the parking lot, building a datacenter, or buying a company vehicle are examples of CapEx.
- Operational Expenditures (OpEx)
	- Spending money on services or products over time.
	- Renting a convention center, leasing a company vehicle, or signing up for cloud services.

Cloud computing falls under OpEx because cloud computing operates on a consumption-based model.
- You don't pay for the physical infrastructure and the underlying operational costs of owning a datacenter (Electricity, Security, Etc).
- Only pay for the IT resource you use. If you don't use any IT Resources this month, you don't pay for any IT resources.

Benefits of consumption-based model:
- No Upfront costs
- No need to purchase and manage costly infrastructure that users might not use to its fullest potential
- The ability to **pay** for some **more resources** when **they are needed**.
- The ability to **stop paying** for resources that are **no longer needed**.

With traditional Datacenters, you try to estimate the future resource needs
- If you overestimate, you spend more on your datacenter than you need to and potentially waste money.
- If you underestimate, your datacenter will quickly reach capacity and your applications and services may suffer from decreased performance.
- Fixing an under-provisioned datacenter can take a long time. You man need to order, receive, and install more hardware, or add more power, cooling, and networking for the extra hardware.

In a Cloud-based model, you don't have to working about getting the resources needs just right. 
- if you find that you need more virtual machines, you add more
- if the demand drops and you don't need as many virtual machines, you can remove it on the fly.
- either way, you're only paying for the VM's that you use, not the "extra capacity" that the cloud provider has on hand.
### Compare Cloud pricing models

- is the delivery of computing services over the internet by using a pay-as-you-go pricing model.
- You typically pay only for the cloud services you use, which helps you:
	- Plan and manage your operating costs
	- Run Infrastructure more efficiently
	- Scale as your business needs change
---
tags:
#module1
 
---

[Previous](Intro-to-Microsoft-Azure-Fundamentals.md) | [Next](Summary-Cloud-Concepts.md)
