## Platform as a Service (PaaS)
- is the middle ground between renting space in a datacenter (IaaS) and paying for a complete and deployed solution (SaaS).
- in a PaaS environment, the cloud provider maintains the physical infrastructure, physical security, and connection to the internet.
- They also maintain OS, middleware, development tools, and business intelligence service that make up a cloud solution
- In a PaaS scenario, you don't have to worry about the licensing or patching for OS and databases.
- PaaS is well suited to provide a **complete development environment** without the **headache of maintaining all the development infrastructure**.
## [Shared Responsibility Model](Introduction-to-Cloud-Computing#Describe-the-Shared-Responsibility-Model)

- The shared responsibility model applies to all the cloud service types. 
- PaaS splits the responsibility between you and the cloud provider. 
- The cloud provider is responsible for maintaining the physical infrastructure and its access to the internet, just like in IaaS. 
- In the PaaS model, the cloud provider will also maintain the operating systems, databases, and development tools. 
- Think of PaaS like using a domain joined machine: IT maintains the device with regular updates, patches, and refreshes.

Depending on the configuration, you or the cloud provider may be responsible for networking settings and connectivity within your cloud environment, network and application security, and the directory infrastructure.

![Shared Responsibility Model Table](https://learn.microsoft.com/en-us/training/wwl-azure/describe-cloud-service-types/media/shared-responsibility-b3829bfe.svg)

## Scenarios
Some common scenarios where PaaS might make sense include:

- Development framework
	- PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. 
	- Similar to the way you create an Excel macro, PaaS lets developers create applications using built-in software components.
	- Cloud features such as scalability, high-availability, and multi-tenant capability are included, reducing the amount of coding that developers must do.
- Analytics or business intelligence
	- Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions.

---
## Tags:
#module3

---
[Previous](Describe-IaaS) | [Next](Describe-SaaS.md)
