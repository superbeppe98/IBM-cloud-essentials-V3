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

- We're going to have a quick demonstration of spinning up an OpenShift cluster on IBM Cloud
    - Accessing it and deploying a sample application
    - Getting started with Red Hat OpenShift on IBM Cloud is similar to getting started with the Kubernetes service on IBM Cloud
    - Go to the cloud catalog, find the Red Hat OpenShift
    - Click it and start configuring your cluster
    - You see, the overview page looks very similar to that of the Kubernetes cluster from the previous lesson
    - We have our worker nodes, worker pools, and add ons
    - To truly get started with OpenShift, let's click on that OpenShift Web console link at the top right
    - Find your username on the top right and click login
    - Here you can find the OC command used to log into the cluster
    - Let's pop open a router and deploy the same application that we did in the previous lesson
        - We start by running the OC new project command
        - And we're going to create a new project called samples
        - Refreshing our console, we can see these samples project is now available
        - Let's run the OC new app command
        - We're going to point it to the Git repository
        - And you can see by going to the developer point of view you can see the topology
        - We've already got one deployment up and running
        - Let's run the OC exposed command
    - That'll give us a route
        - And running the OC get routes command will list all the routes available
        - Before we click on the open URL button, notice that the build is actually still running
        - Let's click on that build
        - You can see here it's actually generating a dockerfile automatically
        - It's not using the one that is built into the directory
        - This is leveraging source to image
        - It's going to automatically detect that node.js is being used and attempt to build an image from your source code
        - You can see that it's also pushing the image to OpenShift's internal registry
        - Now that the push is complete, let's click on our deployment
        - We can click on the pods that are associated with it, click on the logs there
        - We can see our application is up and running
        - Now let's click that open URL button
        - And there's our message
    - Going back to the topology and clicking the overview tab, we can scale up and create three replicas
        - There are many other actions you can take from the OpenShift Console
        - We're going to save that for a different course
        - From the administrative point of view, you can see the pods that are available
        - Let's wrap this up by deleting some of the artifacts that we had created
        - Here's our deployment config
        - Let's start deleting that
        - That'll automatically scale down our application and start deleting the pods
        - And refreshing our page will make it unavailable
    - To delete the cluster, we go back to the cluster overview page and go to the actions menu
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

- Up next, we have a quick demonstration of how to deploy a sample application on Cloud Foundry on IBM Cloud
    - To get started with Cloud Foundry, we're going to go to the Cloud Foundry overview page
    - You can see we have no applications or services running
    - I've pulled down some code here
    - It's our hello world application that we've been using in previous exercises
    - You can see a file manifest.YAML that is specific to Cloud Foundry
    - See, here we have the name, the build pack, and memory and instances
    - Now to get started, we're going to log into IBM Cloud
        - We're gonna run the CF push command
        - You can see our application is already registered on the console
        - It's still building, and we have some output there
        - Alright, we can see our memory is defaulted to 256 megabytes
         -We can increase that if we like
        - We can increase the number of instances
        - You can see the logs available here and clicking on the open URL
    - There we see our hello world message
    - We can edit the name
    - Increase the number of instances
    - And we can also stop our application
    - To delete it, simply go to the action menu and click delete
    - Remember to delete the route also
    - And there's a very basic example of deploying an application on Cloud Foundry
<br>

## Hands-on Lab: Deploy an Application to Cloud Foundry

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Spin up a free cluster of the Kubernetes service
    - Manage and connect to your cluster using the IBM Cloud CLI
    - Run kubectl commands from the IBM Cloud Shell
<br>

## Cloud Functions
What is serverless?
Serverless computing refers to the concept of building and running applications that
well, do not require server management.
It describes a finer grade deployment model where applications bundled as one or more
functions are uploaded to a platform and then executed, scaled, and built in one response
to the exact demand needed at the moment.
With serverless technology, you pay only for code execution.
This means that you will be able to see considerable cost savings relative to other technologies,like
VM's or containers which are likely not being used 100% of the time.
Throughout the course, we've explored several different deployment platforms to run your
workloads.
We started with bare metal virtual servers, made our way to containers, and now we're
at PaaS and Serverless.
Cloud functions are a Functions as a Service offering that enable developers to build serverless
applications.
The developer only has to focus on their application.
This can further simplify the process of deploying code into production.
IBM Cloud functions is a Functions as a Service programming platform based on the open source
project Apache OpenWhisk.
It has an integrated API gateway.
An API gateway is a component of cloud functions to expose API's.
It comes with security, oauth support, rate limiting and custom domain support.
IBM Cloud functions also supports open API, previously known as swagger.
Cloud functions have built in integrations with other IBM Cloud services such as AI,
databases, object storage.
It also has support for external providers such as GitHub and GitLab.
IBM Cloud functions offer up to 5 million free executions per month.
And lastly, there is logging in monitoring through the IBM Cloud Console.
When talking about cloud functions, we have to talk about actions, triggers, and sequences.
Actions are the building blocks of your serverless architecture.
They contain the code performing the work and can be invoked via a rest API or trigger.
Triggers receive events from outside IBM Cloud functions and invoke all connected actions.
A webhook for a GitHub repository would be an example of a trigger.
Sequences invoke multiple actions in linear order.
This makes it possible to pass parameters from one function to the next.
There are several common use cases in Serverless Architectures, let's go over some of them
Serverless APIs.
You can expose application logic by implementing serverless microservices.
Map your functions to well defined API endpoints that a user can call by making use of the
API gateway integration.
ETL workloads.
Execute code whenever data is updated in a data store.
This can be data at rest, like in a database or data in motion, such as a message queue
or streaming data.
The last one is alarm driven.
You can execute your functions periodically.
Think like a batch job or a Cron job.
Periodic intervals so that they can run every few hours or at a specific time or date, either
one time or repeatedly.
Cloud functions on IBM Cloud support many different runtimes.
You have the option of choosing from Java, Node, Python, Go, Swift, PHP, Ruby or any
other language or framework by leveraging containers.
Up next, we have a quick demonstration of using the cloud functions feature on IBM Cloud.
To start playing around with our cloud functions.
We're going to go to the cloud functions overview page.
And click on the start creating button.
You can see here we can create an action trigger or sequence to speed things up.
We're going to use a quick start template.
There are templates for a hello world application cloud and events, event streams, periodic
Slack reminder.
We're going to go ahead and use the get HTTP resource template.
You can see here that you can choose the different programming language that you'd like to use,
like Node or Python And it's going to give you a templated code.
Clicking create will create the action in your namespace.
Here, you can see the code.
You can edit the code and run it locally with the invoke button.
There you go.
Our location has been returned.
It says awesome.
That's exactly what we want.
Clicking on the parameters, you can set environment variables like API keys.
You can also view details about your runtime, like what programming language you're using
and what your time and memory limit are.
The endpoints is interesting over here, 'cause now you have a publicly accessible URL you
can use.
Clicking on that will actually run the application.
You can see it's actually returning the location as awesome.
That's exactly what we expect it to return.
Going back to our code, let's change it up a little bit.
Let's change the location from Austin to Toronto.
Save that change.
Refresh the page and there we go.
We have Toronto.
This has been a basic example of a serverless action.
Let's summarize what we've learned.
Serverless allows you to spend as much time as possible developing code.
Cloud functions on IBM Cloud are built on the open source project Openwhisk.
Cloud functions and IBM Cloud allow you to pay for only the time your code is executed.
Comes with many other benefits, like 5 million for executions.
Tight integration with other providers and an integrated API gateway.

<br>


[Go to Next Module](./4_Services_on_IBM_Cloud.md)
