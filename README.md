# AWS Well-Architected Framework 

## Intro
AWS have produced a series of whitepapers under the collective title "Well Architected Framework".

The series presents an organised collection of best-practices and core strategies for building systems in the cloud.

Many of the practices described translate well to on-prem solutions.

## General practices / Recurring themes
* Working back from the customer (#customer obsessed).  
* Data-driven decisions - stop guessing capacity
* Test at production scale
* Automate as much as possible.  
* Game days - test/rehearse/improve runbooks.
* Detailed logs (audit, architecture state, workload)

## The 5 Pillars of the Framework
AWS's wisdom is distributed among 5 pillars.
* Operational Excellence - Run, monitor and maintain your workloads. 
* Security - Protect information, workloads and assets.
* Reliability - Mitigate disruption and recover from failure
* Performance Efficiency - Use resources efficiently
* Cost Optimisation - Deploy and run your workload at the lowest price point.

## General treatment of each pillar 
Each pillar comprises 
* A small set of Design Principles - general guidelines
* A list of Best Practices for each Design Principle - guidelines to help expose the areas you want to address. 
* Key AWS Services that address can be used to implement each practice

### Example: Design Principles of Operational Excellence
[Operational Excellence Pillar](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=6)
* Perform operations as code
* Annotate documentation
* Small, frequent, reversible changes
* Evolve your ops procedures frequently
* Use Game Days to help anticipate failure
* Learn from all ops failures.

### Example: Best practices of Operational Excellence
Best practices of Operational Excellence are grouped into
* Prepare
* Operate
* Evolve    

For each practice, AWS provide specific questions and practices that can be employed to help provide an answer to each question.
 
### Sample Questions:
#### Operational Excellence
[How do you determine what your priorities are?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=48)
[How do you design your workload you can understand its state?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=49)
[How do you know you are ready to support a workload?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=52)

#### Security
[How do you protect your networks?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=61)
[How do you protect your compute resources?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=61)

### Reliability
[How do your system withstand component failures?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=69)

#### Performance Efficiency
[How do you evolve your workload to take advantage of new releases?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=76)

#### Cost Optimisation
[How do you decommission resources?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=81)


## The Well-Architected Tool
[The Well Architected Tool](https://aws.amazon.com/well-architected-tool)


## Final Thoughts
We have separate groups in TT for managing infrastructure, security and pipelines.

A familiarity of these papers would be good preparation for any discussions with any of these groups.

AWS offer a breadth of services that appear to perfectly address many of the questions posed in this doc.
* Infrastructure as code
* S3 Storage Classes
* Log storage
* Caching services (Elasticache, API gateway, Dynamo DB)
* Replication of data (S3, DynamoDb, RDS)
* Security at all levels of each service.
* Everything is available via Console , API and SDK
* Compute available as VMs, containers or functions.

## Small note on how AWS work
Each team in AWS is given the capability to build their own application (workloads) as they see fit.
To ensure success, AWS put in-place
 1) experts into each team to ensure that practices are being met
 2) automated-checks to ensure that standards are met.
 
There are also a virtual team of principal engineers who are available to review designs and discuss options.
