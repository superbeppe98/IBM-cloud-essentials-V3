[Back to Syllabus](./README.md#course-syllabus)

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
-Inside the IBM Cloud platform there is some layer that connect to each other.
-Two main parts:
  - Console, identity and access management and catalog of products
  - Search and tagging resources, provisioning layer that allocate the resources and billing for unified account management and usage reports.
- The IBM Cloud console is a dashboard for managing all the resources in your account.
- The IBM Cloud CLI is a CLI supported by Mac, Linux and Windows, is extendable with plug-ins.
- There is also the IBM Cloud Shell inside the dashboard
- To interact with services of IBM Cloud services there are API and SDK.
- IBM Cloud have the best-in-industry security standard.
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
- In a single zone cluster your resources remain in the zone in which the cluster is deployed.
- In IBM cloud, there is also the concept of a multi-zone region, a multi-zone region has three or more data centers within 6 miles of each other.
- These data centers are located in close proximity to ensure high availability and resiliency.
- So, essentially with a multi zone you have multiple places where you're deploying these servers and you're going to have more availability.
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
    technical account manager is assigned to your account for quarterly reviews.

- Next, we'll take a deeper look into support and we'll show you how to create a ticket.
  - In the account settings tab is where you can see your account type and then your ID.
  - Click on support from the upper tab.
  - In the support center, you can see your support plan.
- Next, let's go ahead and create a case.
  - Here, you can click on the services that you have provisioned and then click on the one service that you want to create a case for.
  - Next, in the created case, you can give a subject line and then a description and then provide any screenshots to help you provide more details about the case.
  - Lastly, you want to hit continue and that's how you create a case.
<br>

## Billing and Usage
- Billing and usage enables you to view detailed information about your IBM Cloud spending.
- You can view billing by getting a monthly overview or you can view it by specific service, and you can also export your usage as a CSV file.
- Next, we will take an in-depth look at billing and usage through a demo with the IBM Cloud Console.

- So firstly, let's go into billing.
  - So, we can click on this manage tab at the top and we can click on billing and usage.
  - This will take us to the billing landing page and where we can quickly change our payments or uses and then see more things, such as order subscriptions and quotes.

- So, let's click on usage.
- Next, we can quickly add a promotion or a promo code
  - if we click on the promotions tab in the left-hand side.
  - You can click apply here to add promo code.

- If we want to click and create a spending notification, we’ll just go on spending notifications in the left-hand side and we can click on enable here and then add in your email address and then click a threshold.
<br>

## Cost Estimator
- The cost estimator tool does exactly what its name suggests, it estimates the cost of an IBM Cloud service before you create the service.
- The tool is supported by all IBM Cloud services ranging from AI Services to infrastructure, services and Kubernetes clusters.
- You can download your estimate as a PDF and you can calculate your estimate in over 15 currencies.

- Next, let's go ahead and click on virtual server and then we'll add that to the list of products that we want to estimate.
  - So, you can see, here, we're going to click on public, and then we're going to click on hourly billing and the North America South location, and then we'll click on a specific image such as the CentOS.
  - We can add that to our estimate, note that then we'll be keeping track of multiple products to our cost.
  - Next, we'll click a monthly usage as well, so we'll say that we want to rent this instance for a full month.
  - And we're ready to download, so now we can export our cost estimate and send it to anybody across the team.
<br>



[Go to Next Module](./2_Infrastructure.md)
