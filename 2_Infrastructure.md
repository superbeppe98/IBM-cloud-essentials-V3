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

- Next, we're going to go ahead and configure, create, and connect to a virtual server instance
    - From the IBM cloud catalog, we can see the different options we can choose from virtual server, bare metal, hyper, protect and power systems
    - You can see the different profiles that are available for virtual servers
    - After a few minutes our virtual server will be spun up
    - Let's click on the link to see some details about the server
    - On the top right, we have in action button; that lists all the different kinds of actions we can take with the virtual server, such as shutdown, reset
    - Let's open up a terminal and try an SSH into our machine
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

- Up next, we have a quick demonstration of how to attach a volume onto a virtual server
    - From the IBM cloud catalog, we're going to go ahead and find the file storage service
    - We're going to go ahead and select the data center that's associated with our virtual machine and deploy a virtual machine
    - Go back to your device list, find the virtual machine that you want to attach the storage to
    - Find the file storage section, click authorize storage
    - Go ahead and click the storage volume that we just created.
    - We have to go into the system and Mount it.
    - You'll find the Mount Point value when you go and see the file storage properties.
    - So, let's SSH into our VM again.
    - And show that it is in fact mounted on /NFS/extra.
<br>

## Hands-on Lab: Using the Catalog and Cloud Shell

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database
    - Launch the IBM Cloud Shell
    - Use the IBM Cloud CLI

<br>

## Hands-on Lab: Using the Catalog and Cloud Shell

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database
    - Launch the IBM Cloud Shell
    - Use the IBM Cloud CLI

<br>

[Go to Next Module](./3_Deploying_Applications.md)
