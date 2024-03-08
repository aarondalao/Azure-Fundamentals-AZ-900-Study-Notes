When building or deploying a cloud application, two of the biggest considerations are uptime (or availability) and the ability to handle demand (scalability).

### High Availability
- When deploying an app, a service, or any IT Resource, It's important the resources are available when needed.
- High availability focus on ensuring maximum availability, regardless of disruptions or events that may occur.
- When you're architecting your solution, you'll need to account for service availability guarantees. 
- Azure is a highly available cloud environment with uptime guarantees depending on the service. These guarantees are part of the [service level agreements (SLAs)](Service-Level-Agreements.md).

### Scalability
- Refers to the ability to adjust resources to meet demand.
- If you suddenly experience peak traffic and your systems are overwhelmed, the ability to scall means you can add more resources to better handle the increased demand.
- The other benefit of scalability is that you aren't overpaying for your services.
	- because the cloud is a consumption-based model, you only pay for what you use.
- Scaling generally comes in two varieties: Vertical and Horizontal
	- Vertical Scaling is focused on increasing or decreasing the capabilities of resources.
	- Horizontal Scaling is focused on increasing or decreasing the number of resources or instances.

### Vertical Scaling
- if you were developing an app and you needed more processing power, you could vertically scale up to add more CPUs or RAMs to the virtual Machine.
- Conversely, if you realized you had over-specified the needs, you could vertically scale down by lowering the CPU or RAM Specifications.

### Horizontal Scaling
- if you suddenly experienced a steep jump on demand, your deployed resources could be scaled out (either by automatically or manually). (Add more virtual Machines or containers)
- in the same manner, if there was a significant drop in demand, deployed resources could be scaled in (either automatically or manually).

---
## Tags:
#module2

---
[Previous](Intro-Benefits-of-Using-Cloud-Services.md) | [Next](Describe-the-Benefits-of-Reliability-and-Predictability-in-the-Cloud.md)
