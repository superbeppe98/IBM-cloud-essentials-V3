[Back to Syllabus](/READMEmd#course-syllabus)

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
    
- Up next, we have a quick demonstration of how to spin up a IBM Cloud Kubernetes service, access it, and deploy a sample application
    - The first thing we need to do to get started with Kubernetes on IBM Cloud is to spin up a cluster
    - You can see you can flip through the bare metal and virtual shared and virtual dedicated offerings
    - Clicking on the overview and the worker nodes you can see details about your cluster
    - Clicking add ons, you can see the different channels that you can install, like STNK native
    - Alright, let's run an application
    - I've downloaded a simple hello world node application here and we've logged into our IBM Cloud account
    - We're going to set the Kubernetes context to be specific to the new cluster that we just set up here and now we're going to run the CR commands, which are to log into the container registry, cause we're going to be storing our containerized application in the IBM Cloud container registry
    - We can see the kubectl commands are already working
    - We can do get pods, get nodes, and we have information about our cluster
    - Let's take a look at our container registry
    - We've already run some of these commands, but let's go ahead and create a new name space to store our images, let's call it samples
    - Build our code locally with Docker Build and we're going to tag it and upload it to the IBM Cloud container registry
    - You can see the new samples namespace is being created here
    - We have some deployment and service YAML files
    - These are going to set the ports that are required and the image location
    - Let's go ahead and apply these YAML files
    - Let's issue a rollout command stating their application has been rolled out
    - Let's find our external IP by running the get services command
    - Before we view the applications, take a look at the embedded Kubernetes dashboard that's available
    - See here, we have one deployment, one pod, and going to the external IP, we can see our hello world application running

    - Alright, what if we want to make an update to this?
    - What if we want version two?
        - Well, first thing we need to do is update the code and we need to rebuild our image and push it into the IBM Cloud container registry.
        - Refreshing the container registry, we'll see that we now have two images in our namespace.
        - And we're also going to update one of the configuration file to point to the latest version of our image.
        - Let's reapply our YAML files and let's run that rollout command again.
        - Refreshing our external IP, we can see we are now running version 2, just that easy.
        - We can scale our containerized application to three deployments or three replicas.
<br>

## Hands-on Lab: (Optional) Deploy an Application to Kubernetes

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Spin up a free cluster of the Kubernetes service
    - Manage and connect to your cluster using the IBM Cloud CLI
    - Run kubectl commands from the IBM Cloud Shell

<br>



## Hands-on Lab: Using the Catalog and Cloud Shell

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database
    - Launch the IBM Cloud Shell
    - Use the IBM Cloud CLI

<br>

[Go to Next Module](./4_Services_on_IBM_Cloud.md)
