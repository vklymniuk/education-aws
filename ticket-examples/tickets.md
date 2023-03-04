List with links:

```r
1. Which of the following can be enforced for IAM users for securing IAM credentials?

    `-  Enable IAM Groups`
    `+  Enable MFA`
    `+  Use password expiry`
    `-  Enable IAM Users`

 
Why not IAM Groups or IAM Users? Question was about securing existing accounts and not about enabling.


Take a look at AWS as a incapsulated platform which help your buisness to start and grow.
Every single detail and service give your buisnees ability to atomatative the processes inside or
space for hosting and deploying your app.


So, what is basicaly means this IAM account configuration?


That is global security rules-variables setup for `your platform` accounts which 
should be managed and created with tool that we gonna overview next.

Here is example of automatisation global rules for your account with HashiCorp terraform tool.
link: https://github.com/vladimir-klymniuk/aws-practitioner-exam/tree/master/terraform/iam
```

```r
2. Which of the following service can be used to create a self-hosted database?
    - AWS DynamoDB
    + AWS EC2 Instance
    - AWS RDS
    - AWS Aurora


Why, so? Let's get the short overview of following  services examples.

`AWS DynamoDB` - that is fully managed NoSQL database, that supports key-value paradigm for data and documents. She proposed as one of Amazon Web Services. Supplies two tarefication modes based on RPS or traffic size throughout.

`AWS EC2 Instance` - Amazon Elastic Compute Cloud(Amazon EC2) - web service, `EC2` provides ability to users to rent servers which hosts at the amazone cloud. `EC2` service includes in Amazon Web Services infrastructure. Userfriendly web interface allows to get access to instance resources and manage connection interfaces around it and inside.

`AWS RDS` - (Amazon Relational Database Service) is managed relational database service for MySQL, PostgreSQL, MariadDB, Oravle BYOL, or SQL Server.

`AWS Aurora` - is a relational database with MySQL and PostgreSQL compability. Aurora automatically allocates database storage space in 10-gigabyte increments, as needed, up to a maximum of 128 terabytes. Aurora offers automatic, six-way replication of those chunks across three Availability Zones for availability and fault-tolerance. Aurora MultiMaster allows creation of multiple read-write instances in an Aurora database across multiple Availability Zones, which enables uptime-sensitive applications to achive continuous write availability through instance failure.

Сonclusion - Only AWS EC2 Instance is open for installation database inside.
```


```r
3. Which of the followinf service can be used to host a
MariaDB database on the AWS Cloud
    - AWS DynamoDB
    - AWS S3
    + AWS RDS
    - AWS Aurora


To answer for this question we should answer what is `MariaDB`? 


MariaDB is fork of MySQL from 5.2 version with her cutsom database engines which extends and overload MyISAM to Aria and InnoDB to XtraDB. 

Aria improved relability and consistency of data, also operation log supports ability to restore database from any point in bulk operactions (includes CREATE / DROP / RENAME / TRUNCATE).

XtraDB was merged with newest version of InnoDB. 

Sphinx - storage for search queries. Mounted Sphinx-client allow MariadDB to exchange data with searchd, execute search queries and accept results.


Сonclusion - due our previous question we know that: Aurora - supports only original MySQL and PosgreSQL, S3 - is a file storage, DynamoDB - key-value memory storage and RDS is a wrapper around SQL based databases. 

```

```r
4. You are planning on developing an application that will make use of AWS(Amazon Web Service) services. You need to carry out optimization for your application and see ways for improvement. Which of the below service can help in this regard.
    
    + AWS X-Ray
    - AWS CodeInspector (No such service)
    - AWS CodeDeploy
    - AWS CodeCommit    (No such service)


Let's get overview of that services and their differens.

`AWS X-Ray` helps developers analyze and debug production, distributed applications, such as those build using a microservices architecture. With X-Ray, you can understand how your application and it's underlying services are performing to identify and troubleshoot the root cause as they travel through you application, and shows a map of your apllications's underlying components. You can use X-Ray to analyze both applications in development and in production, from simple three-tier applications to complex microservices applications consisting of thousands of services.

`AWS X-Ray` works with `Amazon EC2`, `Amazon EC2 Container Service(Amazon ECS)`, `AWS Lambda`, `Amazon SNS` and `AWS Elastic Beanstalk`. You can use X-Ray with applications written in Java, Node.js and .NET that are deployed on these services. 

A trace repsesents a request to your application and may include multiple data points, such as for calls to other services and database access. The maximum siz of a trace is 500KB. Trace data is retained for 30 days from the time it is recorded at no additional cost.

`AWS CodeDeploy` | TODO: Deploy several types of nodejs applications that uses api (kust graphql), daemon applications (twitch bot).


Integrated and automates software deployments to a variety of compute services such as Amazon EC2, AWS Fargate, AWS Lambda, and your on-premises servers.

Interesting thing about pricing

For CodeDeploy on EC2, Lambda, ECS: There is no additional charge for code deployments to Amazon EC2, AWS Lambda or Amazon ECS through AWS CodeDeploy.

For CodeDeploy On-Premises: You pay $0.02 per on-premises instance update using AWS CodeDeploy. For example, a deployment to three instances equals three instance updats. You will only be charged if CodeDeploy performs an update to an instance. You will not be charged for any instances skipped during the deployment and S3 buckets resources.


From that 4 options, two aren't exists and X-Ray service responsible for workability optimisation and profiling deployed services. CodeDeploy is tool for application deployments.
```

``` r
5. Your IT Security team has notified of suspicious activity in the AWS(Amazon Web Service) account. You need to check and see what API calls were made in the last week. Which of the below service can help fulfil this requirement.


    - AWS Cloudwatch Metrics
    + AWS CloudTrail
    - AWS Cloudwatch Logs
    - AWS VPC Flow Logs


`Cloudwatch` - is monitoring and alerting service.
`CloudTrail` - track user activity and api usage.
VPC Flow Logs - is a feature that enables you to capture information about the IP traffic going to and from network interfaces in you VPS.

If case when we should proccesed suspicious AWS services users activity we should use ClourTrail. If other hand in case we should analyze traffic VPC Flow Logs & CloudWatch is much better tools.
```

```r
6. Which of the following is an advantage of moving from on-premise to AWS(Amazon Web Service) when it comes to costing.

    + Lower capex costs + Variable opex costs
    - Higher capex costs + Variable opex costs
    - Lower capex costs + Fixed opex costs
    - Higher capex costs + Fixed opex costs


`OPEX costs` - is an ongoing cost for running a product, business, or system. 

`CAPEX costs` - is the money an organization or corporate entity spends to buy, maintain, or improve its fixed assets, such as buildings, vehicles, equipment, or land.

On-premise infustructure is a CAPEX, couse we own that physical servers and maximum available usage is fixed. Moving to cloud gaves us ability to pay on-demand services and have variable bills depends on real usage with ability to scale our inrastructure on request.
```

```r
7. Which of the following is available across all AWS(Amazon Web Service) support plans? Choose 2 answers from the options given below.

    - Access to all checks in the Trusted Advisor
    - 24x7 access to Cloud Support forums
    + AWS support forums
    + Personal Health Dashboard


Trusted Advisor - checks available only for Business and Enterprise plans.

24x7 access to Cloud Support forums - has limitation for amazon development plan, available on `Business hours` (08:00 AM to 06:00 PM) in the customer country and only for one account.

AWS support forums - no information about that, looks like simple AWS forums.

AWS Personal Health Dashboard - Dashboard with cusomized events from CloudWatch, aggregate issues in tickets, can be secured with IAM settings. Integrated with pagerduty, datadog, splunk> tools. Available for all plans.
```

```r
8. You have a Hybrid IT architecture. Which of the
        following can help create a secure connection between on-premise and AWS

        + AWS Direct Connect
        - AWS Virtual Private gateway
        - AWS Virtual Private Connection
        - AWS Virtual Private Cloud

AWS Direct Connect - is a cloud service that links your network directly to AWS to deliver consistent, low-latency perfomance. With AWS Direct Connect, you pay only for what you use and there os no minimum fee.

AWS Virtual Private gateway - Secured entry point in private network.
AWS Virtual Private Connection - Resource of your private connection channel.

 AWS Virtual Private Cloud - some termin that describe group of your instances, services, application inside the AWS platform.

 If we are talking about AWS infrastracture services posiblilities for sure Direct Connect is the best choice. Using that services we create secured private channel for data transfer, but indeed VPN ipsec tunnel between SiteToSite point it also could be a solution..
```

```r
9. You are planning on using the Autoscaling Service. What feature does Autoscaling provide to you to create a more scalable architectture.
        + Scale up resources based on the demand
        - Distribure traffic to miltiple resources in diffenerent regions 
        - Distribute traffic to multiple resources in Availability zones
        - Create a secure cloud architecture
        - Create a secure cloud architecture
```


```r
10. A company has many departments that use AWS(Amazon Web Service) resources. They need a way to segregate the costing aspect for each of these accounts. How can you accomplish this

        - Create separate accounts for each department
        - Create separate reports in the Cost Explorer
        - Create separate VPC's for each department 
        - Create separete users for each department
```


```r
11. Which of the following services makes use of edge location? Choose 2 answers from the options given below
    + AWS Cloudfront
    + AWS Shield (only advanced)
    - AWS VPC
    - AWS Elastic Load Balancer


`Edge location` A site that CLoudFront uses to chache copies of your content for faster delivery to users at any locations.

`AWS Cloudfront` - Amazons Global Edge Network. Reliable, low latency and high throughput network connectivity with groupped entry points, cache servers and regional groups of networking communication channels.

`AWS Shield` - Services wich could wrap AWS entry points like Elastic IP, Elastic Load Balncing (ELB), Amazon CloudFront, AWS Gloabal Accelerator, or Amazon Route 53 to reduce common, most frequently occuring network and transport layer DDoS attacks.

`AWS VPC` Networking feature with different analyze and security features.

`Elastic Load Balancer (ELB)` - Distribute network traffic to improve application scalability
```

```r
12. You want to have the ability to distribute content across the world with the least amount of latency. Which of the following service could you use for this requirement.

    + AWS Cloudfront
    - AWS Elastic Load Balancer
    - AWS WAF
    - AWS Shield

AWS Cloudfront - resposible for access in AWS distributed network with own magistrals all over the wold.

AWS Elastic Load Balancer - is internal tool for trafic routing inside that network

AWS WAF - Web Application Firewall that can be deploed on Amazon CLoudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on EC2, AMazon API Gateway for your REST APIs, or AWS AppSync for yout GraphQL APIs. With AWS WAF, you pay only for what you use and the pricing is based on how many rules you deploy and how many web request your application receivers.

AWS Shield - resposible for ddos protect.
```

```r
13. Your company is planning on hosting a mission critical application on the AWS(Amazon Web Service) platform. The application would e hosted on EC2 Instances. The company wants to add `the highest level of fault tolerance to the application`. Which of the following desing patter could be used when it comes to hte application infrastructue?

    - EC2 Instances in a single. Availability zone in a single region.
    
    - EC2 Instances in a multiple Availability zones in a single region

    +/- EC2 Instances in a single Availability zone in 2 regions

    +/- EC2 Instances in multiple Availability zones in 2 regions


Why so? The correct answer.. it depend on

<!-- 1 - We don't know anything about other infrastructure configurations around the instances that's why add autoscalling rules to current instance would be a normal desion.  -->

3 - 4 To reduce pressure on databases located in same location. Each Region contain several availablity zone and each availability zone can contain databse instance.

A source DB instance can have cross-Region read replicas in multiple AWS Regions.

https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.XRgn.html#USER_ReadRepl.XRgn.Cnsdr
```

```r
14. You need to create a snapshot of an EBS volume in another geographic location. Where would you store the snapshot.

    - In another Data Centre
    - In another Availability Zone
    - In another Edge Location
    - In another Region

Edge Location -> Region -> Availability Zone.

Think about availability zone as independent Data Center.

In context of this question not every Data Center uses AWS, but each availabilit zone has other geographic location. And each region has multiple Data Center that can be located in similar refion.

EBS Create or Copy ability gave us only region location option with details customization.
```

```r
15. You need to create a development and test environment for 3 months in AWS. The development and test environment would consist of EC2 Instances. Which of the folliwing would be the ideal pricing model to use for the EC2 instances?

    - On-Demand instances
    - Reserved Instances
    - Spot Instance
    - Dedicated Host
```


    16.
    17.
    18.
    19.
    20.
    21.
    22.
    23.
    24.
    25.
    26.
    27.
    28.
    29.
    30.
    31.
    32.
    33.
    34.
    35.
    36.
    37.
    38.
    39.
    40.
    41.
    42.
    43.
    44.
    45.
    46.
    47.
    48.
    49.
    50.
    51.
    52.
    53.
    54.
    55.
    56.
    57.
    58.
    59.
    60.
    61.
    62.
    63.
    64.
    65.