[Back to Syllabus](/READMEmd#course-syllabus)

## Learning Objectives

- Virtual Servers: This lesson includes a breakdown of the virtual server configurations, supported architectures, and pricing models
- Block and File Storage: An introduction to cloud-based storage, advantages of block and file storage, and recovery options
- Cloud Object Storage: An introduction to object storage and deep dive into the benefits of using IBM Cloud Object Storage
- Networking: This lesson covers the Cloud Internet Services provided by Cloudflare, as well as infrastructure level networking offerings such as load balancers and VPNs 
- Virtual Private Cloud: This lesson offers an introduction to IBM Cloud’s Virtual Private Cloud (VPC) offerings 
- VMware: This lesson covers hosted VMware Solutions on IBM Cloud that offer vSphere and vCenter options.
<br>

## Virtual Servers

- There are four types of virtual server offerings on IBM cloud
    - The first is the virtual server service: this is your usual virtual machine type service that offers a range of operating system and configurable RAM and processing power to fit your use case
    - The bare metal service: this service provides you the raw horsepower that you need for processing intensive and disk IO intensive workloads
    - The power system service: This service, as its name implies, allows you to spin up power system servers with operating systems such as AIX and IBM I
    - The hyper protect service: This service allows you to run virtual servers on IBM Linux 1. You get access to Z technology without having to purchase any unique hardware

- Virtual servers can be deployed in any IBM data center around the world
    - Public servers or multi-tenant in are billed hourly or monthly
    - Dedicated servers are like public servers but they're single tenant
    - Transient servers are the least expensive option, but our D provisioned as capacity grows
    - Reserved servers: these are committed to a one- or three-year contract

- You can choose between different images such as CentOS, Debian,Microsoft Red Hat, and Ubuntu; each with different versions of operating systems for each image
- The virtual machine could have up to 64 V CPU and 512 gigabytes of ram, you can choose to upgrade to a 1 gigabyte per second network connection, and you can even include five SAN volumes and two GPUs that are based on NVIDIA Tesla P-100's

- Bare metal servers like the virtual server counterpart can be provisioned in any IBM data center around the world
    - The service has multiple billing options ranging from hourly, monthly to a one-year and three-year contract depending on the bare metal service you select
    - Much like the virtual server option, you can choose the images that are on there
    - Or you can choose more bare metal specific images like VMware, Citrix or Cloud Linux
    - We offer both VM Ware and SAP certified bare metal servers
    - You can go from 4 cores to 72 core
    - You can go up to 6 terabytes of Ram, an up to 36 drives
    - Lastly, there's GPU support, which is again based off the NVIDIA Tesla P-100 cards

- Let's look at the power system server
    - They're used to deliver flexibel compute capacity for power system workloads
    - They can be deployed to specific data centers in Frankfurt, London, Toronto, Washington
    and Dallas
    - You can choose between the E 880 an S 922 machines and you can choose from various AIX
    and IBM I images or bring your own

- Up next, we have the hyper protect servers
    - These can be deployed to specific data centers in Dallas, Frankfurt, Sydney, and Washington
    - A few other things to note about the hyper protect server
    - Allows you to create an run virtual servers on IBM Linux one, the industry's most secure
    Linux based platform
    - They offer added security as these servers deployed in any secure service container.
    - They're easy to configure and deploy as any other virtual machine, and there are no Z
    skills or hardware required
    - Let's go ahead and compare these virtual server offerings
    - Unsurprisingly, the virtual server option is the cheapest
    - In terms of performance, the power systems an bare metal, had the most to offer and in
    terms of security, it's hard to beat the Linux one offering up
<br>

## Hands-on Lab: (Optional) Upgrade your IBM Cloud account

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Upgrade your account

<br>

## Hands-on Lab:  (Optional) SSH into a Virtual Server

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Add an SSH key to your account
    - Provision a virtual server
    - SSH into a virtual server

<br>

## Block and File Storage
- There are three types of block and file storage related services on IBM Cloud
    - Block storage service: provides virtual servers and bare metal servers with a SAN-like iSCSI storage
    - File storage service: provides virtual servers and bare metal servers with an NFS based storage
    - Cloud backup service: enterprise level backup storage and disaster recovery solution

- Let's start by looking at what block and file storage related services have in common
    - Both are managed through the console or CLI
    - You can authorize a server and mount the volume
    - They are highly durable and resilient 
    - No need to create raid arrays
    - Sizes range from 20 gigabytes to 12 Terabytes and can be increased after Provisioning
    - Data is protected as encryption at rest, is available at no additional charge
    - The number of IOPS, input output operations per second, can be adjusted on the fly and it can go up to 48,000
    - Block and file storage volumes can be provisioned in any IBM Cloud data center around the world
    - And also, you're able to create snapshots manually or schedule them in advance

- Now let's look at how these two services differ
    - Well, first block storage uses iSCSI, whereas file storage uses NFS
    - Block storage can only be attached to one host at a time, whereas file storage can be attached to many
    - You'll likely use block storage for high intensity workloads like a database, whereas file storage and is ideal for workloads that do not require fast connectivity to storage

- Let's talk about the IBM cloud backup service
    - It's used to backup and restore data between servers in one or more IBM cloud data centers
    - Very customizable: you can choose to backup daily, weekly, or on a custom schedule; you can even target full systems, specific directories or even individual files

- Next, is the management portal
    - It's a browser-based portal, allows you to schedule jobs, set retention policy, and perform one click restores
    - Next, there are multiple plugins available for Ms SQL, Ms SharePoint and Oracle
    - Next, it offers end to end data encryption
    - Data is protected at source in transit and to the destination vaults with 256 bit private key encryption

- Lastly, there's also Geo Redundancy
    - You can protect your data across geographically dispersed sources
<br>

## Object Storage
- Object storage is great for storing vast amounts of unstructured data
    - Files are uploaded as objects and saved into buckets
    - Within a bucket, there is no directory or tree structure
    - When an object is placed in a bucket, it is given a unique identifier
    - It has some metadata, like when the data was uploaded or last accessed

- Benefits
    - Access management control: you can set policies on who can access and modify objects via IBM Clouds IAM settings
    - Encryption: all objects stored in IBM Cloud object storage and are encrypted by default; additionally, you can encrypt the data using your own keys with IBM key protect
    - SQL query support: you can run SQL queries against objects stored in buckets
    - High speed transfer: you can leverage esparra to upload data quickly
    - SDK's and API's: objects can be accessed via an S3 compatible rest API or with an SDK that is written for many popular programming languages

- IBM Cloud's object storage service offers different levels of resiliency
    - The cross region option for your instance means that your data is stored across three regions within a geography: this will offer you the highest possible availability, but at the lowest performance level
    - The regional choice is a great blend of availability, performance, and service integration: less available than cross region but is higher performance and when more integration with other services; the single data centers choice is 1; your data is stored across multiple devices in a single data center; this is recommended when keeping your data in country is a top priority.

- There are four different tiers of storage class for IBM Cloud object storage
    - Smart tier: it will automatically give you the lowest storage rate based on your monthly activity
    - The standard storage class: is great when your data needs to be accessed frequently; it is a higher cost per GB, but as higher performance
    - The vault storage class is ideal for data which needs to be accessed once a month or less
    - This is cheaper than the standard storage class, but a bit more expensive than the coldvault option
    - The cold vault option is usually used for archives where data is only accessed a few times per year
<br>

## Hands-on Lab: Get to Know Cloud Object Storage

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create the service
    - Create a bucket
    - Download from the bucket
![2022-08-18 20 51 44 cloud ibm com 745023d27698](https://user-images.githubusercontent.com/29455975/185472076-98976a20-a7da-4f14-98b0-34c53c9aa61b.jpg)
<br>

## Network Services
- IBM Cloud has two different services for networking
    - The first is called Cloud Internet services; this service is based on Cloudflare
    - The second is a collection of networking infrastructure services with options for Vlans, VPNs, and CDN's

- The cloud Internet services provide reliable, secure options for Internet facing applications by leveraging Cloudflare
    - Cloudflare, if you're not familiar, is a web infrastructure company that provides DNS services to 12 million websites and has over 165 points of presence all over the world

- Within IBM Cloud you can use cloud Internet services to configure the following:
    - Domain name server for host name resolution
    - Transport layer security to secure data
    - Global load balancer to reduce latency and increase availability by routing traffic based on server availability and health
    - Rate limiting, which automatically identifies and mitigates excessive request rates
    - DDoS protection, a scalable configurable service that protects against brute force attacks
    - Smart routing, which ensures content is delivered on the fastest path from end user to application
    - Web application firewall, a layered defense to protect data against sophisticated attackers and malicious bots and caching, which reduces latency and improves performance

- There are many networking related services on IBM Cloud
    - The Gateway appliance enables you to create virtual routers, firewalls and private networking devices
        - You can choose between a Juniper or AT&T based appliance
        - There are both hardware and software-based firewalls
        - These will prevent malicious activity, helping to ensure uptime of your server
        - You can add a firewall to a specific virtual server
    - Next are VPNs
        - VPNs facilitate connectivity from your network to IBM's private network
        - Subnets and IPS subnets provide additional IP addresses for virtual machines
        - There are managed independently of virtual machine resources and are available until cancelled
    - Lastly, we have virtual local area networks or VlANs
        - AV line is used to provide packet identification and to let multiple workloads coexist on the same physical equipment
        - Depending on your situation, you may never need to interact with VLANss directly because they are managed automatically

- Let's talk about the direct link service
    - Direct link creates a direct private connection between remote networks and IBM Cloud
    - With direct link you have a secure dedicated connectivity
    - It gives you private access to IBM Cloud infrastructure
    - It offers a fully integrated hybrid environment
    - Whether your resources are in a data center or on IBM Cloud, direct link is perfect for creating multi cloud connectivity in a single environment
    -  And lastly we have speed
        - With direct link you can choose between speeds of 5100, 500 megabits per second or even up to five gigabits per second as your needs change
        You can transition your speed seamlessly

    - IBM Cloud also provides a CDN service
    - A CDN is a highly distributed platform of servers to help minimize delays
        - First off, it's based off Akamai, a best of breed CDN provider to create one of the world's fastest and most reliable content delivery networks
        - Second, smarter scaling automatically scale your service globally to over 2200 points of presence in 36 countries
        - Using a CDN also makes things more secure as now you have a new layer between yourself and infrastructure attacks
        - You can use it to optimize dynamic content
        - You can direct customer requests
        - Through optimized routes, proactively fetching content from origin and large file compression
    - Lastly, there is usage-based pricing
        - Pay for what you use with no minimum monthly fee
        - The last service we'll talk about is the load balancer, which is used to distribute traffic among to your virtual servers
        - You can choose between an IBM Cloud load balancer or a Citrix Netscaler VPX load balancer
        - Elastic load balancers allow for layer four and layer seven load balancing
        - This includes HTTP, HTTPS, NTCP, Public and private load balancing, server health checks, SSL offload, and monitoring metrics
<br>

## Virtual Private Cloud
- What is a virtual private cloud?
    - A virtual private cloud is a secure, isolated private cloud hosted within a public cloud
    - It gives you the security of a private cloud with the cost effectiveness and scalability of a public cloud
    - It offers an on-demand configurable pool of shared resources allocated within a public cloud environment
    - There is isolation between users achieved through private IP subnets and encrypted communication channels
    - In a virtual private cloud, there is a function which authenticates users and provides remote access to the shared resources
    - Virtual private clouds provide the necessary infrastructure in isolation as a fully automated solution

- VPC's allow you to create multiple virtual private clouds in multi zone regions, create subnets in different zones, each region has multiple zones
    - Security groups which are created to filter each network interface by a virtual server based on IP address
    - You can create virtual server instances quickly using predefined profiles optimized for your specific workload
    - You can use a public gateway to enable communication to the Internet for all virtual server instances on the attached subnet
    - You can also add block storage to your virtual private cloud instance by default, a 100 Gigabyte General purpose block storage volume is created automatically

- Let's take a look at a sample architecture for an IBM virtual private cloud
    - First, when the user connects to the Internet and goes to a specific URL, they will need to authenticate to the network.
    - This is the first blue box around our architecture; this will give them a certain predefined access to the network
    - We can see that the VPC Network which is deployed in a specific zone within a region where there are storage, virtual server instances, gateways and load balancers are also hosted
    - The VPC network has access to many cloud services such as AI, databases, IoT and Container Registry 
    - The network also has access to DevOps services including monitoring, log analysis, and continuous delivery

- It's worth noting that right now there are two generation VPC options on IBM cloud.
    - With generation one, it is available in all six regions you have up to 16 gigabytes per second networking
    - With generation two, it's available in five regions and you can get networking speeds of up to 80 gigabytes per second
    - Currently there is only support for provider managed security
<br>

## Vmware
- So why use VMware on cloud?
    - Well, in the early 2000s, before we really had any major public clouds, VMware Solutions became the standard for desktop and server virtualization
    - Many companies were using VMware to virtualize their workloads
    - VMware software was deployed to servers and data centers all over the world
    - In fact, many IBM clients were using VMware or still using VMware to this day
    - In 2016, IBM Cloud became the first cloud vendor to bring VMware services to the cloud

- Why migrate workloads?
    - The 1st and biggest reason is to bring cloud economies to VMware workloads
    - You can expect far less spending on capital expenditures
    - This includes things like purchasing equipment, data centers, so forth
    - By using a cloud provider, you ensure your workloads can take advantage of the underlying highly available networking between regions of a cloud

- IBM Cloud offers two VMware based services
    - The first is VMware solutions dedicated
        - This is a single tenant bare metal solution that has options for vCenter Server and VMware vSphere
        - This service allows you to retain root level access to the hypervisor, giving you a similar experience as you would have on premises in a data center
    - The second is VMware Solutions shared
        - This is a multi-tenant solution that uses shared infrastructure and provides a VMware environment based on Vcloud director
        - The VM ware solutions dedicated service is a bare metal solution with vCenter and vSphere options
        - With the dedicated solution, the customer still has root access down to the hypervisor level
        - The V center option is a fully automated, standardized software defined data center
        - Networking, storage and add ONS can be automatically configured at install time
        - The vSphere option allows for more customization for networking, storage and add ons

- Both solutions provide the option to purchase IBM provided licenses or to bring your own license
- You can also deploy add on services to a new or existing instance
- This includes security and compliance services like big IP and business continuity and migration services like Veeam and Zerto

- On the other hand, we have VMware Solutions shared
    - This allows you to deploy workloads on top of IBM hosted VMware infrastructure
    - IBM provides a self-service on-demand VMware cloud computing platform with VMware vCloud Director running on IBM Cloud
    - With the shared solution IBM manages up to the hypervisor level
    - It's very cost effective
    - You only pay for what you use, and you can start small as small as one V CPU and 1 Gigabyte of ram and expand when you're ready
    - The shared option is perfect for temporary migration and burst scenarios
    - Linked into this is disaster recovery
    - Veeam services enable an economical landing zone for disaster recovery workloads
    - Lastly, self-service, the shared service interface was designed to get you productive from day one
    - You can get up and running within minutes

- So why use VMware on IBM Cloud?
    - IBM Cloud has several unique advantages
    - The first is security, which is provided via encryption and access control
    - IBM provides the highest level of encryption for data at rest and data in motion with FIPS 142 Level 4 based encryption

- Next is compliance
    - We can comply with data sovereignty regulations and sharing
    - We provide geofencing for your workloads

- Expertise
    - IBM is one of the world's largest operators of VM Ware workloads
    - With over 15 years of experience, we've managed over 850,000 workloads and have migrated over 100,000 workloads from on Prem to the cloud
    - This is across many different industry verticals, from government to banking to retail

- The last one I'll mention is rapid setup
    - IBM Cloud's automation can quickly get your VM Ware deployment up and running in hours, not days or weeks
    - At the time of this video, there are 13 optional services you can add to your VM Ware deployment
    - These range from security and compliance to business continuity and migration type services

- I've picked three to talk about at a high level
    - First, we're going to talk about Veeam; it allows you to backup and replicate virtual machines on VM Ware easily
    - Next is Zerto, which assists with creating and managing disaster recovery with VMware
    - And lastly, we have the F5 Big IP Suite of products: these help in networking and security related tools for your VMware solution; it covers things like load balancing, firewalls, DNS and more
<br>

[Go to Next Module](./3_Deploying_Applications.md)
