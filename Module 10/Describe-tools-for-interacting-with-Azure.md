To get the most out of Azure, you need a way to interact with the Azure environment, the management groups, subscriptions, resource groups, resources, and so on. Azure provides multiple tools for managing your environment, including the:
- **Azure portal**
- **Azure PowerShell**
- **Azure Command Line Interface (CLI)****

## What is the Azure portal?
- is a <mark>web-based, unified console that provides an alternative to command-line tools. </mark>
- With the Azure portal, you can manage your Azure subscription by using a graphical user interface. You can:
	- **Build, manage, and monitor everything** from simple web apps to complex cloud deployments
	- **Create custom dashboards** for an organized view of resources
	- **Configure accessibility options** for an optimal experience

- The Azure portal is designed for resiliency and continuous availability. 
- It maintains a presence in every Azure datacenter. 
- This configuration makes the Azure portal resilient to individual datacenter failures and avoids network slowdowns by being close to users. 
- The Azure portal updates continuously and requires no downtime for maintenance activities.

### Azure Cloud Shell

- is a <mark>browser-based shell tool that allows you to create, configure, and manage Azure resources using a shell. </mark>
- Azure Cloud Shell support both Azure PowerShell and the Azure Command Line Interface (CLI), which is a Bash shell.

You can access Azure Cloud Shell via the Azure portal by selecting the Cloud Shell icon:

![Screenshot of the Azure portal with the Cloud Shell icon emphasized.](https://learn.microsoft.com/en-us/training/wwl-azure/describe-features-tools-manage-deploy-azure-resources/media/cloud-shell-icon-dbf37a88.png)

Azure Cloud Shell has several features that make it a unique offering to support you in managing Azure. Some of those features are:

- It is a <mark>browser-based shell experience, with no local installation or configuration required.</mark>
- It is <mark>authenticated to your Azure credentials, so when you log in it inherently knows who you are and what permissions you have.</mark>
- You choose the shell you’re most familiar with; <mark>Azure Cloud Shell supports both Azure PowerShell and the Azure CLI (which uses Bash).</mark>

## What is Azure PowerShell?

- is a shell with which developers, DevOps, and IT professionals can run commands called command-lets (cmdlets). 
	- These commands call the Azure REST API to perform management tasks in Azure. 
	- Cmdlets can be run independently to handle one-off changes, or they may be combined to help orchestrate complex actions such as:
- The routine setup, teardown, and maintenance of a single resource or multiple connected resources.
- The deployment of an entire infrastructure, which might contain dozens or hundreds of resources, from imperative code.
- Capturing the commands in a script makes the process repeatable and automatable.
- In addition to be available via Azure Cloud Shell, you can <mark>install and configure Azure PowerShell on <b>Windows, Linux, and Mac platforms.</b></mark>

## What is the Azure CLI?

- It is functionally equivalent to Azure PowerShell, with the primary difference being the syntax of commands. 
- While <mark><b>Azure PowerShell </b>uses <b><i>PowerShell commands</b></i>, the <b>Azure CLI</b> uses <b><i>Bash commands.</b></i></mark>
- The Azure CLI provides the same benefits of handling discrete tasks or orchestrating complex operations through code. It’s also installable on <mark>Windows, Linux, and Mac platforms, as well as through Azure Cloud Shell.</mark>
- Due to the similarities in capabilities and access between Azure PowerShell and the Bash based Azure CLI, *it mainly comes down to which language you’re most familiar with.*


---
## Tags:
#module10 

---
[Previous](Intro-Describe-features-and-tools-for-managing-and-deploying-Azure-resources.md) | [Next](Describe-the-purpose-of-Azure-Arc.md)
