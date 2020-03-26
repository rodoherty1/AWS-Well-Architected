# AWS Well-Architected Framework 

## Intro
[The Well-Architected Framework whitepaper](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf)

AWS have produced a series of whitepapers under the collective title "Well Architected Framework".

The whitepaper's goal is to **help you build robust, performant, well thought out solutions** that address one of your business's priorities.

It does this by **posing a large collection of questions** that you should ask yourself throughout the lifecycle of the workload that you are building.

The whitepaper presents an organised **collection of best-practices and core strategies** for building systems in the cloud.

Many of the practices described translate well to on-prem solutions.

## Glossary
  **Component**
  
   * Code, configuration and AWS Resources that together deliver against a requirement.
   * Is a unit of technical ownership
   * Is decoupled from other components
  
  **Workload**
  
   * Identifies a set of components that together deliver business value
   * Is at a level that business and technology leaders talk about.
   
  **Architecture**
  
   * How components work together in a workload.
   * Represented by architecture diagrams.
   
  **Technology Portfolio**
  
   * A collection of workloads that are required for the business to operate.
  
## General practices / Re-occurring themes
* Working back from the customer (#customer obsessed).  
* Data-driven decisions - stop guessing capacity
* Test at production scale
* Automate as much as possible.  
* Game days - test/rehearse/improve runbooks.
* Detailed logs (audit, architecture state, workload)

## The 5 Pillars of the Framework (P R O C S)
AWS's wisdom is distributed among 5 pillars.
* **P**erformance Efficiency - Use resources efficiently
* **R**eliability - Mitigate disruption and recover from failure
* **O**perational Excellence - Run, monitor and maintain your workloads. 
* **C**ost Optimisation - Deploy and run your workload at the lowest price point.
* **S**ecurity - Protect information, workloads and assets.

## General structure of each pillar 
Each pillar comprises 
* Some Design Principles - general guidelines
* A list of Best Practices - specific guidelines to help expose the areas you want to address. 
* A small list of questions you should ask yourself
* Key AWS Services that can be used to implement each practice

## Operational Excellence
### Design Principles of Operational Excellence
[Operational Excellence Pillar](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=6)
* Perform operations as code
* Annotate documentation
* Small, frequent, reversible changes
* Evolve your ops procedures frequently
* Use Game Days to help anticipate failure
* Learn from all ops failures.

### Best practices of Operational Excellence
* Operations teams need to understand their business and customer needs so that they can effectively nd efficiently support business outcomes.
* Operations creates and uses procedures to respond to operational events.
* Operations validates that operational procedures support business needs. 
* Operations collects metrics that are used to used to measure the achievement of desired business outcomes.

#### Opertional Excellence - Prepare
* Business, Development and Operations must have a shared goals and a shared understanding of the customer needs and business requirements that relate to the workload being supported.
* Design workloads that can be monitored and inspected (troubleshooting / easily understood) with respect to the requirements as well as customer experience and behaviour.
* Demonstrate through metrics and procedures that an application is ready to move into production and be supported by operations.
* Practise using Game Days.
* Infrastructure as code using CloudFormation so that you can replicate your workload in different environments.
* Collect logs in Cloudwatch, CloudTrail and VPC Flow Logs.
* Minimise the number of architecture standards which each add complexity to a workload.  More burden on dev and ops.

#### Opertional Excellence - Operate
* Define business and customer outcomes that will determine if operations are successful.
* Identify the workload and operations metrics that will determine if operations are successful.
* Use runbooks for well understood events.
* Use playbooks to aid in the resolution of other events.
* Use dashboards and notifications to communicate the health of your workloads.
* Tailor the dashboards and notifications to their target audience.


#### Opertional Excellence - Evolve
* TBC

For each practice, AWS provide specific questions and practices that can be employed to help provide an answer to each question.


### Operational Excellence - Sample Questions
[How do you determine what your priorities are?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=48)

[How do you design your workload you can understand its state?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=49)

[How do you know you are ready to support a workload?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=52)

### Security
[How do you protect your networks?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=61)

[How do you protect your compute resources?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=61)

### Reliability
[How does your system withstand component failures?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=69)

### Performance Efficiency
[How do you evolve your workload to take advantage of new releases?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=76)

### Cost Optimisation
[How do you decommission resources?](https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf#page=81)


## The Well-Architected Tool
[The Well Architected Tool](https://aws.amazon.com/well-architected-tool)


## Final Thoughts
* The is an overview of AWS's experience and advice - why would you ignore that?
* Many of the practices here can be applied to on-prem projects.
* Familiarity with this whitepaper would be good preparation for any conversations with:
  * Product Owners
  * Infrastructure
  * Security
  * Solutions Architects
  * Pipeline management
* It turns out that AWS services can be used to solve all the questions posed in this whitepaper.
  * Infrastructure as code
  * S3 Storage Classes and Lifecycle rules
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
 3) Regular lunchtime talks that focus on applying best practices to real examples.
 
There are also a virtual team of principal engineers who are available to review designs and discuss options.
