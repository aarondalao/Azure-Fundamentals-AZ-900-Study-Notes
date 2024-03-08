# Terminologies
- these are collections of common terminologies that are not mentioned from the Microsoft Azure Fundamental AZ-900 Challenge.
#### API 
- Application Programming Interface
- is a set of routines, protocols, and tools for building software applications. 
- Basically, an API specifies how software components should interact. 
- Additionally, APIs are used when programming graphical user interface (GUI) components.
- A good API makes it easier to develop a program by providing all the building blocks. A programmer then puts the blocks together.
#### CLI
- Command Line Interface
- is a text-based interface where you can input commands that interact with a computer's operating system.
#### VM
- Virtual Machine
- is a compute resource that uses software instead of a physical computer to run programs and deploy apps. 
- One or more virtual “guest” machines run on a physical “host” machine.  
- Each virtual machine runs its own operating system and functions separately from the other VMs, even when they are all running on the same host. 
- This means that, for example, a virtual MacOS virtual machine can run on a physical PC.
#### Virtualization
- Virtualization is the process of creating a software-based, or "virtual" version of a computer, with dedicated amounts of CPU, memory, and storage that are "borrowed" from a physical host computer—such as your personal computer— and/or a remote server—such as a server in a cloud provider's datacenter.

#### TCO
- [Total Cost of Ownership](https://www.investopedia.com/terms/t/totalcostofownership.asp)
- Total cost of ownership (TCO) is the [purchase price](https://www.investopedia.com/terms/p/purchaseprice.asp) of an [asset](https://www.investopedia.com/terms/a/asset.asp) plus the costs of operation. Assessing the total cost of ownership means taking a bigger picture look at what the product is and what its value is over time. 
- When choosing among alternatives in a purchasing decision, buyers often look at an item’s short-term price, known as its purchase price. 
- However they should also consider its long-term price, which is its total cost of ownership. 
- These are the long-term costs and expenses incurred during the product’s useful life and ultimate disposal. 
- The item with the lower total cost of ownership can be the better value in the [long run](https://www.investopedia.com/terms/l/longrun.asp).
- ***In terms of the Cloud, specifically Azure***, TCO Estimate the cost savings you can realise by migrating your workloads to Azure.

#### REST
- Representational State Transfer
- describes the general rules for how the data and services are represented through the API so that other programs will be able to correctly request and receive the data and services that an API makes available

#### CI/CD
- Continuous Integration / Continuous Deployment
- [Continuous integration](https://www.redhat.com/en/topics/integration?cicd=32h281b "Red Hat | Understanding enterprise integration") (CI) refers to the practice of [automatically](https://www.redhat.com/en/topics/automation?cicd=32h281b "Understanding automation") and frequently integrating code changes into a shared source code repository. [Continuous delivery](https://www.redhat.com/en/topics/devops/what-is-continuous-delivery?cicd=32h281b "What is continuous delivery?") and/or deployment (CD) is a 2 part process that refers to the integration, testing, and delivery of code changes. 
- Continuous delivery stops short of automatic production deployment, while continuous deployment automatically releases the updates into the production environment.

#### DevOps
- Development Operations
- DevOps combines development (Dev) and operations (Ops) to increase the efficiency, speed, and security of software development and delivery compared to traditional processes. A more nimble software development lifecycle results in a competitive advantage for businesses and their customers.

#### Repo
- Repository
- contains all of your code, your files, and each file's revision history. You can discuss and manage your work within the repository.

#### BGP
- [Border Gateway Protocol](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-bgp-overview)
- is the standard routing protocol commonly used in the Internet to exchange routing and reachability information between two or more networks.
- [Border Gateway Protocol (BGP)](https://aws.amazon.com/what-is/border-gateway-protocol/#:~:text=Border%20Gateway%20Protocol%20(BGP)%20is,%2C%20devices%2C%20and%20communication%20technologies.) is a set of rules that determine the best network routes for data transmission on the internet. The internet consists of thousands of private, public, corporate, and government networks linked together through standardized protocols, devices, and communication technologies.

#### VPN
- [Virtual Private Network](https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-vpn#:~:text=A%20VPN%2C%20which%20stands%20for,and%20firewalls%20on%20the%20internet.)
- establishes a digital connection between your computer and a remote server owned by a VPN provider, creating a point-to-point tunnel that encrypts your personal data, masks your IP address, and lets you sidestep website blocks and firewalls on the internet. This ensures that your online experiences are private, protected, and more secure.
- By its very definition, a VPN connection is:
	- **Virtual** because no physical cables are involved in the connection process.  
    - **Private** because through this connection, no one else can see your data or browsing activity.  
    - **Networked** because multiple devices—your computer and the VPN server—work together to maintain an established link.
#### RPO
- [**Recovery Point Objective**](https://learn.microsoft.com/en-us/azure/reliability/disaster-recovery-overview#:~:text=Recovery%Point%Objective%(RPO)%is%the%maximum%duration%of,not%data%theft)
- is the maximum duration of acceptable data loss. RPO is measured in units of time, not volume, such as "30 minutes of data" or "four hours of data." RPO is about limiting and recovering from data loss, not data theft.

#### RTO
- [**Recovery Time Objective**](https://learn.microsoft.com/en-us/azure/reliability/disaster-recovery-overview)
- s the maximum duration of acceptable downtime, where "downtime" is defined by your specification. For example, if the acceptable downtime duration in a disaster is eight hours, then the RTO is eight hours.

#### MFA
- [Multifactor Authentication](https://support.microsoft.com/en-au/topic/what-is-multifactor-authentication-e5e39437-121c-be60-d123-eda06bddf661)
- it is a multi-step account login process that requires users to enter more information than just a password. For example, along with the password, users might be asked to enter a code sent to their email, answer a secret question, or scan a fingerprint. A second form of authentication can help prevent unauthorized account access if a system password has been compromised.

#### SSA
- [Single Sign-on](https://learn.microsoft.com/en-us/entra/identity/enterprise-apps/what-is-single-sign-on)
- it is an authentication method that enables users to securely authenticate with multiple applications and websites by using just one set of credentials.

#### Authentication
- is the process that companies use to confirm that only the right people, services, and apps with the right permissions can get organizational resources. 
- It’s an important part of [cybersecurity](https://www.microsoft.com/en-us/security/business/security-101/what-is-cybersecurity) because a bad actor’s number one priority is to gain unauthorized access to systems
- They do this by stealing the username and passwords of users that do have access. The authentication process includes three primary steps:
	- Identification
		- Users establish who they are typically through a username.
	- Authentication
		- Typically, users prove they are who they say they are by entering a password (something only the user is supposed to know), but to strengthen security, many organizations also require that they prove their identity with something they have (a phone or token device) or something they are (fingerprint or face scan).
	- Authorization: 
		- The system verifies that the users have permission to the system that they’re attempting to access.
#### CSPM
- [Cloud security posture management](https://learn.microsoft.com/en-us/azure/defender-for-cloud/concept-cloud-security-posture-management)
- provides detailed visibility into the security state of your assets and workloads, and provides hardening guidance to help you efficiently and effectively improve your security posture.
#### AWS-CIS
- [AWS Center for Internet Security](https://docs.aws.amazon.com/securityhub/latest/userguide/cis-aws-foundations-benchmark.html)
- The CIS AWS Foundations Benchmark serves as a set of security configuration best practices for AWS. 
	- These industry-accepted best practices provide you with clear, step-by-step implementation and assessment procedures. 
	- Ranging from operating systems to cloud services and network devices, the controls in this benchmark help you protect the specific systems that your organization uses.

#### AWS-PCI-DSS
- [AWS Payment Card Industry Data Security Standard](https://docs.aws.amazon.com/securityhub/latest/userguide/pci-standard.html)
- The Payment Card Industry Data Security Standard (PCI DSS) in Security Hub provides a set of AWS security best practices for handling cardholder data. 
	- You can use this standard to discover security vulnerabilities in resources that handle cardholder data. 
	- Security Hub currently scopes the controls at the account level. 
	- We recommend that you enable these controls in all of your accounts that have resources that store, process, or transmit cardholder data.

#### AWS-FSBP
- AWS Foundational Security Best Practices
- The AWS Foundational Security Best Practices standard is a set of controls that detect when your AWS accounts and resources deviate from security best practices.
	- The standard lets you continuously evaluate all of your AWS accounts and workloads to quickly identify areas of deviation from best practices. 
	- It provides actionable and prescriptive guidance about how to improve and maintain your organization’s security posture.

---
## Azure Services #WIP
-  This will be a one-stop place to define the core services offered by Azure.

#### Microsoft-Entra-ID
- Other Name/Old Name: **Azure Active Directory (AD)**
- [Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/whatis) is a cloud-based ***identity and access management*** service that enables your employees access external resources. 
- Example resources include Microsoft 365, the Azure portal, and thousands of other SaaS applications.
- Microsoft Entra ID also helps them access internal resources like apps on your corporate intranet, and any cloud apps developed for your own organization. To learn how to create a tenant, see [Quickstart: Create a new tenant in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/create-new-tenant).
- To learn the differences between Active Directory and Microsoft Entra ID, see [Compare Active Directory to Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/compare). You can also refer to [Microsoft Cloud for Enterprise Architects Series](https://learn.microsoft.com/en-us/microsoft-365/solutions/cloud-architecture-models) posters to better understand the core identity services in Azure like Microsoft Entra ID and Microsoft-365.



---
## Tags:
#General #WIP #Terminology

---
[Previous](Intro-to-Microsoft-Azure-Fundamentals) | [Next](Intro-Benefits-of-Using-Cloud-Services.md)