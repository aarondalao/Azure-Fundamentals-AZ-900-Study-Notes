- a standard industry term
- it is a formal agreement between a service provider and customer that guarantees the customer a stated level of service
	- also used inside organizations, in an agreement between the IT Department, and the business user
- Service Provider
	- may be a commercial company, providing the service (Microsoft for Azure Services, Amazon for AWS, Alphabet for GCP)

## SLA's for Azure
- are represented as a percentage, related to the service or application's availability.
- If the service was always available to use, you'd say it way 100% available / uptime.
- also defines what is defined as down time, when the service is unavailable.
	- and any credit you may be entitled to if the SLA is not met.
- In reality, 100% uptime is expensive and difficult to achieve because it allows no time for taking the service down for required maintenance or upgrades.
	- it also requires duplicating every single component in case one component fails and would require those back up components to pick up the service tasks with zero interruption to the customer.
	- For these reasons, 99%, 99.9%, and 99.95% are more common. 99.99% is also available in some services in Azure.
	- A service with a 99% SLA percentage can be unavailable for up to 1.68 hours/week or 7.2 hours/month. That time is **cumulative**, which means it can be added up over multiple incidents of the service being unavailable
	- A service with a 99.9% SLA percentage can be unavailable for only 10 minutes/week or 43.2 minutes/month.
	- Minutes versus Hours of downtime can make a big difference, but highly available services **do come at an extra cost.**
- Each Azure service has its own SLA. Familiarize yourself with them prior to designing any application that runs on Azure to ensure your optimizing availability against your business needs.

### Resources

This [link](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services?lang=1) will guide you through the SLAs of each Online Services of Microsoft, from Azure, Dynamics 365, Office 365, Intune, Etc. 
***note: as of the time of writing, the latest SLA is March 01, 2024***

---
## Tags:
#module2

---
[Previous](Benefits-of-Using-Cloud-Services.md)
