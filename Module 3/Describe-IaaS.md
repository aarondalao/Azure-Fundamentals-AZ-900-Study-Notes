## Infrastructure as a Service (IaaS)
- it is the most flexible category of cloud services
- it provides you the maximum amount of control for your cloud resources
- in a IaaS model, the cloud provider is responsible for maintaining the hardware, network connectivity (to the internet), and physical security.
- **You** are responsible for everything else: Operating System, installation, configuration, and maintenance; network configuration; database and storage configuration; and so on.
- With IaaS, you're essentially renting the hardware in the cloud datacenter. but what you do with that hardware is up to you.

## [Shared Responsibility Model](Introduction-to-Cloud-Computing#Describe-the-Shared-Responsibility-Model)

The Shared Responsibility model applies to all cloud service types. IaaS places the largest share of responsibility with you. The cloud provider is responsible for maintaining the physical infrastructure and its access to the internet. You are responsible for installation and configuration, patching and updates, and security.

![Shared Responsibility Model Table](https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-service-types/media/shared-responsibility-b3829bfe.svg)

## Scenarios

Some common scenarios where IaaS might make sense include:

- Lift-and-shift migration
	- You’re standing up cloud resources similar to your on-prem datacenter, and then simply moving the things running on-prem to running on the IaaS infrastructure.
- Testing and development
	- You have established configurations for development and test environments that you need to rapidly replicate. You can stand up or shut down the different environments rapidly with an IaaS structure, while maintaining complete control.

---
## Tags:
#module3

---
[Previous](Intro-Describe-Cloud-Service-Types.md) | [Next](Describe-PaaS.md)
