[Back to Syllabus](/README.md#course-syllabus)

## Learning Objectives

- IBM Cloud Deployment Options
- Cloud Foundry
- Kubernetes
- OpenShift
- Serverless
<br>

## Containers and Kubernetes

- What exactly are containers?
    - A container can be thought of a packaging up your application source code dependencies, like runtimes, binaries, libraries, and data
    - Packaged up container is called an image
    - Images are stored in what is called a registry
    - You'll see terms like images, image registry, a lot when talking about containers

    - Before we get into the why, let's talk about the history
    - The term container may be new, but the concept of isolating processes has been around since the 80s
    - With freebsd jails in the 2000s being a popular example
    - The open source project docker made containers an industry standard with simple developer tools that work on both Linux and windows
    - Since then, there have been multiple container runtimes like PodMan, Cryo and container D
    - There are many, many more
    - The container ecosystem has moved to adopting specifications from the open container initiative or OCI

- Last up, we have image registries
    - These can be both private and public, will be getting to that a little bit more later

- So why use container?
    - There are many reasons why
    - Here are a few, the first being that it's portable
    - You can run them anywhere
        - Containers are abstracted away from the host operating system, making them portable
        - They can run uniformly inconsistent across any platform or cloud
    - Next is speed and efficiency
        - Containers share the host operating system kernel and are not bogged down with extra overhead
        - This means you'll have faster startup times as your containers are inherently smaller in capacity compared to VMs
    - The last reason is security and isolation
        - Containers inherently prevent the invasion of malicious code from affecting other containers in the host operating system
        - Additionally, security permissions can be defined to block unwanted components from entering containers or limit communication with unnecessary resources

- Running a few containers on your own is fine, but what do you do when you're running hundreds or thousands?
    - That's where you need a container orchestration
    
- That's exactly what Kubernetes is
    - Kubernetes is an open source project under the Cloud Native Computing Foundation, or CNCF
    - It's around six years old, has thousands of commits, and is a vibrant, well-supported open source
    - Ecosystem with many vendors contributing to the project
    - There are over 150 certified Kubernetes providers on the market today
    - The goal of Kubernetes is to make everything associated with deploying and managing your containers easier and has automated rollouts and rollbacks
    - Kubernetes will automatically scale your services up or down based off of Utilization
    - Ensuring you're only running what you need when you need it
    - It will monitor the health of your services to prevent bad roll outs before things go bad
    - They will also continuously run health checks against your services
    - Restarting containers that fail
    - Most importantly, Kubernetes is built to be used anywhere, allowing you to orchestrate deployments to public clouds, private clouds, on premise or hybrid deployments

-   We're going to quickly talk about her Kubernetes works at a very high level
    - The main way a System Administrator would interact with Kubernetes is through the kubectl CLI
    - It's configured to talk to a specific Kubernetes cluster
    - Each cluster will have a master node and at least one worker node
    - Each worker node can support running multiple pods
    - Each pod is intern running an image of a containerized application
    - IBM Cloud offers a fully managed Kubernetes service in a matter of minutes
    - You can spin up your own Kubernetes cluster, have access to worker nodes and start deploying applications

- IBM Cloud's Kubernetes service has many benefits
    - One, it's fully managed and provides automatic upgrades
    - Two, it’s secure
        - The IBM Cloud Kubernetes service has broad industry compliance including PCI ,HIPAA, SOC1, and more
    - Three, you can configure your cluster as a single or multi zone cluster.
    - Next, are these supported add ons
        - In just a few clicks you can install a service mesh or serverless add onto your cluster
    - Lastly, there's logging and monitoring
        - You can monitor and troubleshoot, define alerts, design custom dashboards, and more

- Let's dive a little deeper on the IBM Cloud Kubernetes service
    - The IBM Cloud community service can be deployed to any of the six regions on IBM Cloud
    - This includes North America, East, West, South, the APAC Region, Europe and South America

- There are different ways to deploy IBM Cloud Kubernetes service
    - The first is on a virtual shared instance
        - This provision IKS on virtual machines
    - Next is a virtual dedicated instance which is going to provide your Kubernetes cluster on a dedicated server
        - Recall that this is a single tenant instance
    - You can provision your Kubernetes cluster on bare metal

- Each type of deployment has multiple profiles
- There are two other services worth mentioning when talking about IBM Cloud's Kubernetes service
    - The first is the container registry
        - This is used to store container images in a fully managed multi-tenant registry
        - It's highly available as the service is hosted and managed by IBM Cloud
        - You can configure your images to be privately accessed by other users in your IBM Cloud account shareable with API keys or even make them publicly available
        - Images in the container registry will also be scanned by the vulnerability advisor tool
        - The helm catalog is also unique to IBM Cloud and allows users to use helm to install and upgrade complex Kubernetes applications in a cluster
        - The helm catalog in IBM Cloud has access to IBM products, popular open source products, like Jenkins and Tecton, and supports multiple architectures like X86 power NZ

- So how does the IBM Kubernetes service work?
    - You first start off by logging into your IBM Cloud account
    - You select a region, you select a resource group, then you list or push images into a container registry with the IBM Cloud CR images command
    - You can list or create new Kubernetes clusters with the IBM Cloud KS command, and you can interact with your Kubernetes cluster with the kubectl Command
<br>

## Hands-on Lab: (Optional) Deploy an Application to Kubernetes

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Spin up a free cluster of the Kubernetes service
    - Manage and connect to your cluster using the IBM Cloud CLI
    - Run kubectl commands from the IBM Cloud Shell

![image](https://user-images.githubusercontent.com/29455975/185631162-a837c9d8-5967-452a-ba35-e08e88f6220f.png)
<br>



## OpenShift

- OpenShift is based on the open source OKD Project.
    - OKD is the community distribution of Kubernetes that Powers OpenShift.
    - OpenShift is a layer that's built on top of Kubernetes
    - OpenShift makes a lot of the difficult tasks like deploying applications and doing day-to-day administrative operations easier by extending Kubernetes in an opinionated way
    - OpenShift like Kubernetes is also deployable on premises or in a cloud and with the exception of OKD, OpenShift benefits from enhanced security from being run on RHEL

- Let's compare Kubernetes and OpenShift side-by-side
    - With Kubernetes you have just the core framework
    - With OpenShift, you have that same core Kubernetes framework, but all of OpenShift's abstractions
    - With Kubernetes, the platform or user, is responsible for integrating beyond the core framework
    - And with OpenShift opinions, an integration of common features are included

- So how does OpenShift extend Kubernetes?
    - The first is it provides an integrated Container Registry
    - It has a powerful integrated console that improve the experience for developers and operators
    - OpenShift takes the Kubernetes namespace concept and extends it with projects, allowing you to control access between who can access namespaces or projects
    - OpenShift greatly simplifies developer workflow with source to image and routes
    - Lastly, system administrators can use built-in monitoring tools like Grafana and Prometheus
    - IBM Cloud offers a highly available, fully managed OpenShift offering
    - In a matter of minutes, you can spin up your own OpenShift cluster and start deploying applications, allowing developers to focus on creating applications, not managing infrastructure

- Red Hat OpenShift on IBM Cloud has many other benefits
    - It has automated upgrades and patching
    - It's secure
    - Like its Kubernetes counterpart, has broad industry compliance, including HIPAA, PCI, and SOC1, and more
    - You can configure cluster as a single or multi zone cluster
    - There's integration with LogDNA insisting and at the time of this recording there are multiple versions available

- The only difference here is that there is no free tier option

- OpenShift 4 brought in many new features
    - The operator framework
        - OpenShift 4 was re-architected around operators
        - Operators enable developers to Automate the management of components like databases in a consistent, repeatable, scalable way
    - The OpenShift Service Mesh
        - OpenShift 4 saw the inclusion of OpenShift Service Mesh, which is based on STO
        - With Red Hat on IBM Cloud, you can install a Service Mesh on your cluster in just a few clicks
    - OpenShift Serverless Computing
        - OpenShift 4 saw the inclusion of OpenShift Serverless Computing, which is based on K native
        - Just like the server mesh component, you can install a Service Mesh on your cluster in just a few clicks
    - OpenShift pipelines cloud native CI CD pipelines were introduced in OpenShift 4
        - These are based on detect an open source project and code ready workspaces built on the Eclipse Che Open Source Project
        - Red Hat Code ready workspaces uses Kubernetes and containers to provide a user with a consistent and secure development environment

- With OpenShift’s rise in popularity, it has become available in many different platforms
    - IBM based platforms such as IBM Cloud as well as IBM Z and Power
    - Other major cloud providers such as AWS, Azure, and GCP also provide OpenShift
    - You can deploy OpenShift to Red Hat OpenStack or virtualization platforms
    - You can also deploy to VMware vSphere or on another bare metal server
    - Two things to point out code ready containers will spin up a minimal cluster on a local machine, which is ideal for a dev and test purposes
    - And the OpenShift playground is available online with no sign up required
    - It's great for experimenting, but only available for 60 minutes up next
<br>

## Cloud Foundry

- Cloud Foundry is an example of a Platform as a Service offering or PaaS
    - With Paas offerings, such as Cloud Foundry, you don't have to worry about the underlying infrastructure like runtimes, operating systems or servers
    - It enables you to focus exclusively on your application, code and data
    - Another major benefit of using the PaaS model is that deploying applications and services is typically a matter of minutes, not hours or days

- So, what is Cloud Foundry?
    - First off, it's open source
    - Cloud Foundry is an open source project that had its initial release in 2011
    - In 2015, the project was transferred to the newly created Cloud Foundry Foundation
    - The source code for Cloud Foundry is under an Apache license

- Deployment automation
    - Cloud Foundry has a container-based architecture that runs apps in any programming language
    - You can deploy apps to Cloud Foundry using existing tools with zero modification to the code
- Flexible infrastructure
    - By decoupling applications from infrastructure, you can make individual decisions about where to host workloads on premise, in public clouds or in managed infrastructure
- Commercial options
    - Cloud Foundry is container-based architecture runs apps in the most popular programminglanguages
    - An on the choice of your cloud infrastructure IBM Cloud, AWS, Azure, GCP and more
- Lastly, we have community support
A broad community contributes to and supports Cloud Foundry
Over 3,500 contributors 12,000 Slack participants and 850 meetups worldwide
Currently, when you deploy with Cloud Foundry on IBM Cloud, you'll get a fully managed multi-tenant environment
There are three ways to deploy your Cloud Foundry application on IBM Cloud
The first is to add a toolchain that includes the IBM Cloud continuous delivery service to your application
Alternatively, you can deploy from the application level console
You can view logs, setup environment variables, raise and lower the instances memory, and even scale your application by creating multiple instances
Lastly, you'll be able to bind to other IBM services automatically
Runtimes link IBM Cloud services to applications as endpoints, giving any instance of an application embedded knowledge of how to manage relevant calls and data
There are many benefits to using Cloud Foundry on IBM Cloud
These include access control
You can set up fine grain assignment of compute capacity to development teams with IBM Cloud IAM policies
- Health management
    - Applications that are crashing will automatically try to restart
- Automatic routing
    - Publicly reachable URLs are automatically created for your applications
- It's also Lite tier compatible
    - No credit card required
- The Lite tier limit has a memory of 256 megabytes of application runtime
    - This is good enough for most weekend projects
    - There are many Cloud Foundry runtimes that are supported on IBM Cloud
    - This includes Java, node.js, Python, Go, Swift, PHP.net, Tomcat ,and Ruby
<br>

## Cloud Functions
- What is serverless?
    - Serverless computing refers to the concept of building and running applications that well, do not require server management
    - It describes a finer grade deployment model where applications bundled as one or more functions are uploaded to a platform and then executed, scaled, and built in one response to the exact demand needed at the moment
    - With serverless technology, you pay only for code execution
    - This means that you will be able to see considerable cost savings relative to other technologies,like VM's or containers which are likely not being used 100% of the time

- Cloud functions are a Functions as a Service offering that enable developers to build serverless applications
    - The developer only has to focus on their application
    - This can further simplify the process of deploying code into production

- IBM Cloud functions is a Functions as a Service programming platform based on the open source project Apache OpenWhisk
    - It has an integrated API gateway
    - An API gateway is a component of cloud functions to expose API's
    - It comes with security, oauth support, rate limiting and custom domain support
    - IBM Cloud functions also supports open API, previously known as swagger

- Cloud functions have built in integrations with other IBM Cloud services such as AI, databases, object storage
    - It also has support for external providers such as GitHub and GitLab
    - IBM Cloud functions offer up to 5 million free executions per month
    - There is logging in monitoring through the IBM Cloud Console

- When talking about cloud functions, we have to talk about actions, triggers, and sequences
    - Actions are the building blocks of your serverless architecture
        - They contain the code performing the work and can be invoked via a rest API or trigger
    - Triggers receive events from outside IBM Cloud functions and invoke all connected actions
        - A webhook for a GitHub repository would be an example of a trigger
    - Sequences invoke multiple actions in linear order
        - This makes it possible to pass parameters from one function to the next

- There are several common use cases in Serverless Architectures, let's go over some of them Serverless APIs
    - You can expose application logic by implementing serverless microservices
    - Map your functions to well defined API endpoints that a user can call by making use of the API gateway integration
    - ETL workloads
    - Execute code whenever data is updated in a data store
    - This can be data at rest, like in a database or data in motion, such as a message queue or streaming data
    - The last one is alarm driven
        - You can execute your functions periodically
        - Think like a batch job or a Cron job
        - Periodic intervals so that they can run every few hours or at a specific time or date, either one time or repeatedly
    - Cloud functions on IBM Cloud support many different runtimes
        - You have the option of choosing from Java, Node, Python, Go, Swift, PHP, Ruby or any other language or framework by leveraging containers
<br>

## Module Summary
- We performed an overview of the IBM Cloud platform
- We covered IBM Cloud at a high level, locations and regions, account types and support plans, billing and usage, the cost estimator tool, and identity and access management
<br>

[Go to Next Module](./4_Services_on_IBM_Cloud.md)