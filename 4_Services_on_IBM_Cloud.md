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
Welcome to module 4.
My name is Horea Porutiu and I'll be your instructor for this module.
I'm very excited to talk more about module 4 because it covers some of the most popular
services in IBM Cloud.
We'll be covering necessities such as databases and then going into more emerging technologies
such as blockchain, IoT, and AI.
In this first video, we're going to talk about databases.
We're going to cover things such as the SQL database.
We'll talk about document databases and then key value databases.
And then we'll end with the database as a service offerings on IBM Cloud.
Let's get started.
Before we get into it, let's talk about what exactly is a database.
A database is an organized collection of data stored on a computer.
Traditionally, this was done via rows and columns as commonly seen in the relational
or SQL database.
Now, databases have evolved into storing information in ways that do not depend on SQL which are
commonly referred to as NoSQL.
Databases are used for a variety of use cases, ranging from storing personal or employee
information, transaction history or customer data.
You'll see them in just about any application you're using.
There are many types of databases, so we'll cover three types as they relate to services
available on IBM Cloud.
First, we have a relational database, which is an example of a SQL database.
A relational database is a collection of data organized into a table structure, organized
into rows and columns.
Structured query language, SQL is typically the standard programming language used to
update and query the database.
Relational databases are also great for asset compliance and high transaction applications
such as online transaction processing.
Next, we have document databases.
There an example of a non-SQL database document.
Databases have flexible schemas.
They're best suited to store semi structured data and it can handle dynamic querying.
Some common use cases for document stores include customer data, user generated content,
and order data.
Lastly, we have a key value database.
Another example of a non-SQL database.
A key value database is a non-relational database that stores data as a collection of key value
pairs in which a key serves as a unique identifier.
Common use cases for these types of databases are leaderboards, caches, and shopping cart
data
Database as a service is a cloud computing service that lets users access and use a cloud
database system without purchasing and setting up their own hardware, installing their own
database software, or managing the database themselves.
Database as a service or DBaaS offers your organization significant financial, operational
and strategic benefits.
First, we have simpler, less costly management.
With database as a service,the cloud provider manages everything.
Although you can choose to manage certain aspects yourself if you wish.
Scalability, you can quickly and easily provision additional storage and computing capacity
at runtime if you need it, and you can scale down your database cluster during non-peak
usage times to save cost.
And you have rapid development and faster time to market.
With DBaaS, developers can help themselves to database capabilities and spin up and configure
a database that's ready to integrate with their application in minutes.
IBM Cloud has a few different options in terms of relational databases.
Db2, a fully hosted, highly performant relational data store running the enterprise class Db2
database engine.
We also have Db2 hosted which lets you run Db2 with full administrative access on cloud
infrastructure.
Then we have my SQL, one of the most popular databases.
It is free an under the GNU General Public License and also Postgres.
Postgres is an open source object relational database with over 30 years of history.
Next, let's talk a little bit about document databases on IBM Cloud.
First, we have MongoDB, which is the most popular document database and is available
as a managed service on IBM Cloud.
It features a flexible data model, high availability, automated backup orchestration, auto scaling
and coupled allocation of storage RAM, and vCPUs and is HIPAA compliant.
Next, we have clouded, which is IBM's database as a service based on Apache's CouchDB.
It has a 99.99% service level agreement.
Next, we have Elasticsearch which is IBM Cloud's enterprise-ready fully managed solution for
JSON document indexing and full text search capabilities.
Next, we'll talk about the key value databases on IBM Cloud.
We have two options for that.
First is Reddis, which is an open source in memory data structure store, used as a database,
cache, and message broker.
Next, we have etcd, which is an object relational database management system with an emphasis
on extensibility and on standards compliance.
Next, we're going to go into a little bit more detail on using the cloudant database.
So, here, we're in our IBM Cloud and we've already provisioned a cloudant database service,
and we're here in the manage tab of that service.
You can see we have a button to launch the dashboard and we have our external endpoint
here.
So later in the video will be making a curl request to that external endpoint.
Now we've launched their dashboard and we see we've created a database here called demo
IBM Cloud essentials.
We can see that the number of docs is three and here, once we click that database, we
see our documents and currently they are shown in meta data format.
But we can change the table format and then we can go back to metadata and go into JSON.
So you can see these three documents.
Each document has a name, city, and professional key, and then it has different value associated
with that.
The first document has my name and my city.
The second document has Bob Simon, so it's a different person and it has their city and
profession, and the next document has Dana Porutiu you.
And then it has a different city and a profession.
So what we're going to be doing later on in the video is making a query to this database.
So now we're going to go ahead to our terminal and we're going to show you a sample query.
So, here is a JSON, which uses a selector to make a query.
So, this is what cloudant enables us to do.
So, for our selector we're looking for the name field.
And we're going to, we're looking for Horea Porutiu specifically.
So, we should be able to return that document which has that key and value pair name where
Horea Porutiu.
So here we're making that curl request.
You can see we're using curl and then we have that external endpoint that we showed you
earlier.
And then you can see we're doing /demo-ibmcloudessentials.
That's the database name that we've created, and we're doing a find, so we're using the
find operation.
So we're going to find the documents in that database that match our query so you can see
here we have authorization token, so I've already created that in previous steps.
And there's documentation on how to do that, but you will need to use your API key to create
a token to authorize yourself.
And then in the data we're just using my selector.
So again, here we see that using that selector we have got our document back and we have
the document ID, the name, the city, and the profession, which we showed you earlier.
So, that was a quick example showing how to use a curl, a cloudant relational database.
And now let's go ahead and summarize.
There are many different types of databases out there.
Relational or SQL databases, document databases, and key value databases.
Database as a service or DBaaS offerings have lowered the cost of manage database while
enabling faster integration with existing applications.
IBM Cloud has many database as a service options from DB2 to cloudantt and from MongoDB to
Postgres.
<br>


## Hands-on Lab: Get to Know Cloudant

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Cloudant database service
    - Create a database in with your Cloudant service
    - Create a document within your database
    - Query your database using the Cloudant Console
<br>

## Integration
In this video, we're going to talk about integration services on IBM Cloud.
We'll start with a basic understanding of integration and then move on to the several
different offerings that IBM Cloud has in terms of integration.
Lastly, we'll end with a demo showing how to use one of these integration services to
send data between applications.
Let's get started.
First, let's define what is integration.
Integration provides connectivity, routing, and transformation for different services.
It enables sharing of data, connecting applications, and security.
IBM Cloud has several services that enable integration, each of which have a free or
Lite tier plan.
API connect which provides API creation and management with security rich features and
centralized governance.
App connect which allows you to connect your applications, automate tasks with hundreds
of built-in connectors.
Event streams, which is a high throughput message bus built with Apache Kafka.
MQ which provides enterprise grade messaging.
Let's take a look at each in more detail.
API connect is a comprehensive end to end API lifecycle solution that enables the automated
creation of APIs.
It also has other features to assist in API lifecycle management, such as being able to
rapidly generate swagger compliant API's from back end data sources,
graphically assembling the API invocation flow and applying access control policies,
being able to share, publish and manage description of APIs through a self-service portal,
and viewing analytics and data about your APIs.
App connect is used to connect different applications and have event trigger actions between the
applications.
For example, in the screenshot below you can see that app connect is being called when
you sales first contact is created, which triggers a nuro in a Google Sheets file which
then sends a message to a specific Slack channel and then creates a task in Insightly.
Using app connect you can automate your workflow, integrate your data and apps with over 75
connectors, use any of the 50 plus templates to quickly get started an create, and expose
flows as rest API's to help developers build applications quickly.
IBM event streams is a high throughput message bus built with Apache Kafka.
It features a fully managed Apache Kafka Service, which is built with the open source Apache
Kafka project.
It's also highly available and resilient.
It leverages the availability zone support from IBM Kubernetes service to ensure that
in the unlikely event of an entire zone being unavailable, your applications will continue
to work uninterrupted.
It also has an intuitive user experience.
And it also has an event driven architecture.
It integrates with services such as the Watson IoT platform and IBM Cloud functions to make
it easy to leverage event streams as the critical component of your event driven architecture.
IBM MQ provides proven enterprise grade messaging capabilities such as point to point and publish
subscribe models to facilitate the flow of information in the form of messages between
applications.
Here are some of the features of the MQ service.
It has a managed messaging service.
It also enables you to extend your enterprise messaging to the cloud.
You can connect new cloud-based apps to your core business systems by integrating with
your existing on Prem MQ Network.
You can quickly provision messaging capability in the cloud of your choice.
You can use it both on IBM Cloud AWS.
And you can manage your way.
You could either use the MQ Explorer, the MQ console, or script commands.
Now let's take a look at a demo using the integration services.
So, here in our event streams we're on, we're about to create a topic and we create this
topic called test and we have one partition and then we have one day where we keep our
messages.
So, this is our stream service and we've created a topic called test.
Now we're going to go into our app connect, so we're going to go ahead and launch it.
And within app connect you can see that we can either create an event driven flow, create
flows for an API, or import a flow.
We're going to create an event driven flow.
Next, we can start the flow here, and then we'll click on toolbox and use the scheduler.
And here with the scheduler, we're going to have a repeating interval, and we'll run that
interval every minute.
And now we're going to add a separate part to the app connects, and then here we'll use
our event streams.
So, we've just created that topic.
As you can remember, and now we have to link the account.
So, the way to link the account is you have to use the service credentials from that service.
So, we're going to go back to the event streams manage console and will copy the credentials
and will place them in.
And then we'll click connect.
And now we're going to be connected to our event streams and you can see we've got a
new account and then we can click send message.
And here we have to find the topic.
The topic is already created, which is called test and the payload.
We're able to add in mappings from the flow.
So, we already have our scheduler, so we'll add in the current event time from the scheduler.
And we'll leave that partition zero, and we can go ahead and try this so we can try the
action test to see if it works and you'll see we get a 200, which is good.
We got a successful request and we can see the payload is just a dummy data which is
1985 April 12, so that's just the current event time, but that is dummy data since we're
just testing the flow now.
We're going to go into storage and we're going to go into our cloudant service.
We're on our product service and we're going to watch the dashboard and will create a database
and we're just going to call it IBM Cloud essentials, and we'll keep it as non-partitioned.
And wie'll it create so will here in our database we can now go ahead and create a document
and now we're going to grab our API key.
So, we'll need to actually connect this Cloud Service an in that we can actually automatically
create a document using app connect.
So now we're going to hit connect and we'll just need our host name and API key.
So, here's our API key and we already grabbed that host name earlier.
We'll click connect.
So, now we're connected to Cloudant.
So, now we should find our database which is IBM Cloud essentials.
And now we're going to leave the document ID empty and then for the document data we
can actually pass in some of the mappings from the flow.
So, we can pass in our scheduler and we can pass in the current event time.
And then we also have our IBM event streams offset available, so that's what we actually
get from our IBM event stream service.
So, we can say hello at this current time from this offset from our IBM event streams.
And let's go ahead and try this out.
So basically, we're just going to create a new document in cloudant and we'll write this
message which is hello at at a certain time from this offset.
And will save this flow in app connect.
And we can start the flow now.
So, once we start the flow, we should get real data so we won't get that.
1985 will get 2020 data here in cloudant and if we refresh, we'll see that we have this
dummy data from hello at 1985 an now.
We also have this real data.
Once we started the flow.
So, hello August 27, 2020 from offset one and if we wait another minute we will refresh
again and now we'll see we should get offset two so, Hello on August 27th from offset two.
So, this was a quick demo showing IBM event streams, and cloudant, and app connect.
Now let's summarize.
Integration enables secure communication between services.
It also allows for sharing of data between applications.
Messaging events and triggers are key components to understand when talking about integration.
IBM Cloud has multiple services that enable integration, such as API connect, app connect,
event streams and MQ.
<br>

## Artificial Intelligence
In this video, we're going to look at one of my favorite topics, artificial intelligence
on IBM Cloud.
We're going to start with the basics around data science and AI, and then we'll move to
IBM's cloud specific offerings in this area.
We'll end with a demo of showing our most popular AI services.
Data science is a method for gleaning insights from structured and unstructured data using
analytics and machine learning.
Data is key here.
Data science excels when there is a massive amount of data to analyze.
What kind of problems can data science solve?
There are plenty of use cases across many industries such as:
Healthcare - uncover insights from clinical trials and patient data.
Banking - give on the spot answers to loan applications.
Education -support personalized planning tracking and data informed advisors.
These are all dealing with large amounts of data.
Good data quality is essential to solving these use cases, but about 80% of a data science’s
time is spent on finding, cleaning, and organizing data.
Once we have good data will be able to build models that can predict and forecast trends.
What is artificial intelligence?
AI is a huge field with many different domains.
What do they all have in common?
You can decently predict things if your model is good enough.
How do you make an affective model though?
It all comes down to the data you use to train that model.
To understand speech and language, we have tons and tons of data available through books,
videos, and other documents.
Once we have that data, how do we create the model?
This is where an iframe workers come into play.
These are incredibly popular frameworks that are flexible and powerful.
The biggest hurdle is the understanding of data science and AI principles to be able
to effectively use these frameworks.
All of these frameworks, such as TensorFlow, Scikit Learn, and PyTorch are open source
and have their various advantages and disadvantages.
Now, let's talk about some of the AI services available on IBM Cloud.
First, we have the AI Lifecycle management tools such as Watson Studio, Watson Machine
Learning, Watson OpenScale, and knowledge catalog.
Next, we have tools, which analyze text such as Natural Language Understanding and tone
analyzer.
We then have intelligent search called discovery.
We have a service, which enables you to build custom models for discovery and for Natural
Language Understanding and that's called knowledge studio.
We also have our speech and language services such as speech to text, text to speech, language
translator, and assistant.
Let's take a look at the AI Lifecycle management tools.
These tools will help you build and scale AI with trust and transparency by automating
AI Lifecycle management.
Watson Studio provides a suite of tools and a collaborative environment for data scientists,
developers, and domain experts.
Watson machine learning lets you run and deploy machine learning models anywhere across any
cloud.
Watson knowledge catalog lets you discover, curate, categorize, and share data assets
and models with access control.
Watson OpenScale lets you measure and manage AI models in production to promote trust and
confidence.
Watson Natural Language Understanding uses deep learning to extract metadata from text,
such as enemies, keywords, categories, sentiment, emotion, relation, and syntax.
Watson tone analyzer uses linguistic analysis to identify tones such as anger, disgust,
fear, joy, and sadness.
It could also detect social propensities such as extraversion and language styles such as
analytical, confident or tentative from text.
Now, let's take a look at Watson Assistant one of the most popular Watson services.
Watson Assistant lets you build conversational interfaces into any application device or
channel.
It has an easy to use UI.
It has a plug-in for Slack and other applications.
It also has a catalog of entities for industries so that you can quickly get started with some
of the most frequently asked questions over chat.
You can also quickly integrate with Twilio, Salesforce, Zendesk, and voice agents as well.
Watson Discovery is an intelligent search service that will deliver specific answers
to your questions while also serving up the entire document for exploration.
Watson Discovery can be trained with entire documents and you can use Watson Knowledge
Studio to build a custom model to train Watson Discovery with unique relationships and entities.
In this example, we trained Discovery with the car service manual to look for information
about what kind of engine oil to use.
With Discovery on the left-hand side, we are linked to the correct section and relevant
information is highlighted.
We also have a confidence score as well.
Now, let's take a look at the speech and language services that are offered on IBM Cloud.
First, we have speech to text, which is a service that transforms voice into written
text.
Next, we have text to speech, which enables you to convert written text into natural sounding
audio in a variety of languages and voices.
Also, we have language translator, which can dynamically translate news, patents, or conversational
documents from over 20 languages and can identify up to 68 languages.
Natural language classifier allows you to assign custom categories to input a text.
Now, let's go into a demo of the Natural Language Understanding service.
So you can see where in the Watson Natural Language Understanding text analysis demo.
You can see we have some sample industry domains such as legal, financial, and media, or you
can just use the base model.
And we have NLU, Natural Language Understanding, has some features to extract meaning from
data.
And we can use the base model by using inputting our own URL.
So, we're just going to go ahead and analyze ESPN.com.
And see what Watson Natural Language Understanding understands from that specific website.
So, it's going to take a little bit of time.
And now we have some entities right out of the box.
So, you can see up at the top, we have the text that Watson is analyzing.
So that's the best fantasy intel compiled on a printable CHEAT SHEET and you can see
the names of the players like James Harden, the name of the organization NBA.
We also have keywords.
So, Watson is great at understanding keywords.
So we have the CHEAT SHEET, the Fantasy Intel, the dozens of films, exclusive live fight
nights.
So, these are all the keywords that is, that is picked up from this text.
Then we have concepts.
We have ESPN, MLB, we have the National Football League and then we have the relations.
We also can have...
We can also see the classification.
So we can see how positive or negative certain entities and the sentiment behind those entities
are.
So, we can see that the football had a pretty negative entity.
But yeah, MLB had a very positive entity.
And if we go to an emotion, we see joy is the highest emotion, and then we have the
categories, such as sports/baseball, sports/basketball, other things like that.
There's also the linguistics or the actual semantic roles such as, such as the subject
action and object form.
And these are kind of the more advanced features of Natural Language Understanding, which is
kind of taken apart that text.
So, that was a quick demo of Watson Natural Understanding.
Of course, you can make the model stronger by training Watson with your domain language
and coming up with unique entities there.
Let's summarize.
We have AI Model Lifecycle management tools to help you build and scale AI such as Watson
Studio, Watson machine learning, and Watson OpenScale.
We have more developer focused AI services such as language translator, Assistant, Discovery
and Natural Language Understanding, which all have premade models.
So, you start using the tools quickly without having to create any models.
Also, all of these services have plenty of API and SDK support for popular languages
such as Python, Go, Android, node.js, Swift, Java, and Salesforce.
<br>

## Hands-on Lab: Get to Know Watson Discovery

- Navigate to [link](https://cloud.ibm.com) to launch the IBM Cloud
    - Create a Watson Discovery service
    - Interact with the Watson Discovery interface
    - Run queries with Watson Discovery

## Analytics
In this video, we're going to talk about Analytics Services on IBM Cloud.
We'll start with looking at the different types of Analytics and then go into the big
open source projects that are in the Analytics space.
We'll then look at IBM Clouds offerings in this area and end with a demo that shows how
to modify a database table and store those results in cloud object storage.
Let's get started.
Data analytics is the science of analyzing raw data in order to make conclusions about
that information.
Any type of information can be subjected to data analytics techniques to get insight that
can be used to improve things.
Let's talk about a few different types of Analytics and understand how they enable us
to make better decisions.
Descriptive analytics looks at past performance and understands that performance by mining
historical data to look for the reasons behind past success or failure.
Diagnostic analytics examines data or content to answer the question, why did this happen?
It is characterized by techniques such as drilldown, data discovery, data mining, and
correlations.
Predictive analytics encompasses a variety of statistical techniques from data mining,
predictive modeling, and machine learning that analyze current and historical facts
to make predictions about future or otherwise unknown events.
Prescriptive analytics takes advantage of the results of Descriptive and predictive
analytics and suggests a decision.
Spark is a unified analytics engine for big data processing with built in modules for
streaming, SQL, machine learning and graph processing.
It is an open source project with 750 contributors from 200 organizations.
Hadoop is a framework that allows for a distributed processing of large data sets across clusters
of computers using simple programming models.
Like Spark, it is also open source.
Hadoop uses the MapReduce programming model for parallel processing of large volumes of
data in a distributed environment.
There are five main analytics services on IBM Cloud.
We have analytics engine, streaming analytics, DB2 warehouse, Cognos dashboard, and information
server.
Let's dive a bit deeper into each one.
Analytics engine lets you deploy and develop applications using open source Apache Spark
and Apache Hadoop.
It also has on-demand scalability and is HIPAA ready for the Dallas region.
It also gives you the ability to customize the environment with third party analytics
libraries and packages.
The streaming analytics service is used to ingest, analyze, monitor and correlate data
in real time.
It evaluates a broad range of streaming data from unstructured text, video, audio data
to Geospatial and sensor data.
It performs real time analysis on data in motion and it can connect with virtually any
data source, whether unstructured, structured or streaming, and integrate with Hadoop and
Spark.
Lastly, it has built in Domain Analytics like machine learning, natural language, spatial
temporal, text, acoustics and more to create adaptive stream applications.
Db2 warehouse is a fully managed elastic cloud data warehouse that delivers independent scaling
of storage and compute and is built for machine learning.
You can train and run models directly in the DB2 warehouse engine using SQL, Python and
R.
It is highly scalable, and you can easily manage and independently scale up, compute
and storage.
It is secure.
You can control and monitor activity on your database with fine grained access control
and database auditing capabilities.
And it's also Oracle compatible.
You can leverage Db2's Oracle capability to run your existing Oracle applications on Db2
warehouse.
The Cognos Dashboard Service lets you add end to end data visualizations to your application.
The visualizations allow users to interact, for instance, they can drag and drop to quickly
find valuable insights on their own.
The visualizations have a live connection to the underlying data.
Updates the data will be reflected in the visualizations in real time.
You could also embed visualizations in your applications.
Data can be explored using filters and navigation paths.
The information server is a market leading data integration platform, which includes
a family of products that enable you to understand, cleanse, monitor, transform, and deliver data,
and to collaborate to bridge the gap between business and IT.
The data stage tool allows you to create jobs that can extract, transform, and load data.
The information governance catalog allows you to track data lineage.
The information analyzer provides data profiling and analysis to accurately evaluate the content
and structure of your data for consistency and quality.
Now let's see an example of the information server in action.
So, here in our information server we have our connections, and we can see we have our
cloud database and our local Db2 warehouse.
We also have table definitions at the top.
So, these are the tables that we have from Db2 warehouse.
We have parameter sets and jobs.
So, now we're going to go ahead and create a job.
And we'll make it a parallel job an in here we can look for some connections.
So pass in a connection from the cloud Db2 warehouse.
And here we will get the schema so will have different schemas and in this blue admin we
can go for seven different types.
And here we can search for a specific column.
And we'll leave all of these employee columns.
It will add these to the job.
So, basically, we have all of these employee columns from that database from Db2 warehouse
and now we can go ahead and cleanse and do some transformations on this data.
So, here we can do a peek and that's just going to show us the top 10 parts of our data.
So now we've connected that database table to the peek and then now we have.
A remove duplicates, so that will just remove any duplicate data in our table and then we
have a sort.
So, we're going to sort this table.
So, we really want to do.
In the end is we want to sort the employee salary from highest to lowest.
And now we've added a cloud object storage connection, so we're going to store the updated
table in cloud object storage.
So now we're going to go ahead and find the connection cloud object storage.
So, we have the login URL and we're going to go back to our cloud object storage instance,
and we'll grab our resource instance ID and API key.
So, here's our cloud object storage.
We have our resource instance ID.
And then we have our API key.
So, we'll paste that in there.
And the region is US East, so I'll paste that in there.
And then that's pretty much it.
We'll click OK and that will connect us to our cloud object storage instance.
And now we're just going to compile and run this job, and we see that run was successful.
And now if we look in our cloud object storage instance, we should be able to see this, this
new table which will have the ascending order for the salary.
So, if we refresh, we have this output dot CSV file and if we go ahead and download it.
We can open it up so we'll open it up with text edit and here we see the database table
and we can see the ascending.
So we can see the salaries 152,000, 9896, 90, 4,089, thousand etc.
So that's how we do a really quick and simple example on information server to transform
some data and then send that to cloud object storage.
And now to summarize, it's all about the data whether you're cleaning it, transforming it,
or visualizing it.
Analytics is all about helping you make data driven decisions.
IBM Cloud has a full set of products that can help you in making use of your data.
At IBM, our analytics engine offering is based on the popular open source projects Hadoop
and Spark.
<br>

## DevOps
In this video, we're going to take a look at DevOps on IBM Cloud.
We'll first learn about DevOps Methodologies and then go into the differences between continuous
integration, continuous delivery, and continuous deployment.
We'll then take a look at IBM specific DevOps services and end with a demo showing how to
use continuous delivery to deploy an application to Cloud Foundry.
Let's get started.
What is DevOps?
DevOps is a set of practices that combine software development dev and it operations
ops.
It aims to shorten the development lifecycle by providing continuous deployment with high
software quality via automated tests and delivery governance.
Continuous integration, continuous delivery, and continuous deployment are key topics for
DevOps.
Let's understand the differences between the three.
Continuous integration is a form of automation testing which checks that the application
is not broken whenever new commits are integrated into the main branch.
Developers using continuous integration aimed to merge their changes back to the main branch
as often as possible.
Continuous delivery goes one step further than continuous integration in that you have
an automated release process that merges your changes from the automated testing process
and pushes them to a staging environment.
Finally, continuous deployment goes one step further than continuous delivery and automates
the process of pushing changes from the staging environment to the production environment.
This enables new features and patches to reach your customer even faster.
The IBM Cloud DevOps services are a set of tools that support development, deployment,
continuous delivery, and operational tasks.
A DevOps toolchain is a set of tools and templates that automates the tasks of developing and
deploying your application.
It contains templates for building and deploying your project.
It also supports integration with many third-party tools.
The continuous delivery service automates the building and deployment of applications.
The delivery pipeline is a part of the continuous delivery service.
It allows developers to automate builds, unit tests, and deployments.
Here we see an example of using the DevOps approach with IBM Cloud tool chain.
First, we have the thing phase in which we use GitLab to plan our Sprint tasks using
issues.
Next, we have the code phase in which we commit changes to our code from the Orion web IDE
to our repository.
Once the commit is pushed, the deliver phase starts automatically.
In this phase, we delivered the latest version of our code to our staging and production
environments using our delivery pipeline.
Next, we have the run phase.
In this phase our application is pushed to a Cloud Foundry service or Kubernetes service
and we can see it running on IBM Cloud dashboard.
Next, we have the learn phase.
We use Google Analytics to gather data and feedback to incorporate into future releases.
Last, we have the culture.
Slack enables teams to communicate faster and more efficiently.
Here are some examples of tools which you can use to build your code in IBM Cloud toolchains:
GitLab CE, GitHub, and Bitbucket.
IBM Cloud toolchains offer a few different delivery options.
First, we can deliver a docker application and its helm chart together in source control
and have it built and deployed automatically to a Kubernetes cluster.
Another option is that you can develop an application and deploy changes using a Razee
agent in your Kubernetes cluster.
Most of the toolchain templates have an option of using Tekton as your delivery pipeline,
which is an open source Kubernetes native in framework for continuous delivery.
In the run stage you can choose the target or where your application will be deployed.
With Cloud Foundry, your application will be deployed as a Cloud Foundry application
on IBM Cloud.
You can also choose to run your applications on a Kubernetes cluster.
As a more advanced option, you can choose to run your application on a virtual server
of your choice.
In the learn stage, you can gather data and feedback about your application to continuously
improve and prioritize features in future releases.
Here are some of the integration the IBM Cloud tool chain support.
We support New Relic, which provides an observe ability platform to ensure your stack is running
as efficiently as possible.
We support Google Analytics, which is an analytic software which helps monitor your website
traffic and better understand your customers.
Ans Sauce labs, a cloud-based platform which specializes in automated testing for web and
mobile applications.
Then we have culture.
In the culture stage, IBM Cloud toolchains provides tools to improve cross functional
communication between teams.
We have slack, which is a channel based searchable messaging platform PagerDuty, an incident
response platform, and Jira, which is an issue tracking product developed by Atlas Ian that
allows bug tracking, an agile project management.
Let's get into an example of using continuous integration to deploy an application to Cloud
Foundry.
So first we start in the IBM Watson/Stock Advisor GitHub repo.
And here we have the deployed to IBM Cloud button.
So, you can see in the documentation we can click on deploy to IBM Cloud and this will
create a toolchain for us in our IBM Cloud.
So here we named the toolchain IBM Cloud Essentials, and we leave it in the Dallas region and we
can see the source repository URL is IBM-Watson stock advisor.
Delivery pipeline, we create a new API key.
And the region, organization, and space is automatically filled up based on our IBM Cloud
account.
And I am in space dev.
And now we're going to create our delivery pipeline.
So now you can see that in the in the code stage we have the Orion, but now we're looking
at the delivery pipeline and we can see the build stage an in the input
we can see that we're inputting a git repository and we're checking the latest changes and
we're pulling from that IBM slash Watson stock advisor so we can see the latest commit.
That's the last input, and then we can see that it's the build stages past now the deploy
stage is running, so that's automatically triggered.
So that is deploying our application now, so we can check the logs and we see that the
it's going well and we're binding a couple services to our application.
And now we see that the application was deployed successfully and we have the URL.
So, Watson stock advisor dash IBM Cloudessentials.mybluemix.net
So here we can see our deployed application.
It's looking good.
We can add stocks, we can do whatever.
But now if we go back into our IBM Cloud we can look and check the status of our Cloud
Foundry application that was automatically deployed with our tool chain.
So, here we are in our application we can see the instances.
We can see the runtime SDK for node.
We can visit the app URL.
It'll take us back to Watson stock advisor.
So, that was a quick demo of how to use continuous delivery within IBM Cloud tool chains.
To summarize, DevOps on IBM Cloud allows you to shorten your software development lifecycle
and provide high quality software.
You can customize your pipeline to make it as simple or complex as you'd like.
You can use third-party integrations to allow you to plug into different tools, and we have
an end to end solution for all stages of your DevOps process.
<br>

## Blockchain
In this video, we're going to talk about blockchain on IBM Cloud.
We'll first covering the blockchain data structure, smart contracts and consensus, and then we'll
look at hyperledger fabric and the IBM blockchain platform.
We'll end with showing a demo of how to use smart contracts to record transactions on
a blockchain network.
Let's get started.
What is a blockchain?
A blockchain is a growing list of records, called blocks that are linked using cryptography.
Each block contains a cryptographic hash of the previous block, timestamp, and transaction
data.
By design, A blockchain is resistant to modification of the data.
Once recorded, the data in any given block cannot be altered retroactively without alteration
of all subsequent blocks, which requires consensus of the network majority.
So, here we have a demo of the blockchain data structure and we have the data and the
previous hash.
And then the hash.
And then we can see this is the Genesis Block, which just means is the first block and then
we have the timestamp.
So, what we're going to do is we're going to add some data and add a new block, and
we're going to just say hello from IBM Cloud in the data field.
We'll add that block, and we can see the data is reflected in that block.
And the important thing to note is that previous hash 7CF.
We can see it's the same as the hash of the Genesis Block.
And our current hash for block number 1 ends in four, 1, four and the timestamp is August
24th.
And now if we add another block we can say hello from San Francisco, add that block and
we can see the previous block ends in 414.
Just like we are expecting it to and then we have our timestamp there and then we have
that hash.
Let's talk about some key elements of a blockchain network.
Blockchains are distributed permanent and record transaction between two parties.
They are distributed.
All network participants have access to the distributed Ledger and it's immutable record
of transactions.
They're also immutable.
No participant can change or tamper with the transaction after it's been recorded to the
shared Ledger, and they use smart contracts to speed transactions.
A set of roles called Smart contracts is stored on the Blockchain and executed automatically.
What is hyperledger fabric?
Hyperledger fabric is an implementation of blockchain technology that is designed as
the foundation for developing blockchain applications.
It has an emphasis on ledger, mark objects, confidentiality, resiliency, and scalability.
Due to popularity, hyperledger fabric has been adopted by major cloud providers including,
Alibaba, AWS, Azure, Google, IBM, and others.
Hyperledger fabric is an Apache two licensed open source project with the founding codebase
originally donated to the Linux Foundation by IBM and digital asset.
Let's take a deeper dive into smart contracts within hyperledger fabric.
Smart contracts are required to create a blockchain application with hyperledger fabric.
Fabric offers SDK's in node.js and Java and support for Python and Go is planned for later
releases.
Smart contracts are executed to change or read a value in the world state.
These smart contract executions are recorded as transactions within the blocks on the Blockchain.
In this way, we have a tamper-proof history of all transactions which have happened on
a particular blockchain network.
Let's talk a little bit about consensus.
Consensus is the process by which nodes agree on the order of transactions.
There are multiple ways of doing consensus, however you do it, the aim of consensus is
to get from the before state on the left to the after state on the right.
In this case, there are four nodes, two of which think that the world state is ABC.
One mistakenly thinks it's DEF due to network latency and one is a malicious node who will
do anything to convince you that the world state is XYZ.
Consensus will get to a situation where all the good nodes agree that the world state
is ABC and the bad node is just ignored.
Consensus assumes that there is a sufficient portion of good actors on the network who
are trustworthy.
The value of Blockchain comes from participants sharing common smart contracts and agreeing
on the source of truth.
Since transactions are automated, participants can be assured money is received upon the
agreement of their contract.
Participants also have visibility into the history of a particular asset and how that
ownership has changed overtime.
This is the IBM blockchain platform in a single chart.
It's based on hyperledger fabric and runs on the IBM Cloud platform, although other
options are available.
IBM blockchain platform aims to help with the entire lifecycle of a blockchain solution
from inception through the deployment and beyond.
There are set of tools for the solution development as well as tools to allow clients to govern
and operate blockchain business networks.
IBM's key differentiators are advanced tooling for building, operating, and growing blockchain
networks and the ability to deploy blockchain networks anywhere.
Now, let's take a look at the IBM blockchain platform in more detail.
Here is the IBM blockchain platform console and where you can see your blockchain nodes.
They have the peers, peer one here.
We have the certificate authorities which give away the public and private keys on the
network and then we have the ordering service which actually keeps track of the channel
and the order of the blocks.
So now we on the left we have smart contracts, our wallet, organizations, and the users on
the network.
Also, we have settings as well.
First, we can take a look at organizations an we can see we have our org one MSP and
then the order MSP.
We can check our wallet, and this is where our credentials are so our public and private
keys are here.
And then we have the smart contracts we have currently.
One smart contract called voter contract that's installed on the network and on the channel
we have one channel called my channel.
And here if we go to the Org One Certificate Authority, we can see that to actually use
an app and to submit transactions to the smart contract, we need to actually get the location
of that org One CA,
and since it's deployed on Kubernetes, we have our URL for our certificate authority
here and we can see that in our application we have this file called IBM blockchain platform
connection,
and this is where we list all the different members of our network, such as the certificate
authorities, the peers, and the ID's and then the URL's to reach those peers.
So you can see that that same certificate authority URL is used.
So, now that in our application we have we have that connection profile that talks to
the peers and the certificate authorities.
We can submit transactions to the channel.
So now we have six blocks in my channel.
And we can see the block history here.
The last transaction was on the 31st of August.
So now we have an application running on localhost 8080 and this one is connected to the blockchain
platform using that connection profile that I showed you earlier.
So, we have a very simple application and we're just going to submit a transaction to
the smart contract.
So, when I create this form and I submit it, I'm going to update that in the smart contract.
So you can see, now when I update our last transaction is today which is September 2nd
and in that transaction I'm going to have whatever I wrote in the application which
was E 311311.
My first name and last name Horea Porutiu in San Francisco and you can see that that
smart contract being referenced up there.
Photo contract 700.
So, you can see that this is being recorded.
We have the transaction ID and this is that new block being added.
So that was a really quick demo and overview of what the blockchain platform looks like.
Let's summarize what we've learned.
Blockchain is a data structure that contains the immutable history of transactions on a
network in cryptographically ordered blocks.
The Order of blocks on a network is reached by the agreement of nodes on the network using
a consensus algorithm.
Mark contracts are code on the blockchain that execute automatically and automate transactions.
IBM blockchain platform is based on hyperledger fabric and adds many operational tools to
speed development and the ability to deploy anywhere.
<br>

## Internet of Things
In this video, we're going to take a look at the IoT platform on IBM Cloud.
First, we'll learn some of the basics around IoT and then take a look at some of the most
common use cases.
We'll then go into the IoT platform on IBM Cloud and end with analyzing the architecture
of the IoT platform.
Let's get started.
What is IoT?
IoT or Internet of Things is a system of interrelated computing devices that transfer data over
a network without requiring human interaction.
There are many use cases for IoT, and here are three.
One.
We have predictive maintenance.
Keeping assets up and running has the potential to significantly decrease operational expenditures,
saving companies millions of dollars.
Two.
Asset tracking.
The goal of asset tracking is to allow an enterprise to easily locate and monitor key
assets along the supply chain to optimize logistics, maintain inventory levels, prevent
quality issues, and detect theft.
Three.
Connected vehicles.
These are computer enhanced vehicles that automate many normal driving tasks.
In some cases even driving themselves.
IBM Cloud's Internet of Things platform or the IoT platform, lets you communicate with
and consume data from connected devices and gateways using a builtin web console to monitor
your IoT data and analyze it in real time.
It has several features such as quickly and securely register and connect your devices
and gateways.
Information management.
Control what happens to the data that is received from your connected devices.
Manage data storage, configure data transformation actions, and integrate with other data services.
Analyze in real time.
Monitor real time device data through rules, analytics and dashboards.
Risk and security management.
Our secure by design control capabilities protect the integrity of your IoT solution
through secure connectivity and access control for users and applications.
The IBM Cloud IoT platform has a powerful dashboard that allows for viewing connected
devices by device type, showing how much data has been transferred, monitoring real time
sensor data, and Geo location data about your devices.
How does it work?
The IoT platform uses the following IoT device data flow.
First, you must register your IoT device in the IoT platform.
Your IoT devices send data using MQTT to the IoT platform, which acts as a message broker
and writes data to cloudant IBM event streams and DB2 warehouse.
Then the data set is also written to cloud object storage for long term storage.
Lastly, analytics services are used to connect to the device, an external data sources to
enable custom dashboards for business users.
<br>

## Cloud Paks
In this video, we'll take a look at IBM Cloud Paks.
We’ll first learn the basics around Callbacks and then look at where they run.
We'll take a look at each Cloud Pak in more detail and end with a demo showing how to
use the Cloud Pak to train an AI model.
Let's get started.
What are IBM Cloud Paks?
Cloud Paks are containerized software solutions built to run anywhere?
I like to think of it as a bundle of continuous software.
The goal of the Cloud Pak is to make container management and application modernization easier
for an organization.
Cloud Paks come in a variety of use cases, which we'll explore later.
For now, let's look at the values of Cloud Paks.
Cloud Paks have a modular architecture, meaning you can pick and choose which software you
want to deploy.
Cloud Paks put AI to work.
They operationalize AI throughout your business.
Cloud Paks are built on OpenShift, which allows them to run anywhere.
So, what do we mean by anywhere?
Cloud Paks can be run on any platform you choose.
You can install them on IBM Cloud.
You can install them on premise.
Use your own hardware or with the Cloud Pak system, or you can install them on any cloud
by first provisioning OpenShift and then installing Cloud Paks on top.
The following picture is a representation of how different Cloud Paks are available.
The six Cloud Paks that we will cover are applications, data, integration, automation,
security, and multi-cloud management.
The Cloud Pak for applications has tools to help you modernize existing applications and
build new cloud native ones.
The four main capabilities are:
Accelerator' for cloud native development, which bring together open source technologies
and put them in a microservices based framework.
IBM modernization and developer tools.
Modernization guidance gives you a plan to start strategically updating your applications.
A Java EE platform is a collection of Java APIs that help you write secure, flexible
server side applications.
Mobile app development tools for building apps for mobile, wearables, conversation,
web or progressive web apps.
Cloud Pak for data has the following features built in:
It has a single platform that integrates data management, data governance, and analysis.
It has databases so you can spin up your favorite IBM or open source database.
It has data governance built in, like automated discovery and classification of data, and
masking of sensitive data.
It also has data virtualization so you can query easily across multiple sources, on cloud
or on premises.
It has IBM Cloud AI services, such as Watson Assistant or Discovery.
And it has AI model lifecycle tools, such as Jupyter or RStudio to create notebook,
serve them with Watson Machine Learning, or automate the whole process with Auto AI
Cloud Pak from Multi Cloud Management is an IT management platform designed to provide
full visibility and control wherever your workloads run.
Using the dashboard, you can monitor application lifecycle management so you can deploy and
move application across clouds.
It provides cloud protection and compliance with automated policy enforcement and compliance
testing.
It has built in SRE tooling with AI OPS to use event correlation and machine learning
to improve operational efficiency and readiness.
It also has many add-on capabilities from IBM partners such as Turbonomic, Sysdig, Humio,
and Hazelcast..
Cloud Pak for integration is a complete set of integration capabilities to efficiently
connect your applications and data wherever they live.
You can use API connect, app connect, MQ and event streams and you have the Aspera high
speed data transfer so you can move data of any size around the world at maximum speed.
IBM Cloud Pak for security is a platform that helps you uncover hidden threats.
Make more informed risk-based decisions and prioritize your teams' time.
It has core platform services such as threat, intelligence, insights, and data Explorer,
and has integrations with existing tools and data such as Qradar and Splunk.
The IBM Cloud Pak for automation provides applications in core areas where automation
provides benefits, content, workflow, decisions, and capture cloud fact for automation.
Provides low code consumable tools, API's and application connectors that make it easy
to consume content in business applications.
You can also automate your end to end workflow with IBM business automation workflow and
you can use IBM operational decision manager to automate the implementation of business
policies in your organization.
So, now let's dive a little bit deeper and show you an example of IBM Cloud Pak for data
in action.
So, here we're logging in with our username and password into our Cloud Pak port data
instance.
We click sign in and here we're greeted with the overview page.
Here we can see our projects or instances and if we go to the top right, we can see
our services catalog.
Here we have all the AI services, such as assistant discovery, knowledge studio, and
the one that we're going to use today is Watson Studio, and we see it's enabled.
And now we can go back to our overview page and we can click on projects to create a new
project and we’ll create an analytics project and then we'll create an empty project.
But you can also create a project from a file, but now we'll just do an empty one and we'll
call it Horea demo.
We’ll click create.
And now you can see that we're into Watson studio here and in our Watson Studio instance
we can click on auto AI experiment.
That's going to give us a new experiment which will automatically train AI model.
We’ll call it demo auto AI and we'll give it a compute configuration and now we have
to give it a data set.
So, this is an insurance data set from Kaggle.
Using age, sex, BMI, number of children, smokers, whatever region you're in and then it's trying
to predict expenses.
So, we're predicting how much is an individual person going to pay for their insurance expense,
is are they going to pay 16,000, 1,700?
4,000, 21,000, and it's all based on if they're smoker or not, their BMI, their age and other
factors.
So, we're going to use that insurance file that I showed you earlier, and we're going
to feed that into Auto AI.
Auto AI is going to automatically detect what type of data that column is and we're going
to predict expenses
And you can see it's a decimal type.
So it's going to be a continuous value from zero to Infinity, and we're going to predict
based on all of these factors and all this training data, once we give it new data, you
know what... is my insurance going to be?
My insurance charge going to be?
You can see here in auto AI we can see our different pipelines being created.
Here we can see the model itself.
We can rank by different metrics such as R-squared, root mean, squared error.
These are all different ways to see how well the model is doing once you feed it new data
and test it with new data.
You can see the algorithm too, using random forest regressor or gradient boosting regressor.
And here we can save it as a model.
So, now we've saved it as a model and already deployed it.
And once we've deployed our model, we can go ahead and use it via rest API.
So, you'll see this is our endpoint, the Zen1-CPD.
So you can copy that and use a rest API call, and you can use Curl, Java, JavaScript.
And we have these code snippets ready for you to show you how to make a post request.
So, here's the input data that we saw based on what we saw earlier.
Age, sex, BMI, children...
So, I'll fill in this details.
Zero, smokers no, region of Southwest.
If I click predict, it's going to use this train model that we've deployed and it's going
to come up with a prediction.
So, we have 4,000.
If we say yes for smoker, the value should be much larger because if you're a smoker,
you're going to pay more for your insurance.
So you can see the value is much larger at 16,000 instead of 4,000 before keeping all
other data points equal.
So, this was an example of using Watson studio within Cloud Pak for data and showing you
the interface and how easy it is to use auto AI to train a model.
<br>