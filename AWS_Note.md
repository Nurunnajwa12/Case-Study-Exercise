# Module 1

Definition: on-demand delivery of compute power, db, storage, apps, and other via internet with pay-as-you-go



Advantages:
- trade capital expense for variable expense
- massive econ for scale
- stop guess capacity
- increase speed and agility
- stop spending money on running and maintaining data centers
- go global in minutes

## Intro to AWS:

What is web services: any piece of software that makes itself available on the internet and uses standardized format 
AWS is a 
- secure cloud platform that offer many products
- provides on demand access
- offers flexibility
- work together
- pay for what u use and when u use

Three ways to interacts with AWS
- AWS management console
- command line interface (CLI)
- software development kits (SDKs)

## Moving to AWS Cloud

Cloud Adaption Framework (CAF)
provide guidance and best practice to help org
six perspectives:
1. business (IT finance and strategy)
2. people (HR, staff, manager)
3. governance (management)
4. platform (provisioning)
5. security (identity, detective control)
6. ops (service monitoring, performance monitoring)

# Module 2: Cloud Economics and Billing

## Fundamentals of pricing
3 cost
1. compute (charged per hour, varies by instance)
2. storage (charged per GB)
3. data transfers

how u pay
- pay for what u use
- pay less when u reserve
- pay less when u use more as AWS grow
Custom Pricing

AWS Free Tier(1 year)

Services with no charges
VPC, beanstalk, auto scaling, cloud formation, iam

### Total Cost of Ownership
financial estimate to help identify direct and indirect costs of system

considerations
- server cost
- storage cost
- network cost
- IT labor cost

AWS pricing calculator
- estimate monthly costs
- identify opportunities to cut costs
- model solution before build them
- explore price point

hard benefits
- reduced spending
- reductions in hardware
- reductions in operational costs
- reductions on operations personnel

soft benefits
- reuse of service and applications
- increased dec productivity
- improved customer sat
- agile business process
- increase global reach

### AWS Org
consolidate multiple acc into an irg tree which each branch represent org unit

features and benefits
- policy based account management
- group based

Security with AWS org
control access with aws identity and access management

org setup
1. create org
2. create org unit
3. create service control policies
4. test restriction

access aws org
- aws management console
- aws cli tools
- sdks
- https query api

### AWS billing and cost management
AWS billing dashboard
spend summary, month to date spend by service

tools
aws budgets, aws cost and usage report, aws cost explorer

### Technical Support Models
provide unique combination of tools and expertise
- aws support
- aws support plans

support is provided 
- experimenting with AWS
- production use of AWS
- business-critical use of AWS

proactive guidance 
- technical account manager

best practices
- aws trusted advisor

account assistance
- aws support concierge

support plans
1. basic support - resource center access, service health dashboard
2. developer support - support for early dev on AWS
3. business support - cust that run production workloads
4. enterprise support - cust that run business and mission-critical workloads

## AWS Global Infrastructure

AWS Region is a geographical area
- data replication across regions is controlled by u
- communication between regions uses AWS backbone network infras
each region provides full redundancy and connectivity
region typically consists of 2 or mote availability zones

selecting a region
- data governance, legal req
- proximity to cust
- services available within region
- cost

Availability zones
- each region has multiple availability zones
- fully isolated partition of the aws infras
	- 69 worldwide
	- consists discrete data center
	- design for fault isolation
	- interconnect with other AZ by using high-speed private internet
	- replicate data and resource across AZ

AWS data centers
- design for security
- where data resides and data process
- has redundant power, networking and connectivity
- has 50000 to 80000 physical servers

Points of presence
- AWS provides global network of 187 pop loc
- consists 176 edge location and 11 regional edge caches
- used with amazon CloudFront to reduced latency

features
- elasticity and scalability
- fault-tolerance
- high availability

Section 2 AWS services and service cat 
storage service
amazon s3, ebs elastic block storage, efs elastic file system, simple storage service glacier

compute service
amazon ec2, ec2 auto scaling, ecs elastic container service, ec2 container registry, elastic beanstalk, aws lambda, eks, fargate

database service
relational db service, aurora, redshift, dynamodb

networking and content delivery
amazon vpc, elastic load balancing, cloudfront, transit gateway, route 53, direct connect, vpn

security, identity and compliance
iam, org, cognito, artifact, key management service, sheild

cost management
cost and usage report, bdgets, cost explorer

management and governance
management console, config, cloudwatch, auto scaling, cli, trusted advisor, architected tool, cloudtrail

## AWS Cloud Security

### Share responsibility model
aws responsible for security of the cloud (software/hardware)
cust. responsible for security in the cloud

- physical security of data center(control, need based access)
- hardware and software infrs(storage decom, host os access logging, auditing)
- network infras(intrusion detection)
- virtualization infras(instance isolation)

aws services
1. compute
2. storage
3. database
4. networking

global infras
- region
- AZ
- edges

### AWS IAM
allow to define fine-grained access rights:
- who can access resource
- which resources can be access and what can the user do to the resource
- how resource can be access

no cost account feature

IAM essential components
1. IAM user
2. IAM group
3. IAM policy
4. IAM role 

 authentication
 - programmatic access
	 - authenticate using access key id and secret access key
	 - provides aws cli and sdk access
- aws management console access
	- 12 digit id, user name, pw
	- MFA prompts code


## Module 5: Networking and Content Delivery

### Section 1: Networking Basics
Network - 2 or more machine connected 
IP addresses - unique address that are assign to each machine

Classless Inter-Domain Routing (CIDR)

Open System Interconnection (OSI) model
1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

### Amazon VPC
provision a logically isolated section of the AWS cloud
control over virtual networking resources
customize network configurations
multiple layers of security

Reserved IP Address
10.0.0.0 - Network Access
10.0.0.1 - Internal communication
10.0.0.2 - DNS resolution
10.0.0.3 - Future use
10.0.0.255 - Network broadcast 

Public IP address types
public: manually assigned,

Elastic Network interface
attach to an instance
detach from instance and
