# EC2 - Elastic Compute Cloud

Amazon Elastic Compute Cloud (EC2) is a web service provided by Amazon Web Services (AWS) that allows users to rent virtual servers in the cloud. EC2 instances provide scalable compute capacity and are commonly used for a variety of applications, including web hosting, application development, testing, and more.

Here's a high-level summary of EC2 and the different types of EC2 instances:

## Types of EC2 Instances

Sure, here is the response in markdown format:

## EC2 Instance Types

There are many different types of Amazon Elastic Compute Cloud (EC2) instances, each with its own strengths and weaknesses. The best instance type for a particular workload will depend on the specific needs of that workload.

Here are some of the most common EC2 instance types:

**General purpose:** These instances are designed for a wide variety of workloads, including web servers, application servers, and databases. They are a good choice for workloads that do not have specific requirements for CPU, memory, or storage.


**Compute optimized:** These instances are designed for workloads that require high CPU performance. They are a good choice for workloads such as high-performance computing (HPC), scientific computing, and machine learning.


**Memory optimized:** These instances are designed for workloads that require a large amount of memory. They are a good choice for workloads such as in-memory databases, caching, and analytics.


**Storage optimized:** These instances are designed for workloads that require a large amount of storage. They are a good choice for workloads such as data warehouses, big data, and archival storage.


**Accelerated computing:** These instances are designed for workloads that require specialized hardware, such as GPUs or FPGAs. They are a good choice for workloads such as graphics rendering, video encoding, and machine learning.


When choosing an EC2 instance type, it is important to consider the following factors:

* **Workload:** What type of workload will the instance be running?
* **CPU:** How much CPU performance does the workload need?
* **Memory:** How much memory does the workload need?
* **Storage:** How much storage does the workload need?
* **Network:** How much bandwidth does the workload need?
* **Cost:** How much can you afford to spend on an instance?

Once you have considered these factors, you can use the AWS Instance Type Comparison Tool to narrow down your choices. This tool allows you to compare different instance types based on a variety of factors, such as CPU, memory, storage, network, and cost.

It is also important to note that there are several different ways to pay for EC2 instances. You can pay on-demand, which means you pay for the instance by the hour. You can also purchase reserved instances, which gives you a discount on the hourly rate in exchange for committing to a one-year or three-year term. Additionally, you can use Spot Instances, which are unused instances that Amazon sells at a significantly reduced price. However, Spot Instances can be terminated at any time by Amazon if they are needed for other purposes.

By carefully considering your workload requirements and budget, you can choose the right EC2 instance type for your needs.

## EC2 instance Purchase Options


Amazon Elastic Compute Cloud (EC2) offers a variety of instance purchase options to suit different needs and budgets. These options include:

* **On-Demand Instances:** The most flexible option, On-Demand Instances offer pay-as-you-go pricing with no upfront commitments. You can launch and terminate instances as needed, and you will only be charged for the time your instances are running.
* **Reserved Instances (RIs):** RIs provide a significant discount on the hourly usage of On-Demand Instances in exchange for a one- or three-year commitment. RIs are a good option for workloads that have predictable usage patterns.
* **Spot Instances:** Spot Instances are up to 90% cheaper than On-Demand Instances, but they can be interrupted by AWS at any time if there is not enough capacity available. Spot Instances are a good option for workloads that can be tolerant of interruptions.
* **Dedicated Hosts:** Dedicated Hosts provide you with dedicated physical servers that are fully isolated from other AWS customers. This can be a good option for workloads that require high performance or isolation.
* **Dedicated Instances:** Dedicated Instances are similar to Dedicated Hosts, but they are a more flexible option that allows you to choose the instance type that you need. Dedicated Instances can be a good option for workloads that require high performance or isolation, but that do not need a full physical server.
* **Capacity Reservations:** Capacity Reservations provide you with the ability to reserve capacity in a specific Availability Zone for a one- or three-year term. This can help you to ensure that you have enough capacity to run your workloads, even during periods of high demand.

The best EC2 instance purchase option for you will depend on your specific needs and requirements. Consider factors such as your workload's predictability, tolerance for interruptions, performance requirements, and budget when making your decision.

Here is a table that summarizes the key differences between the different EC2 instance purchase options:

| Option | Upfront Commitment | Pricing | Interruptibility | Isolation |
|---|---|---|---|---|
| On-Demand Instances | No | Pay-as-you-go | No | No |
| Reserved Instances (RIs) | Yes (1- or 3-year) | Significant discount on On-Demand Instances | No | No |
| Spot Instances | No | Up to 90% cheaper than On-Demand Instances | Yes | No |
| Dedicated Hosts | Yes (1- or 3-year) | Pay-as-you-go for the host, plus On-Demand or RI pricing for instances | No | Yes |
| Dedicated Instances | Yes (1- or 3-year) | Pay-as-you-go for the instances | No | Yes |
| Capacity Reservations | Yes (1- or 3-year) | Pay-as-you-go for the capacity reservation, plus On-Demand or RI pricing for instances | No | No |

I hope this helps!

## In addition to the above options, you can also use the following strategies to save money on your EC2 costs:

* **Right-sizing your instances:** Make sure you are using the right instance type for your workload. You can use the AWS Auto Scaling service to automatically scale your instances up or down based on demand.
* **Using RI purchase discounts:** AWS offers a variety of discounts on RIs, such as volume discounts and discounts for committing to longer terms.
* **Using Spot Instances:** Spot Instances can be a great way to save money on workloads that can be tolerant of interruptions. However, you need to be aware of the risks involved in using Spot Instances, such as the possibility of interruptions.
* **Using Capacity Reservations:** Capacity Reservations can be a good way to save money on workloads that have predictable usage patterns and require high availability.

By using a combination of these strategies, you can significantly reduce your EC2 costs.

Certainly! Here's the information formatted in Markdown with the use of tables:

## AWS Shared Responsibility Model for EC2

### AWS's Responsibilities:

| Responsibility                 | Description                                                                                          |
| ------------------------------ | ---------------------------------------------------------------------------------------------------- |
| Physical Security              | AWS is responsible for the physical security of the data centers hosting EC2 instances.               |
| Network Infrastructure         | AWS manages the underlying network infrastructure, including hardware and software components.      |
| Hypervisor Security            | AWS is responsible for securing the hypervisor, enabling multiple EC2 instances on a single host.    |
| Foundational Services Security | AWS ensures the security of foundational services like IAM, KMS, and AWS CloudTrail.                 |

### Customer's Responsibilities:

| Responsibility                    | Description                                                                                   |
| --------------------------------- | --------------------------------------------------------------------------------------------- |
| Operating System and Applications | Customers are responsible for securing the OS and applications on their EC2 instances.        |
| Data Encryption                   | Customers are responsible for encrypting data at rest and managing encryption keys.            |
| Identity and Access Management    | Customers configure and manage IAM roles and permissions for users and applications.           |
| Firewall and Security Groups      | Customers configure security groups and network ACLs to control inbound and outbound traffic. |
| Data Backups and Recovery          | Customers implement backup strategies and mechanisms for data recovery in case of incidents.  |
| Application Security              | Security measures related to applications running on EC2 instances are the customer's duty.   |
| Instance Security                 | Customers secure EC2 instances, manage access, and implement host-based firewalls.            |

Understanding and adhering to the shared responsibility model is crucial for ensuring a secure AWS environment. It guides customers in making informed decisions about security controls, monitoring, and incident response.