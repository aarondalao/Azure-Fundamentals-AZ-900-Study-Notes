If you need to host your application on Azure, you might initially turn to a virtual machine (VM) or containers. Both VMs and containers provide excellent hosting solutions. VMs give you maximum control of the hosting environment and allow you to configure it exactly how you want. VMs also may be the most familiar hosting method if you’re new to the cloud. Containers, with the ability to isolate and individually manage different aspects of the hosting solution, can also be a robust and compelling option.

There are other hosting options that you can use with Azure, including Azure App Service.

---
### Azure App Service
- enables you to build and host web apps, background jobs, mobile back-ends, and [RESTful API](Terminologies#REST) in the programming language of your choice without managing infrastructure.
- It offers automatic scaling and high availability.
- App Service supports Windows and Linux.
	- It enables automated Deployments from Github, Azure [DevOps](Terminologies#DevOps), or any Git repo to support [Continuous Deployment Models](Terminologies#CI/CD)
- Azure App Service is a robust hosting option that you can use to host your apps in Azure.
- Lets you focus on building and maintaining you app, and Azure focuses on keeping the environment up and running.
- it is also a HTTP-based Service for hosting web apps, REST APIs and mobile back-ends.
	- It supports multiple languages, including .NET, .NET Core, Java, Ruby, Node.js, PHP, or Python.
	- It also supports both Windows and Linux Environments.
### Types of App Services

With App Service, you can host most common app service styles like:
- Web Apps
- API Apps
- WebJobs
- Mobile Apps

App Service handles most of the infrastructure decisions you deal with in hosting web-accessible apps:
- Deployment and management are integrated into the platform
- Endpoints can be secured
- Sites can be scaled in quickly to handle high traffic loads.
- Built-in load balancing and traffic manager provide high availability.

### API apps
- Much like hosting a website, you can build REST-based web APIs by using your choice of language and framework. 
- You get full Swagger support and the ability to package and publish your API in Azure Marketplace. 
- The produced apps can be consumed from any HTTP- or HTTPS-based client.

### WebJobs
- You can use the WebJobs feature to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app. 
- They can be scheduled or run by a trigger.
	- WebJobs are often used to run background tasks as part of your application logic.

### Mobile apps
- Use the Mobile Apps feature of App Service to quickly build a back end for iOS and Android apps. With just a few actions in the Azure portal, you can:
	- Store mobile app data in a cloud-based SQL database.
	- Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook.
	- Send push notifications.
	- Execute custom back-end logic in C# or Node.js.
- On the mobile app side, there's SDK support for native iOS and Android, Xamarin, and React native apps.

---
## Tags:
#module5

---
[Previous](Describe-Azure-Functions.md) | [Next](Describe-Azure-Virtual-Networking.md)
