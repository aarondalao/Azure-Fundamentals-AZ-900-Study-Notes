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
tags:
#module1
 
---
[Previous](What-is-Cloud-Computing.md) | [Next](Define-Cloud-Models.md)
