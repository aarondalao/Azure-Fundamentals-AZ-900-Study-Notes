Azure Functions is an ***event-driven, serverless compute option*** that doesn’t require maintaining virtual machines or containers. If you build an app using VMs or containers, those resources have to be “running” in order for your app to function. With Azure Functions, an event wakes the function, alleviating the need to keep resources provisioned when there are no events.

## Serverless computing in Azure
- As a Software Developer, you want to spend time doing what matters, building an application. You don't want to spend time executing tedious, time-consuming tasks like installing an OS or downloading system updates.
- The goal of serverless computing is to help you with this by taking care of those tiresome types of server management tasks, so that you can focus your effort on getting your applications to your customers.
- ***Serverless Computing*** is a bit of misleading name. because there are in fact servers being used. But what it really means is that the responsibility of managing servers is already handled for you.
	- in other words, it's an abstraction of servers so that you can take your mind off of infrastructure concerns and focus them on developer concerns.
## Benefits of Azure Functions
- Using Azure Functions is ideal when you're only concerned about the code running your service and not about the underlying platform or infrastructure. 
- Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.
- Functions scale automatically based on demand, so they may be a good choice when demand is variable.
- Azure Functions runs your code when it's triggered and automatically deallocates resources when the function is finished. In this model, you're only charged for the CPU time used while your function runs.
- Functions can be either ***stateless or stateful***. When they're **stateless** (the default), they behave as if they're restarted every time they respond to an event. When they're **stateful** (called **Durable Functions**), a context is passed through the function to track prior activity.
- Functions are a key component of serverless computing. 
	- They're also a general compute platform for running any type of code. 
	- If the needs of the developer's app change, you can deploy the project in an environment that isn't serverless. 
	- This flexibility allows you to manage scaling, run on virtual networks, and even completely isolate the functions.

---
## Tags:
#module5

---
[Previous](Describe-Azure-Containers.md) | [Next](Describe-application-hosting-options.md)
