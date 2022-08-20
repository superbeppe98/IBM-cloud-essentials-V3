[Back to Syllabus](/READMEmd#course-syllabus)

## Learning Objectives

- Databases
- Integration
- Artificial Intelligence
- Analytics
- DevOps
- Blockchain
- Internet of Things
- Cloud Paks
<br>

## Databases
- A database is an organized collection of data stored on a computer
    - Traditionally, this was done via rows and columns as commonly seen in the relational or SQL database
    - Now, databases have evolved into storing information in ways that do not depend on SQL which are commonly referred to as NoSQL
    - Databases are used for a variety of use cases, ranging from storing personal or employee information, transaction history or customer data
    - You'll see them in just about any application you're using

- First, we have a relational database, which is an example of a SQL database
    - A relational database is a collection of data organized into a table structure, organized into rows and columns
    - Structured query language, SQL is typically the standard programming language used to update and query the database
    - Relational databases are also great for asset compliance and high transaction applications such as online transaction processing
- Next, we have document databases
    - Databases have flexible schemas
    - They're best suited to store semi structured data and it can handle dynamic querying
    - Some common use cases for document stores include customer data, user generated content, and order data
- Lastly, we have a key value database
    - Another example of a non-SQL database
    - A key value database is a non-relational database that stores data as a collection of key value pairs in which a key serves as a unique identifier
    - Common use cases for these types of databases are leaderboards, caches, and shopping cart data

- Database as a service is a cloud computing service that lets users access and use a cloud database system without purchasing and setting up their own hardware, installing their own database software, or managing the database themselves
    - Database as a service or DBaaS offers your organization significant financial, operational and strategic benefits
    - First, we have simpler, less costly management
    - With database as a service,the cloud provider manages everything
    - Although you can choose to manage certain aspects yourself if you wish
    - Scalability, you can quickly and easily provision additional storage and computing capacity at runtime if you need it, and you can scale down your database cluster during non-peak usage times to save cost
    - And you have rapid development and faster time to market
    - With DBaaS, developers can help themselves to database capabilities and spin up and configure a database that's ready to integrate with their application in minutes

- IBM Cloud has a few different options in terms of relational databases
    - Db2, a fully hosted, highly performant relational data store running the enterprise class Db2 database engine
        - We also have Db2 hosted which lets you run Db2 with full administrative access on cloud infrastructure
    - Then we have my SQL, one of the most popular databases
        - It is free an under the GNU General Public License and also Postgres
    - Postgres is an open source object relational database with over 30 years of history

- Next, let's talk a little bit about document databases on IBM Cloud
    - First, we have MongoDB, which is the most popular document database and is available as a managed service on IBM Cloud
    - It features a flexible data model, high availability, automated backup orchestration, auto scaling and coupled allocation of storage RAM, and vCPUs and is HIPAA compliant

- Next, we have clouded, which is IBM's database as a service based on Apache's CouchDB
    - It has a 99.99% service level agreement

- Next, we have Elasticsearch which is IBM Cloud's enterprise-ready fully managed solution for JSON document indexing and full text search capabilities

- Next, we'll talk about the key value databases on IBM Cloud
- We have two options for that
    - First is Redis, which is an open source in memory data structure store, used as a database, cache, and message broker
    - Next, we have etcd, which is an object relational database management system with an emphasis on extensibility and on standards compliance
<br>

## Hands-on Lab: Get to Know Cloudant
- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database service
    - Create a database in with your Cloudant service
    - Create a document within your database
    - Query your database using the Cloudant Console
![image](https://user-images.githubusercontent.com/29455975/185653877-14a299d3-6b8a-47d5-9afc-674c0d0e4815.png)

<br>

## Integration
- Integration provides connectivity, routing, and transformation for different services
    - It enables sharing of data, connecting applications, and security
    - IBM Cloud has several services that enable integration, each of which have a free or Lite tier plan
    - API connect which provides API creation and management with security rich features and centralized governance
    - App connect which allows you to connect your applications, automate tasks with hundreds of built-in connectors
    - Event streams, which is a high throughput message bus built with Apache Kafka
    - MQ which provides enterprise grade messaging

- Let's take a look at each in more detail
    - API connect is a comprehensive end to end API lifecycle solution that enables the automated creation of APIs
    - It also has other features to assist in API lifecycle management, such as being able to rapidly generate swagger compliant API's from back end data sources, graphically assembling the API invocation flow and applying access control policies, being able to share, publish and manage description of APIs through a self-service portal, and viewing analytics and data about your APIs
    - App connect is used to connect different applications and have event trigger actions between the applications
        - For example, in the screenshot below you can see that app connect is being called when you sales first contact is created, which triggers a nuro in a Google Sheets file which then sends a message to a specific Slack channel and then creates a task in Insightly
        - Using app connect you can automate your workflow, integrate your data and apps with over 75 connectors, use any of the 50 plus templates to quickly get started an create, and expose flows as rest API's to help developers build applications quickly
    - IBM event streams is a high throughput message bus built with Apache Kafka
    - It features a fully managed Apache Kafka Service, which is built with the open source Apache Kafka project
        - It's also highly available and resilient
        - It leverages the availability zone support from IBM Kubernetes service to ensure that in the unlikely event of an entire zone being unavailable, your applications will continue to work uninterrupted
        - It also has an intuitive user experience
        - And it also has an event driven architecture
        - It integrates with services such as the Watson IoT platform and IBM Cloud functions to make it easy to leverage event streams as the critical component of your event driven architecture
    - IBM MQ provides proven enterprise grade messaging capabilities such as point to point and publish subscribe models to facilitate the flow of information in the form of messages between applications
        - It has a managed messaging service
        - It also enables you to extend your enterprise messaging to the cloud
        - You can connect new cloud-based apps to your core business systems by integrating with your existing on Prem MQ Network.
        - You can quickly provision messaging capability in the cloud of your choice
        - You can use it both on IBM Cloud AWS and you can manage your way
        - You could either use the MQ Explorer, the MQ console, or script commands
<br>

## Artificial Intelligence
- Data science is a method for gleaning insights from structured and unstructured data using analytics and machine learning
    - Data is key here
    - Data science excels when there is a massive amount of data to analyze

- What kind of problems can data science solve?
    - There are plenty of use cases across many industries such as: Healthcare - uncover insights from clinical trials and patient data
        - Banking - give on the spot answers to loan applications
        - Education -support personalized planning tracking and data informed advisors
    - These are all dealing with large amounts of data
    - Good data quality is essential to solving these use cases, but about 80% of a data science’s time is spent on finding, cleaning, and organizing data
    - Once we have good data will be able to build models that can predict and forecast trends

- What is artificial intelligence?
    - AI is a huge field with many different domains
- What do they all have in common?
    - You can decently predict things if your model is good enough
- How do you make an affective model though?
    - It all comes down to the data you use to train that model

- To understand speech and language, we have tons and tons of data available through books, videos, and other documents
    - Once we have that data, how do we create the model?
    - This is where an iframe workers come into play
    - These are incredibly popular frameworks that are flexible and powerful
    - The biggest hurdle is the understanding of data science and AI principles to be able to effectively use these frameworks
    - All of these frameworks, such as TensorFlow, Scikit Learn, and PyTorch are open source and have their various advantages and disadvantages

- Now, let's talk about some of the AI services available on IBM Cloud
    - First, we have the AI Lifecycle management tools such as Watson Studio, Watson Machine Learning, Watson OpenScale, and knowledge  catalog
    - Next, we have tools, which analyze text such as Natural Language Understanding and tone analyzer
    - We then have intelligent search called discovery
    - We have a service, which enables you to build custom models for discovery and for Natural Language Understanding and that's called knowledge studio
    - We also have our speech and language services such as speech to text, text to speech, language translator, and assistant

- Let's take a look at the AI Lifecycle management tools
    - These tools will help you build and scale AI with trust and transparency by automating AI Lifecycle management
        - Watson Studio provides a suite of tools and a collaborative environment for data scientists, developers, and domain experts
        - Watson machine learning lets you run and deploy machine learning models anywhere across any cloud
        - Watson knowledge catalog lets you discover, curate, categorize, and share data assets and models with access control
        - Watson OpenScale lets you measure and manage AI models in production to promote trust and confidence
        - Watson Natural Language Understanding uses deep learning to extract metadata from text, such as enemies, keywords, categories, sentiment, emotion, relation, and syntax
        - Watson tone analyzer uses linguistic analysis to identify tones such as anger, disgust, fear, joy, and sadness
    - It could also detect social propensities such as extraversion and language styles such as analytical, confident or tentative from text

- Now, let's take a look at Watson Assistant one of the most popular Watson services
    - Watson Assistant lets you build conversational interfaces into any application device or channel
        - It has an easy to use UI
        - It has a plug-in for Slack and other applications
        - It also has a catalog of entities for industries so that you can quickly get started with some of the most frequently asked questions over chat
        - You can also quickly integrate with Twilio, Salesforce, Zendesk, and voice agents as well
    - Watson Discovery is an intelligent search service that will deliver specific answers to your questions while also serving up the entire document for exploration
        - Watson Discovery can be trained with entire documents and you can use Watson Knowledge Studio to build a custom model to train Watson Discovery with unique relationships and entities
        - In this example, we trained Discovery with the car service manual to look for information about what kind of engine oil to use
        - With Discovery on the left-hand side, we are linked to the correct section and relevant information is highlighted
        - We also have a confidence score as well

- Now, let's take a look at the speech and language services that are offered on IBM Cloud
    - First, we have speech to text, which is a service that transforms voice into written text
    - Next, we have text to speech, which enables you to convert written text into natural sounding audio in a variety of languages and voices
    - Also, we have language translator, which can dynamically translate news, patents, or conversational documents from over 20 languages and can identify up to 68 languages
    - Natural language classifier allows you to assign custom categories to input a text
<br>

## Hands-on Lab: Get to Know Watson Discovery
- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Watson Discovery service
    - Interact with the Watson Discovery interface
    - Run queries with Watson Discovery

![image](https://user-images.githubusercontent.com/29455975/185654570-19ee602f-ab7e-49d3-b067-77b8350da304.png)
<br>

## Analytics
- Data analytics is the science of analyzing raw data in order to make conclusions about that information
    - Any type of information can be subjected to data analytics techniques to get insight that can be used to improve things

- Let's talk about a few different types of Analytics and understand how they enable us to make better decisions
    - Descriptive analytics looks at past performance and understands that performance by mining historical data to look for the reasons behind past success or failure
    - Diagnostic analytics examines data or content to answer the question, why did this happen?
    - It is characterized by techniques such as drilldown, data discovery, data mining, and correlations
    - Predictive analytics encompasses a variety of statistical techniques from data mining, predictive modeling, and machine learning that analyze current and historical factsto make predictions about future or otherwise unknown events
    - Prescriptive analytics takes advantage of the results of Descriptive and predictive analytics and suggests a decision

- Spark is a unified analytics engine for big data processing with built in modules for streaming, SQL, machine learning and graph processing.
    - It is an open source project with 750 contributors from 200 organizations
    - Hadoop is a framework that allows for a distributed processing of large data sets across clusters of computers using simple programming models
    - Like Spark, it is also open source
    - Hadoop uses the MapReduce programming model for parallel processing of large volumes of data in a distributed environment

- There are five main analytics services on IBM Cloud
    - We have analytics engine, streaming analytics, DB2 warehouse, Cognos dashboard, and information server

- Let's dive a bit deeper into each one
    - Analytics engine lets you deploy and develop applications using open source Apache Spark and Apache Hadoop
    - It also has on-demand scalability and is HIPAA ready for the Dallas region
    - It also gives you the ability to customize the environment with third party analytics libraries and packages
    - The streaming analytics service is used to ingest, analyze, monitor and correlate data in real time
    - It evaluates a broad range of streaming data from unstructured text, video, audio data to Geospatial and sensor data
    - It performs real time analysis on data in motion and it can connect with virtually any data source, whether unstructured, structured or streaming, and integrate with Hadoop and Spark
    - Lastly, it has built in Domain Analytics like machine learning, natural language, spatial temporal, text, acoustics and more to create adaptive stream applications

- Db2 warehouse is a fully managed elastic cloud data warehouse that delivers independent scaling of storage and compute and is built for machine learning
    - You can train and run models directly in the DB2 warehouse engine using SQL, Python and R
    - It is highly scalable, and you can easily manage and independently scale up, compute and storage
    - It is secure
    - You can control and monitor activity on your database with fine grained access control and database auditing capabilities
    - And it's also Oracle compatible
    - You can leverage Db2's Oracle capability to run your existing Oracle applications on Db2 warehouse

- The Cognos Dashboard Service lets you add end to end data visualizations to your application
    - The visualizations allow users to interact, for instance, they can drag and drop to quickly find valuable insights on their own
    - The visualizations have a live connection to the underlying data
    - Updates the data will be reflected in the visualizations in real time
    - You could also embed visualizations in your applications
    - Data can be explored using filters and navigation paths
    - The information server is a market leading data integration platform, which includes a family of products that enable you to understand, cleanse, monitor, transform, and deliver data, and to collaborate to bridge the gap between business and IT
    - The data stage tool allows you to create jobs that can extract, transform, and load data
    - The information governance catalog allows you to track data lineage
    - The information analyzer provides data profiling and analysis to accurately evaluate the content and structure of your data for consistency and quality
<br>

## DevOps
- What is DevOps?
    - DevOps is a set of practices that combine software development dev and it operations ops
    - It aims to shorten the development lifecycle by providing continuous deployment with high software quality via automated tests and delivery governance
    - Continuous integration, continuous delivery, and continuous deployment are key topics for DevOps

- Let's understand the differences between the three
    - Continuous integration is a form of automation testing which checks that the application is not broken whenever new commits are integrated into the main branch
    - Developers using continuous integration aimed to merge their changes back to the main branch as often as possible
    - Continuous delivery goes one step further than continuous integration in that you have an automated release process that merges your changes from the automated testing process and pushes them to a staging environment
    - Finally, continuous deployment goes one step further than continuous delivery and automates the process of pushing changes from the staging environment to the production environment
    - This enables new features and patches to reach your customer even faster

- The IBM Cloud DevOps services are a set of tools that support development, deployment, continuous delivery, and operational tasks
    - A DevOps toolchain is a set of tools and templates that automates the tasks of developing and deploying your application
    - It contains templates for building and deploying your project
    - It also supports integration with many third-party tools
    - The continuous delivery service automates the building and deployment of applications
    - The delivery pipeline is a part of the continuous delivery service
    - It allows developers to automate builds, unit tests, and deployments

- Here we see an example of using the DevOps approach with IBM Cloud tool chain
    - First, we have the thing phase in which we use GitLab to plan our Sprint tasks using issues
    - Next, we have the code phase in which we commit changes to our code from the Orion web IDE to our repository
        - Once the commit is pushed, the deliver phase starts automatically
        - In this phase, we delivered the latest version of our code to our staging and production environments using our delivery pipeline
    - Next, we have the run phase
        - In this phase our application is pushed to a Cloud Foundry service or Kubernetes service and we can see it running on IBM Cloud dashboard
    - Next, we have the learn phase
        - We use Google Analytics to gather data and feedback to incorporate into future releases
    - Last, we have the culture
        - Slack enables teams to communicate faster and more efficiently

- Here are some examples of tools which you can use to build your code in IBM Cloud toolchains: GitLab CE, GitHub, and Bitbucket
    - IBM Cloud toolchains offer a few different delivery options
    - First, we can deliver a docker application and its helm chart together in source control and have it built and deployed automatically to a Kubernetes cluster
        - Another option is that you can develop an application and deploy changes using a Razee agent in your Kubernetes cluster
    - Most of the toolchain templates have an option of using Tekton as your delivery pipeline, which is an open source Kubernetes native in framework for continuous delivery
    - In the run stage you can choose the target or where your application will be deployed
    - With Cloud Foundry, your application will be deployed as a Cloud Foundry application on IBM Cloud
    - You can also choose to run your applications on a Kubernetes cluster
        - As a more advanced option, you can choose to run your application on a virtual server of your choice
    - In the learn stage, you can gather data and feedback about your application to continuously improve and prioritize features in future releases

- Here are some of the integration the IBM Cloud tool chain support
    - We support New Relic, which provides an observe ability platform to ensure your stack is running as efficiently as possible
    - We support Google Analytics, which is an analytic software which helps monitor your website traffic and better understand your customers
    - Ans Sauce labs, a cloud-based platform which specializes in automated testing for web and mobile applications

- Then we have culture
    - In the culture stage, IBM Cloud toolchains provides tools to improve cross functional communication between teams
    - We have slack, which is a channel based searchable messaging platform PagerDuty, an incident response platform, and Jira, which is an issue tracking product developed by Atlas Ian that allows bug tracking, an agile project management
<br>

## Blockchain
- What is a blockchain?
    - A blockchain is a growing list of records, called blocks that are linked using cryptography
    - Each block contains a cryptographic hash of the previous block, timestamp, and transaction data
    - By design, A blockchain is resistant to modification of the data
    - Once recorded, the data in any given block cannot be altered retroactively without alteration of all subsequent blocks, which requires consensus of the network majority

- Let's talk about some key elements of a blockchain network
    - Blockchains are distributed permanent and record transaction between two parties
    - They are distributed
    - All network participants have access to the distributed Ledger and it's immutable record of transactions
    - They're also immutable
    - No participant can change or tamper with the transaction after it's been recorded to the shared Ledger, and they use smart contracts to speed transactions
    - A set of roles called Smart contracts is stored on the Blockchain and executed automatically

- What is hyperledger fabric?
    - Hyperledger fabric is an implementation of blockchain technology that is designed as the foundation for developing blockchain applications
    - It has an emphasis on ledger, mark objects, confidentiality, resiliency, and scalability
    - Due to popularity, hyperledger fabric has been adopted by major cloud providers including Alibaba, AWS, Azure, Google, IBM, and others
    - Hyperledger fabric is an Apache two licensed open source project with the founding codebase originally donated to the Linux Foundation by IBM and digital asset

- Let's take a deeper dive into smart contracts within hyperledger fabric
    - Smart contracts are required to create a blockchain application with hyperledger fabric
    - Fabric offers SDK's in node.js and Java and support for Python and Go is planned for later releases
    - Smart contracts are executed to change or read a value in the world state
    - hese smart contract executions are recorded as transactions within the blocks on the Blockchain
    - In this way, we have a tamper-proof history of all transactions which have happened on a particular blockchain network

- Let's talk a little bit about consensus
    - Consensus is the process by which nodes agree on the order of transactions
    - There are multiple ways of doing consensus, however you do it, the aim of consensus is to get from the before state on the left to the after state on the right
    - In this case, there are four nodes, two of which think that the world state is ABC
    - One mistakenly thinks it's DEF due to network latency and one is a malicious node who will do anything to convince you that the world state is XYZ
    - Consensus will get to a situation where all the good nodes agree that the world state is ABC and the bad node is just ignored
    - Consensus assumes that there is a sufficient portion of good actors on the network who are trustworthy
    - The value of Blockchain comes from participants sharing common smart contracts and agreeing on the source of truth
    - Since transactions are automated, participants can be assured money is received upon the agreement of their contract
    - Participants also have visibility into the history of a particular asset and how that ownership has changed overtime

- This is the IBM blockchain platform in a single chart
    - It's based on hyperledger fabric and runs on the IBM Cloud platform, although other options are available
    - IBM blockchain platform aims to help with the entire lifecycle of a blockchain solution from inception through the deployment and beyond
    - There are set of tools for the solution development as well as tools to allow clients to govern and operate blockchain business networks
    - IBM's key differentiators are advanced tooling for building, operating, and growing blockchain networks and the ability to deploy blockchain networks anywhere
<br>

## Internet of Things
- What is IoT?
    - IoT or Internet of Things is a system of interrelated computing devices that transfer data over a network without requiring human interaction

- There are many use cases for IoT, and here are three
    - We have predictive maintenance
        - Keeping assets up and running has the potential to significantly decrease operational expenditures,saving companies millions of dollars
    - Asset tracking
        - The goal of asset tracking is to allow an enterprise to easily locate and monitor key assets along the supply chain to optimize logistics, maintain inventory levels, prevent quality issues, and detect theft
    - Connected vehicles
        - These are computer enhanced vehicles that automate many normal driving tasks
        - In some cases even driving themselves

- IBM Cloud's Internet of Things platform or the IoT platform, lets you communicate with and consume data from connected devices and gateways using a builtin web console to monitor your IoT data and analyze it in real time
    - It has several features such as quickly and securely register and connect your devices and gateways
    - Information management
        - Control what happens to the data that is received from your connected devices
        - Manage data storage, configure data transformation actions, and integrate with other data services
    - Analyze in real time
        - Monitor real time device data through rules, analytics and dashboards
    - Risk and security management
        - Our secure by design control capabilities protect the integrity of your IoT solution through secure connectivity and access control for users and applications
    - The IBM Cloud IoT platform has a powerful dashboard that allows for viewing connected devices by device type, showing how much data has been transferred, monitoring real time sensor data, and Geo location data about your devices

- How does it work?
    - The IoT platform uses the following IoT device data flow
        - First, you must register your IoT device in the IoT platform
            - Your IoT devices send data using MQTT to the IoT platform, which acts as a message broker and writes data to cloudant IBM event streams and DB2 warehouse
        - Then the data set is also written to cloud object storage for long term storage
        - Lastly, analytics services are used to connect to the device, an external data sources to enable custom dashboards for business users
<br>

## Cloud Paks
- What are IBM Cloud Paks?
    - Cloud Paks are containerized software solutions built to run anywhere?
    - I like to think of it as a bundle of continuous software
    - The goal of the Cloud Pak is to make container management and application modernization easier for an organization
    - Cloud Paks come in a variety of use cases, which we'll explore later

- For now, let's look at the values of Cloud Paks
    - Cloud Paks have a modular architecture, meaning you can pick and choose which software you want to deploy
    - Cloud Paks put AI to work
    - They operationalize AI throughout your business
    - Cloud Paks are built on OpenShift, which allows them to run anywhere

- So, what do we mean by anywhere?
    - Cloud Paks can be run on any platform you choose
    - You can install them on IBM Cloud
    - You can install them on premise
    - Use your own hardware or with the Cloud Pak system, or you can install them on any cloud by first provisioning OpenShift and then installing Cloud Paks on top

- The six Cloud Paks that we will cover are applications, data, integration, automation, security, and multi-cloud management
    - The Cloud Pak for applications has tools to help you modernize existing applications and build new cloud native ones

- The four main capabilities are:
    - Accelerator' for cloud native development, which bring together open source technologies and put them in a microservices based framework
    - IBM modernization and developer tools
        - Modernization guidance gives you a plan to start strategically updating your applications
    - A Java EE platform is a collection of Java APIs that help you write secure, flexible server side applications
    - Mobile app development tools for building apps for mobile, wearables, conversation, web or progressive web apps

- Cloud Pak for data has the following features built in:
    - It has a single platform that integrates data management, data governance, and analysis
    - It has databases so you can spin up your favorite IBM or open source database
    - It has data governance built in, like automated discovery and classification of data, and masking of sensitive data
    - It also has data virtualization so you can query easily across multiple sources, on cloud or on premises
    - It has IBM Cloud AI services, such as Watson Assistant or Discovery
    - And it has AI model lifecycle tools, such as Jupyter or RStudio to create notebook, serve them with Watson Machine Learning, or automate the whole process with Auto AI

- Cloud Pak from Multi Cloud Management is an IT management platform designed to provide full visibility and control wherever your workloads run
    - Using the dashboard, you can monitor application lifecycle management so you can deploy and move application across clouds
    - It provides cloud protection and compliance with automated policy enforcement and compliance testing
    - It has built in SRE tooling with AI OPS to use event correlation and machine learning to improve operational efficiency and readiness
    - It also has many add-on capabilities from IBM partners such as Turbonomic, Sysdig, Humio, and Hazelcast..

- Cloud Pak for integration is a complete set of integration capabilities to efficiently connect your applications and data wherever they live
    - You can use API connect, app connect, MQ and event streams and you have the Aspera high speed data transfer so you can move data of any size around the world at maximum speed
    - IBM Cloud Pak for security is a platform that helps you uncover hidden threats
    - Make more informed risk-based decisions and prioritize your teams' time
    - It has core platform services such as threat, intelligence, insights, and data Explorer, and has integrations with existing tools and data such as Qradar and Splunk
    - The IBM Cloud Pak for automation provides applications in core areas where automation provides benefits, content, workflow, decisions, and capture cloud fact for automation
    - Provides low code consumable tools, API's and application connectors that make it easy to consume content in business applications
    - You can also automate your end to end workflow with IBM business automation workflow and you can use IBM operational decision manager to automate the implementation of business policies in your organization
<br>