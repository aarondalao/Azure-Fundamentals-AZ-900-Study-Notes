Managing hybrid and multi-cloud environments can rapidly get complicated. Azure provides a host of tools to provision, configure, and monitor Azure resources. What about the on-premises resources in a hybrid configuration or the cloud resources in a multi-cloud configuration?

### Azure Arc
- In utilizing Azure Resource Manager (ARM), Arc lets you <mark>extend your Azure compliance and monitoring to your hybrid and multi-cloud configurations. </mark>
- Azure Arc **simplifies governance and management** by delivering a consistent multi-cloud and on-premises management platform.
- Azure Arc provides a centralized, unified way to:
	- <mark>Manage your entire environment together</mark> by projecting your existing non-Azure resources into ARM.
	- <mark>Manage <b>multi-cloud</b> and <b>hybrid virtual machines, Kubernetes clusters, and databases</b> as if they are running in Azure.</mark>
	- Use familiar Azure services and management capabilities, regardless of where they live.
	- Continue using traditional ITOps while introducing DevOps practices to support new cloud and native patterns in your environment.
	- Configure custom locations as an abstraction layer on top of Azure Arc-enabled Kubernetes clusters and cluster extensions.

## What can Azure Arc do outside of Azure?

Currently, Azure Arc allows you to manage the following resource types hosted outside of Azure:
- Servers
- Kubernetes clusters
- Azure data services
- SQL Server
- Virtual machines (preview)

---
## Tags:
#module10 

---
[Previous](Describe-tools-for-interacting-with-Azure) | [Next](Describe-Azure-Resource-Manager-and-Azure-ARM-templates.md)
