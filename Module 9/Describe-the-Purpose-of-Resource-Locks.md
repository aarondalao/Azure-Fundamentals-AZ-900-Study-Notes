### Resource Lock 
- <mark>prevents resources from being accidentally deleted or changed.</mark>
- Even with Azure role-based access control (Azure RBAC) policies in place, there's still a risk that people with the right level of access could delete critical cloud resources. 
- Resource locks prevent resources from being deleted or updated, depending on the type of lock. Resource locks can be applied to ***individual resources, resource groups, or even an entire subscription. ***
	- Resource locks are inherited, meaning that if you place a resource lock on a resource group, all of the resources within the resource group will also have the resource lock applied.

## Types of Resource Locks

- There are *two types* of resource locks, one that <mark>prevents users from deleting</mark> and one that <mark>prevents users from changing or deleting a resource.</mark>
	- **Delete** means <mark>authorized users can still read and modify a resource, but they can't delete the resource.</mark>
	- **ReadOnly** means <mark>authorized users can read a resource, but they can't delete or update the resource. </mark>Applying this lock is similar to restricting all authorized users to the permissions granted by the Reader role.

## How do I manage resource locks?

- You can manage resource locks from the ***Azure portal, PowerShell, the Azure CLI, or from an Azure Resource Manager template.***
- To view, add, or delete locks in the Azure portal, go to the Settings section of any resource's Settings pane in the Azure portal.

![A screenshot showing the resource lock control, under settings, for a storage account.](https://learn.microsoft.com/en-us/training/wwl-azure/describe-features-tools-azure-for-governance-compliance/media/resource-lock-54695e43.png)

## How do I delete or change a locked resource?

- Although locking helps prevent accidental changes, you can still make changes by following a two-step process.
- <mark>To modify a locked resource, you must first remove the lock.</mark> 
	- After you remove the lock, you can apply any action you have permissions to perform. 
- Resource locks apply regardless of RBAC permissions. 
- Even if you're an owner of the resource, you must still remove the lock before you can perform the blocked activity.

---
## Tags:
#module9 

---
[Previous](Describe-the-Purpose-of-Azure-Policy) | [Next](Exercise-Configure-a-Resource-Lock.md)
