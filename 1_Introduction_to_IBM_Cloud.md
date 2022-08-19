[Back to Syllabus](/READMEmd#course-syllabus)

## Learning Objectives

- Location of IBM Cloud Datacenters
- Account Type and Support Plans
- Billing and Usage
- The Cost Estimator
- Identity and Access Management
- IBM Cloud Console
- IBM Cloud CLI
- IBM Cloud Shell
<br>

## High Level Overview
- IBM Cloud has:
  - Over 200 services
  - 60 data centers worldwide
  - 47 of 50 Fortune companies

- Inside the IBM Cloud platform there is some layer that connect to each other
- Two main parts:
  - Console, identity and access management and catalog of products
  - Search and tagging resources, provisioning layer that allocate the resources and billing for unified account management and usage reports
- The IBM Cloud console is a dashboard for managing all the resources in your account
- The IBM Cloud CLI is a CLI supported by Mac, Linux and Windows, is extendable with plug-ins
- There is also the IBM Cloud Shell inside the dashboard
- To interact with services of IBM Cloud services there are API and SDK
- IBM Cloud have the best-in-industry security standard
<br>

## Locations and Regions
- IBM Cloud can deploy workloads in over:
  - 6 regions
  - 18 availability zones
  - 60 data centers

- The six IBM Cloud regions are:
  - Dallas
  - Washington DC
  - London
  - Frankfurt
  - Tokyo
  - Sydney

- In a single zone cluster your resources remain in the zone in which the cluster is deployed
- In IBM cloud, there is also the concept of a multi-zone region, a multi-zone region has three or more data centers within 6 miles of each other
- These data centers are located in close proximity to ensure high availability and resiliency
- So, essentially with a multi zone you have multiple places where you're deploying these servers and you're going to have more availability
<br>

## Account Types and Support Plans
- IBM Cloud has three main types of accounts:
  - Lite: free of charge
  - Pay-as-You-Go: access all IBM Cloud services
  - Subscription: enterprise customers

- Benefits
  - Lite: access to over 40 services like cloud object storage and cloud databases
  - Pay-as-You-Go: account are access to all services in the catalog, access to
    basic support, and it is fit for production use cases
  - Subscription: offers discounted pricing for services and support

- IBM Cloud support levels come in three forms:
  - Basic, which has access to create cases or tickets and can talk with support via phone or chat
  - Advanced, which guarantees a response time of 1 to 8 hours based on the severity of your ticket  
  - Premium, which guarantees a response time of 15 minutes to two hours and a
    technical account manager is assigned to your account for quarterly reviews
    
- Next, we'll take a deeper look into support and we'll show you how to create a ticket
  - In the account settings tab is where you can see your account type and then your ID
  - Click on support from the upper tab
  - In the support center, you can see your support plan
- Next, let's go ahead and create a case
  - Here, you can click on the services that you have provisioned and then click on the one service that you want to create a case for
  - Next, in the created case, you can give a subject line and then a description and then provide any screenshots to help you provide more details about the case
  - Lastly, you want to hit continue and that's how you create a case
<br>

## Billing and Usage
- Billing and usage enables you to view detailed information about your IBM Cloud spending
- You can view billing by getting a monthly overview or you can view it by specific service, and you can also export your usage as a CSV file
- Next, we will take an in-depth look at billing and usage through a demo with the IBM Cloud Console
- So firstly, let's go into billing
  - So, we can click on this manage tab at the top and we can click on billing and usage
  - This will take us to the billing landing page and where we can quickly change our payments or uses and then see more things, such as order subscriptions and quotes
- So, let's click on usage
- Next, we can quickly add a promotion or a promo code
  - if we click on the promotions tab in the left-hand side
  - You can click apply here to add promo code
- If we want to click and create a spending notification, we’ll just go on spending notifications in the left-hand side and we can click on enable here and then add in your email address and then click a threshold
<br>

## Cost Estimator
- The cost estimator tool does exactly what its name suggests, it estimates the cost of an IBM Cloud service before you create the service
- The tool is supported by all IBM Cloud services ranging from AI Services to infrastructure, services and Kubernetes clusters
- You can download your estimate as a PDF and you can calculate your estimate in over 15 currencies
- Next, let's go ahead and click on virtual server and then we'll add that to the list of products that we want to estimate
  - So, you can see, here, we're going to click on public, and then we're going to click on hourly billing and the North America South location, and then we'll click on a specific image such as the CentOS
  - We can add that to our estimate, note that then we'll be keeping track of multiple products to our cost
  - Next, we'll click a monthly usage as well, so we'll say that we want to rent this instance for a full month
  - And we're ready to download, so now we can export our cost estimate and send it to anybody across the team
<br>

## Hands-on Lab: Use the Cost Estimator Tool

- Navigate to [link](https://cloud.ibm.com/catalog) to launch the IBM Cloud Catalog
    - Add a quote
    - Review estimate
    - Download the PDF
![image](https://user-images.githubusercontent.com/29455975/185594127-ba741651-c8c6-4d39-9c51-57d88bc325d3.png)
<br>

## IAM
- In IBM Cloud, IAM is comprised of four concepts:
  - Users: these are the people that log in and use the account
  - Access groups: this is a way of grouping users together
  - Resources: a provision service offering selected from the catalog
  - Resource groups: a way of grouping resources together
- At the very highest level of IAM in IBM Cloud, we have an account
  - An account is comprised of many users
  - Each user has an email address that they use to log into IBM Cloud with
  - In each account there is an account owner
- In practice, for most enterprises this is usually a shared enterprise email that multiple
people can access should someone leave their job
- Difference between a service and a resource
  - A service is an entry from the IBM Cloud catalog, like a virtual machine or object storage or
one of the many other offerings
  - A resource is an instance of a service
- For example, in the IBM Cloud catalog, there's a database service called Cloudant
  - We can provision two instances of this service and called them DB-Dev and DV-prod
  - These would be our resources
- A user represents an IBM ID enabled account
  - Users are invited to join accounts which can be done through the console, IBM Cloud CLI or API
  - Users can create API keys to use with the CLI as an alternative to passwords for authentication
  - Users are given a role for the platform when invited, and these roles range from read-only viewer role to the administrator role, which can invite other users and view billing information
- Access groups are a collection of users
  - For instance, you may decide to group your users into access groups such as admins, billing, and basic users
  - Access groups help enable a cleaner separation of control, and it's worth noting that users can be part of multiple access groups at the same time
  - Resources have an automatically generated service ID, and they can be deployed to specific regions
- Resources have roles that can limit user access for that resource
  - For example, with cloud object storage, a user with the reader role could list and download objects in buckets
  - A user with a writer role could create and destroy buckets and a user with a manager role could control all aspects of data storage, like adding a retention policy and bucket firewall
- Resource groups are a collection of IBM Cloud resources
  - By grouping resources together, you can more easily provide access to multiple resources at once
  - Resource groups are specified at service creation time
  - A resource’s resource group cannot be changed
  - Resource groups have no geographical restrictions: this means you can put resources from Dallas and resources from Sydney in the same group,bringing it all together is the concept of an access policy
  - An access policy is the combination of a subject, which is a user or an access group, their role and a target, a resource or resource group



- Today, I want to show you a little bit of how to create an API key and how to authenticate yourself in a terminal or command line interface with your API key and then also I want to show you how to create and invite users to your account, and then give them certain permissions over services and other resource groups
  - From the manage tab in the top tab of IBM Cloud, you can click on access or IAM, we're going to go into the left sidebar, and we'll click on API keys
  - I'm just going to create a new one and I'll call it test and, great, we can see that the API key has been successfully created We can copy it and download it, which is always a good idea
  - Now that we're in my terminal, we can authenticate into IBM Cloud
  - So, we can do IBM Cloud login, dash dash API key, and then I'll just do paste, and I'll paste in my API key and in a couple of seconds you should see that you're authenticated and you can check all the resource groups
  - Great, so again you can see that we've authenticated, and we've seen all my instances in my account

- Alright, so now we've seen a little bit about API keys and now let's go ahead and talk a little bit about users and access groups
  - So, let's go ahead and click on users from the left-hand side bar, here we have all the account users that we have on this particular account, and I will be able to go ahead and click on invite users
  - So, here, we can already see that we can add users to access groups, these are things that have already been set up so we can actually create access groups to group all of these new users that come into this account into specific buckets
  - So, one of the buckets that we can group them into is the admin bucket, you can see that they have this number 129 is the actual actions for this role
  - So, they have a lot of user management actions so they can add other users
  - They can do a lot of the administrative features within this account 
  - Then there's also billing, so billing is able is actually working with finance to pay the bills

- So, let's talk a little bit about assigning users
  - Depending on your level of access, you can assign that same level of access or less to a new user
  - So, let's go ahead and click on the classic infrastructure and go to the devices
  - So, this is where you can see all the different specifications and permissions and actions for a specific device
  -With the Super user, of course, you could upgrade the server and view the software passwords, etc

- Now let's go ahead and talk about the IAM services
  - We can click all IAM services or we can go ahead and click on a specific service
  - So, we have cloud object storage, and we'll go cloudant in our account and we can give them access to only one region again so we can do Dallas or Frankfurt
  - We can click on Dallas and then all we do is we actually specify the service instance here and then we can give them editor access and then writer access 
  - So, and then let's do a test at Gmail and then all you do is add this and then you can see for this Cloud IAM services we've given them editor and writer access

- So, that's a little bit about IAM and that's how you would assign users additional access

<br>

## Hands-on Lab: Using the Catalog and Cloud Shell

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database
    - Launch the IBM Cloud Shell
    - Use the IBM Cloud CLI

<br>

[Go to Next Module](./2_Infrastructure.md)
