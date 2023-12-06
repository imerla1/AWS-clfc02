# What is cloud computing?

## Cloud Computing

Cloud computing is a technology that enables access to and delivery of computing resources, including computing power, storage, and various services, over the internet. Instead of owning and maintaining physical servers or infrastructure, users can rent or lease these resources on a pay-as-you-go basis from a cloud service provider.

Key characteristics of cloud computing include:

- **On-Demand Self-Service:** Users can provision and manage computing resources as needed without requiring human intervention from the service provider.
- **Broad Network Access:** Cloud services are accessible over the internet from various devices, such as laptops, tablets, and smartphones.
- **Resource Pooling:** Resources are pooled to serve multiple customers. Providers use multi-tenant models with different physical and virtual resources dynamically assigned and reassigned.
- **Rapid Elasticity:** Resources can be rapidly scaled up or down to accommodate changes in demand. Users only pay for the resources they consume.
-**Measured Service:** Cloud computing resources are metered, and usage can be monitored, controlled, and reported, providing transparency for both the provider and the consumer.


## Service Models

Cloud computing encompasses various service models and deployment models. Here are the primary types of cloud computing:

### Infrastructure as a Service (IaaS)
- Provides virtualized computing resources over the internet.
- Users can rent virtual machines, storage, and networking infrastructure.
- Examples: Amazon EC2, Microsoft Azure Virtual Machines.

### Platform as a Service (PaaS)
- Offers a platform allowing customers to develop, run, and manage applications without dealing with the complexities of infrastructure.
- Typically includes development frameworks, databases, and other tools.
- Examples: Heroku, Google App Engine.

### Software as a Service (SaaS):

- Delivers software applications over the internet on a subscription basis.
- Users access the software through a web browser without worrying about underlying infrastructure.
- Examples: Google Workspace, Microsoft 365, Salesforce.

<img title="a title" alt="Alt text" src="./01-what_is_cloud_computing/assets/iaas-vs-paas-vs-saas-examples.png">

## AWS Regions

### Region
A geographical area that consists of two or more Availability Zones. AWS regions are isolated from each other, and they are designed to provide low-latency and high-throughput connections between each other.

### Availability Zone (AZ):
A data center or cluster of data centers within a region. Each Availability Zone is isolated from others to protect against failures.



# IAM - Identity and Access Management


## Introduction to AWS Identity and Access Management (IAM)
AWS Identity and Access Management (IAM) is a crucial service that enables secure control over access to AWS resources. IAM allows you to manage users, groups, roles, and policies to ensure a granular and secure access control model within your AWS environment.



## IAM Components

### IAM Users
IAM users represent individuals, employees, or systems interacting with your AWS environment. Each user has a unique set of security credentials for programmatic access and a password for console access. Users can be organized into groups, and permissions can be assigned directly to users or via group membership.

### IAM Groups

Groups are a way to organize IAM users. Instead of attaching policies directly to users, you can assign policies to groups. This simplifies the process of managing permissions, especially when dealing with multiple users who require similar access levels. Users can be members of multiple groups, making it flexible to assign permissions based on roles.

### IAM Policies

IAM policies are JSON documents that define permissions. Policies specify what actions are allowed or denied on what AWS resources. Policies can be attached to IAM users, groups, or roles. They follow the principle of least privilege, ensuring that users have the minimum permissions required to perform their tasks.

### IAM Roles

IAM roles are entities with policies that define what actions users, applications, or AWS services can perform. Roles are often used to grant temporary permissions to entities outside AWS, such as applications running on EC2 instances or Lambda functions. Roles can assume other roles, allowing for delegation of permissions.

### Best Practices

1) **Principle of Least Privilege:**
    - Grant only the permissions necessary to perform a task.

2) **Regular** Monitoring:
    - Regularly review IAM configurations to ensure they align with security policies.

3) **MFA** Usage:
    Enable Multi-Factor Authentication (MFA) for an additional layer of security.

4) **Policy Conditions**:
    Use policy conditions to add an extra layer of control based on contextual criteria.

5) **Credential Rotation**:
    - Implement automatic rotation of access keys and credentials.

## MFA Multi Factor Authentiaction


Multi-Factor Authentication (MFA) is a security feature in AWS that adds an extra layer of protection to user accounts. AWS supports various MFA device options for users to enable MFA on their accounts. 

1) **Virtual MFA Devices**
   - These are software-based MFA devices that run on a smartphone or tablet.
   - Common apps include Google Authenticator and Authy.
   - Users scan a QR code to set up the virtual MFA on their device.
2) **Hardware MFA Devices:**
    - Physical hardware tokens that generate MFA codes.
    - Users receive a physical device that they can use to generate MFA codes.
    - Examples include devices from Yubico and Gemalto.

3) **SMS Text Messages:**
    - Users receive MFA codes via SMS on their registered mobile phone.
    - This option is less secure than using a dedicated MFA device.

4) **U2F Security Keys:**

    - Universal Second Factor (U2F) security keys provide hardware-based authentication.
    - Users insert the key into their computer's USB port or use a Bluetooth connection.

## AWS access ways

1) **AWS Management Console:**

    - **Web-Based Interface:** The AWS Management Console is a web-based user interface that allows users to interact with AWS services using a web browser. It provides a visual way to manage and configure AWS resources.

2) **AWS Command Line Interface (CLI):**

    - **Command-Line Access:** The AWS CLI is a command-line tool that allows users to interact with AWS services using text-based commands. It   provides a powerful and scriptable interface for managing AWS resources.

3) AWS SDKs (Software Development Kits):

    - **Programmatic Access:** AWS provides SDKs for various programming languages, including Java, Python, Ruby, and more. Developers can use these SDKs to integrate AWS services into their applications.


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


# EC2 Instance Storage

## EBS Overview

Amazon Elastic Block Store (Amazon EBS) volumes are block-level storage devices that can be attached to Amazon EC2 instances. EBS provides persistent and high-performance block storage that is separate from EC2 instances. Here are key characteristics and features of EBS volumes:

1. **Block Storage:** EBS volumes are block-level storage devices that can be attached to EC2 instances. Each EBS volume appears as a raw block device to the instance, and you can format it with a file system of your choice.

2. **Persistent Storage:** EBS volumes persist independently from the life of an EC2 instance. This means that data on an EBS volume remains intact even if the associated EC2 instance is stopped or terminated.

3. **High Performance:** EBS volumes offer high and consistent performance for a variety of workloads. Different volume types are available to meet specific performance and cost requirements.

4. **Snapshots:** EBS volumes can be backed up by creating point-in-time snapshots. These snapshots are incremental backups and capture only the changed data since the last snapshot, making them efficient for backup and disaster recovery.

5. **Volume Types:**
   - **General Purpose (SSD):** Balanced performance for a wide range of workloads.
   - **Provisioned IOPS (SSD):** Designed for I/O-intensive workloads, providing predictable and high-performance storage.
   - **Throughput Optimized (HDD):** Low-cost magnetic storage with high throughput, suitable for large, sequential workloads.
   - **Cold HDD:** Lowest-cost magnetic storage designed for less frequently accessed data.

6. **Size and Performance:** EBS volumes come in different sizes, and their performance characteristics depend on the volume type. Larger volumes generally offer higher performance.

7. **Attachment and Detachment:** EBS volumes can be easily attached to and detached from EC2 instances. You can attach multiple volumes to an instance, and they can be moved between instances.

8. **Encryption:** EBS volumes can be encrypted to provide an additional layer of data security. Encryption is supported for both boot volumes and additional data volumes.

9. **Use Cases:** EBS volumes are suitable for a variety of use cases, including database storage, application storage, and providing additional block-level storage for EC2 instances.
10. **The EBS volume and the EC2** instance must be in the same Availability Zone for them to be directly attached.

When working with EC2 instances, you can choose the appropriate EBS volume type and size based on the performance requirements and characteristics of your applications. EBS volumes play a crucial role in providing scalable and durable block storage for EC2 instances in the AWS cloud.

Amazon EBS (Elastic Block Store) snapshots are point-in-time backups of your EBS volumes. They capture the data, configuration, and encryption status of a volume, providing a mechanism for data backup, recovery, and disaster preparedness. However, there isn't a direct concept of a "Recycle Bin" for EBS snapshots in the way it is commonly understood in desktop environments. Instead, let's discuss how EBS snapshots work and how you can manage them:

### EBS Snapshots Overview:

1. **Creation:**
   - You can create EBS snapshots manually or automate the process using AWS services like AWS Backup or by scripting with AWS CLI or SDKs.

2. **Incremental Backups:**
   - EBS snapshots are incremental, meaning that only the changes since the last snapshot are saved. This helps in optimizing storage and reducing costs.

3. **Data Lifecycle:**
   - Snapshots are independent of the EBS volumes they are created from. Even if an EBS volume is deleted, its snapshots persist, allowing you to recreate the volume.

4. **Volume Restoration:**
   - You can use an EBS snapshot to create a new EBS volume or restore an existing one to the state captured by the snapshot.

5. **Cross-Region Copy:**
   - EBS snapshots can be copied to different AWS regions, providing a mechanism for cross-region disaster recovery.

### Managing EBS Snapshots:

1. **Deletion:**
   - EBS snapshots can be deleted manually when they are no longer needed. However, be cautious, as deleted snapshots cannot be recovered.

2. **Lifecycle Policies:**
   - AWS provides Amazon Data Lifecycle Manager (DLM), which allows you to automate the creation, retention, and deletion of snapshots based on defined policies.

3. **Tagging:**
   - Tagging snapshots can help in organizing and identifying them. Tags can include information such as purpose, owner, or project.

4. **Monitoring:**
   - AWS CloudWatch can be used to monitor the status and performance of EBS snapshots, providing insights into the snapshot creation process.

Amazon Elastic File System (Amazon EFS) is a scalable and fully managed file storage service provided by Amazon Web Services (AWS). It is designed to provide scalable and shared file storage that can be easily mounted on multiple Amazon EC2 instances. Here's an overview of Amazon EFS:

1. **Fully Managed File Storage:**
   - Amazon EFS is a fully managed service, which means AWS takes care of the underlying infrastructure, storage capacity, and maintenance tasks. Users can focus on using and managing their files without worrying about the underlying hardware.

2. **Scalable and Elastic:**
   - EFS can automatically scale its capacity up or down as you add or remove files, providing elastic and scalable storage for your applications. It can grow to petabyte scale, accommodating the changing needs of your data.

3. **Shared File Storage:**
   - EFS allows multiple EC2 instances to mount and access the same file system concurrently. This makes it suitable for workloads that require shared access to files, enabling collaboration and data consistency.

4. **Compatibility:**
   - EFS supports the Network File System version 4 (NFSv4) protocol, making it compatible with a wide range of Linux-based applications and tools. It can be easily mounted on Linux-based EC2 instances.

5. **Performance:**
   - EFS provides low-latency performance for file operations, making it suitable for a variety of use cases, including content management systems, web serving, development environments, and more.

6. **Durability and Redundancy:**
   - Data stored in EFS is distributed across multiple Availability Zones within a region to provide high durability and availability. This design ensures that your data remains accessible even if one Availability Zone becomes unavailable.

7. **Security:**
   - EFS supports AWS Identity and Access Management (IAM) for access control, allowing you to manage permissions at the file system level. Additionally, data at rest can be encrypted using AWS Key Management Service (KMS) keys.

8. **Lifecycle Management:**
   - EFS provides lifecycle management features to automatically move files to lower-cost storage classes, helping optimize costs based on access patterns.

9. **Integration with AWS Services:**
   - EFS can be easily integrated with other AWS services such as Amazon EC2, AWS Lambda, and AWS Elastic Beanstalk. This enables seamless integration with various applications and services within the AWS ecosystem.

Amazon EFS is a versatile storage solution that caters to a wide range of use cases, particularly those requiring shared file storage with scalability and elasticity. Whether you're running web applications, content management systems, or development environments, EFS provides a scalable and managed file storage solution in the AWS cloud.

The shared responsibility model for AWS EC2 storage follows the broader AWS shared responsibility model, which outlines the division of security responsibilities between AWS (the cloud service provider) and the customer. Let's break down the shared responsibility model specific to AWS EC2 storage:

### AWS's Responsibilities:

1. **Physical Security:**
   - AWS is responsible for the physical security of the infrastructure, including data centers, where EC2 instances and their storage are housed.

2. **Hypervisor Security:**
   - AWS manages the security of the virtualization layer (hypervisor), which ensures the isolation of EC2 instances and their associated storage from other instances.

3. **Storage Infrastructure:**
   - AWS is responsible for the security, durability, and availability of the underlying storage infrastructure supporting EC2 instances. This includes services such as Amazon Elastic Block Store (EBS) and Amazon Elastic File System (EFS).

### Customer's Responsibilities:

1. **Data Management:**
   - Customers are responsible for managing their data stored on EC2 instances, including data classification, encryption, and access controls.

2. **Data Encryption:**
   - Customers are responsible for implementing encryption for data at rest and in transit. AWS provides tools and features such as AWS Key Management Service (KMS) to facilitate encryption.

3. **Access Controls:**
   - Configuring access controls, permissions, and identity management for EC2 instances and their storage is the responsibility of the customer. This involves using AWS Identity and Access Management (IAM) to control who can access what.

4. **Operating System Security:**
   - Customers are responsible for securing the operating system and applications running on EC2 instances. This includes patching, updates, and applying security best practices.

5. **Network Security:**
   - Configuring security groups, network access control lists (ACLs), and implementing network security measures are the customer's responsibility. This ensures that only authorized traffic is allowed to and from EC2 instances.

6. **Backup and Recovery:**
   - Implementing backup and recovery strategies for data on EC2 instances, including snapshots for Amazon EBS volumes, is the responsibility of the customer. This helps in ensuring data resilience and availability.

7. **Application Security:**
   - Customers are responsible for securing their applications running on EC2 instances, including code security, authentication, and authorization mechanisms.

By understanding and adhering to the shared responsibility model, customers can effectively secure their applications and data on AWS EC2 instances. It's essential to stay informed about AWS best practices and security features to maintain a robust and secure cloud environment.


Amazon FSx is a family of fully managed file storage services that makes it easy to set up, operate, and scale file storage in the AWS Cloud. The different variants within the Amazon FSx family include:

### 1. Amazon FSx for Lustre:

#### Overview:
- **Use Case:** Primarily designed for high-performance computing (HPC) workloads, machine learning, and analytics that require fast and scalable file systems.
- **File System Type:** Lustre, an open-source parallel file system.
- **Performance:** Provides high throughput and low-latency performance.
- **Integration:** Seamlessly integrates with other AWS services like Amazon S3 and AWS Identity and Access Management (IAM).

### 2. Amazon FSx for Windows File Server:

#### Overview:
- **Use Case:** Ideal for Windows-based applications and workloads that require native Windows file system features.
- **File System Type:** Windows Server Message Block (SMB) protocol-based file system.
- **Integration:** Easily integrates with Microsoft Active Directory for user authentication and access control.
- **Compatibility:** Supports Windows file system features like Access Control Lists (ACLs), symbolic links, and more.

### 3. Amazon FSx for NetApp ONTAP:

#### Overview:
- **Use Case:** Suited for business applications, databases, enterprise applications, and workloads requiring advanced data management capabilities.
- **File System Type:** Based on NetApp ONTAP technology.
- **Performance:** Offers high performance, scalability, and advanced data management features.
- **Integration:** Integrates with other AWS services and supports features like SnapMirror for data replication.

### Key Features Common to Amazon FSx Services:

1. **Fully Managed:**
   - AWS handles the operational aspects of the file system, including hardware provisioning, software configuration, maintenance, and updates.

2. **Highly Available:**
   - Designed for high availability across multiple Availability Zones (AZs) within an AWS region to ensure data durability and resilience.

3. **Scalable:**
   - Scales storage and throughput independently to meet the changing needs of your applications.

4. **Data Protection:**
   - Provides features such as automated backups, data replication, and data-at-rest encryption to enhance data protection.

5. **Integration with AWS Services:**
   - Integrates seamlessly with other AWS services, enabling you to build comprehensive solutions that meet specific application requirements.

Choosing the right variant of Amazon FSx depends on your specific use case, application requirements, and the protocols your applications use. Each variant is optimized for different scenarios, offering performance, scalability, and compatibility with specific file system types. Always refer to the official AWS documentation for the latest and most detailed information on each Amazon FSx variant.


## Summary

### Amazon Elastic Block Store (EBS):

- **Use Case:** EBS provides block-level storage volumes for use with Amazon EC2 instances.
- **Volume Types:**
  - **General Purpose (SSD):** Balanced performance for a wide range of workloads.
  - **Provisioned IOPS (SSD):** High-performance storage for I/O-intensive workloads.
  - **Throughput Optimized (HDD):** Low-cost magnetic storage with high throughput.
  - **Cold HDD:** Lowest-cost magnetic storage designed for less frequently accessed data.
- **Features:**
  - Snapshots for point-in-time backups.
  - Encryption for data at rest.
  - Volumes are attached to EC2 instances.
  - Suitable for databases, boot volumes, and applications requiring block-level storage.

### Amazon Elastic File System (EFS):

- **Use Case:** EFS provides scalable, shared file storage for use with Amazon EC2 instances.
- **File System Type:** Supports Network File System version 4 (NFSv4).
- **Features:**
  - Shared access to files across multiple EC2 instances.
  - Scalable storage capacity.
  - Integration with IAM for access control.
  - Suitable for content management, web serving, and development environments.
  - Automatic scaling of storage based on demand.

### Amazon FSx:

#### Amazon FSx for Lustre:

- **Use Case:** Designed for high-performance computing (HPC) workloads, machine learning, and analytics.
- **File System Type:** Lustre, an open-source parallel file system.
- **Features:**
  - High throughput and low-latency performance.
  - Integration with AWS services like S3.
  - Scalable storage for demanding workloads.

#### Amazon FSx for Windows File Server:

- **Use Case:** Ideal for Windows-based applications and workloads requiring native Windows file system features.
- **File System Type:** Windows Server Message Block (SMB) protocol-based file system.
- **Features:**
  - Native Windows compatibility.
  - Integration with Microsoft Active Directory.
  - Supports Windows file system features.

#### Amazon FSx for NetApp ONTAP:

- **Use Case:** Suited for business applications, databases, and workloads requiring advanced data management capabilities.
- **File System Type:** Based on NetApp ONTAP technology.
- **Features:**
  - High performance and scalability.
  - Advanced data management features.
  - Integration with other AWS services.

These services cater to different storage use cases, offering a range of features and performance characteristics. The choice depends on the specific requirements of your applications and workloads. Always refer to the official AWS documentation for the latest and most detailed information on each storage service.


# ELB & ASG - Elastic Load Balancing & Auto Scaling Groups

## Scaling

Horizontal scaling and vertical scaling are two approaches to adjusting the capacity or performance of a system, and they are often used in the context of load balancing and auto-scaling in cloud environments.

### Horizontal Scaling:

- **Description:**
  - Horizontal scaling involves adding more instances (or nodes) to a system to handle an increase in load or demand.
  - It is often associated with the use of auto-scaling groups, where additional instances are automatically added or removed based on predefined policies or conditions.

- **Key Characteristics:**
  - **Adding Instances:** When demand increases, new instances are added horizontally to distribute the load.
  - **Distributed Load:** Each instance added contributes to handling a portion of the overall load.
  - **Fault Tolerance:** Can enhance fault tolerance as workload is distributed across multiple instances.

- **Example:**
  - In an auto-scaling group, as the incoming traffic increases, new instances are automatically launched to share the load. When demand decreases, instances are terminated.

### Vertical Scaling:

- **Description:**
  - Vertical scaling involves increasing the resources (such as CPU, memory, or storage) of an existing instance to handle increased load.
  - It is often associated with modifying the characteristics of an individual instance rather than adding more instances.

- **Key Characteristics:**
  - **Increasing Resources:** Resources like CPU, RAM, or storage are increased on an existing instance.
  - **Single Instance:** The approach focuses on optimizing the performance of a single instance.
  - **Limited by Hardware:** The scalability is limited by the maximum capacity of the underlying hardware.

- **Example:**
  - Instead of adding more instances to handle increased load, you upgrade the resources (e.g., increase CPU or memory) of an existing instance.

### When to Use Each:

- **Horizontal Scaling:**
  - Effective for distributing load across multiple instances.
  - Well-suited for cloud environments with auto-scaling capabilities.
  - Enhances fault tolerance and availability.

- **Vertical Scaling:**
  - Appropriate when a single instance needs more resources.
  - Limited by the capacity of the underlying hardware.
  - Useful when the application is not designed for horizontal scaling.

In the context of Elastic Load Balancing (ELB) and Auto Scaling Groups (ASG) in AWS, both horizontal and vertical scaling play important roles. ASGs enable horizontal scaling by automatically adjusting the number of instances based on demand, while vertical scaling involves modifying the characteristics of individual instances within the ASG. The choice between horizontal and vertical scaling depends on factors such as application architecture, workload characteristics, and performance requirements.

Elastic Load Balancing (ELB) is a cloud service that automatically distributes incoming traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses. ELB helps distribute traffic evenly across your targets, improving application responsiveness and availability. It also monitors the health of your targets, and routes traffic only to the healthy targets. This helps ensure that your applications are available to users even if some of your targets are unavailable.

There are four main types of ELB load balancers:

* **Application Load Balancers (ALBs)**: ALBs route traffic based on the content of the request, such as the HTTP method, URL path, or headers. This makes ALBs a good choice for applications that use HTTP/HTTPS protocols.

* **Network Load Balancers (NLBs)**: NLBs route traffic based on the source IP address of the request. This makes NLBs a good choice for applications that use UDP or TCP protocols, or for applications that require low latency and high throughput.

* **Gateway Load Balancers (GLBs)**: GLBs route traffic between VPCs and on-premises networks. This makes GLBs a good choice for connecting your on-premises applications to your VPC-based applications.

* **Classic Load Balancers (CLBs)**: CLBs are the original type of ELB load balancer. They are still supported, but they are not recommended for new applications.

ELB can be used to load balance traffic for a variety of applications, including:

* **Web applications:** ELB can be used to distribute traffic across multiple web servers. This can help improve the performance and availability of your web applications.

* **Mobile backends:** ELB can be used to distribute traffic across multiple mobile backends. This can help improve the performance and availability of your mobile applications.

* **Microservices:** ELB can be used to distribute traffic across multiple microservices. This can help to improve the scalability and resilience of your microservices architectures.

ELB is a highly scalable and cost-effective solution for load balancing your applications. It is easy to use and configure, and it can be used with a variety of AWS services, including Amazon EC2, Amazon ECS, and Amazon EKS.

Here are some of the benefits of using ELB:

* **Improved application performance:** ELB can help to improve the performance of your applications by distributing traffic evenly across your targets. This can help to reduce latency and improve response times.

* **Increased application availability:** ELB can help to increase the availability of your applications by routing traffic only to healthy targets. This can help to ensure that your applications are available to users even if some of your targets are unavailable.

* **Scalability:** ELB can automatically scale to handle changes in traffic demand. This can help you to avoid the need to manually provision and manage load balancers.

* **Cost-effectiveness:** ELB is a cost-effective solution for load balancing your applications. You only pay for the traffic that you use, and there are no upfront costs.

If you are looking for a way to improve the performance, availability, and scalability of your applications, then Elastic Load Balancing (ELB) is a great option to consider.


Amazon EC2 Auto Scaling Groups (ASGs) in AWS provide a way to automatically scale the number of Amazon EC2 instances in a group based on demand or a predefined schedule. ASGs are a key component of building scalable, reliable, and cost-effective applications in the AWS cloud. Let's dive into an overview of Auto Scaling Groups and some common strategies for effective use:

### Overview of Auto Scaling Groups:

1. **Dynamic Scaling:**
   - Automatically adjusts the number of EC2 instances in a group based on demand or criteria specified in scaling policies.

2. **Availability and Fault Tolerance:**
   - Distributes instances across multiple Availability Zones (AZs) to ensure high availability and fault tolerance.

3. **Integration with Load Balancers:**
   - Integrates seamlessly with Elastic Load Balancing (ELB) to distribute traffic across instances.

4. **Launch Configurations and Launch Templates:**
   - Defines the configuration of EC2 instances, including the Amazon Machine Image (AMI), instance type, and key pair. Launch Templates provide a more flexible and feature-rich alternative.

5. **Health Checks:**
   - Monitors the health of instances and replaces unhealthy instances automatically.

6. **Scheduled Scaling:**
   - Allows scaling based on a predefined schedule, such as increasing the number of instances during peak hours and reducing them during off-peak hours.

7. **Mixed Instances Policy:**
   - Supports launching instances from multiple instance types to optimize cost and performance.

8. **Scaling Policies:**
   - Define scaling policies based on metrics like CPU utilization, network activity, or custom metrics.

9. **Cooldown Periods:**
   - Avoids unnecessary scaling activities by introducing a cooldown period after a scaling action.

### Auto Scaling Strategies:

1. **Dynamic Scaling (Based on Metrics):**
   - **Use Case:** Adjust the number of instances based on metrics like CPU utilization, network activity, or application-specific metrics.
   - **Strategy:** Define scaling policies that automatically add or remove instances based on the specified metric thresholds.

2. **Scheduled Scaling:**
   - **Use Case:** Plan for predictable traffic patterns by scheduling scaling activities.
   - **Strategy:** Set up scheduled actions to increase or decrease the desired capacity of the Auto Scaling Group at specific times.

3. **Manual Scaling:**
   - **Use Case:** Manually adjust the number of instances in response to specific events or situations.
   - **Strategy:** Use manual scaling to override automatic scaling and make immediate adjustments based on your operational needs.

4. **Mixed Instances Policy:**
   - **Use Case:** Optimize cost by launching instances from multiple instance types.
   - **Strategy:** Define a mixed instances policy specifying the instance types and weighting for each type.

5. **Instance Termination Policies:**
   - **Use Case:** Define criteria for selecting instances to terminate during a scale-in event.
   - **Strategy:** Specify termination policies to control which instances are terminated first, helping to optimize for various factors like cost or instance age.

6. **Lifecycle Hooks:**
   - **Use Case:** Perform actions before instances are launched or terminated.
   - **Strategy:** Use lifecycle hooks to perform custom actions, such as validating instances before they are put into service.

7. **Using Auto Scaling with Spot Instances:**
   - **Use Case:** Take advantage of cost savings offered by Spot Instances.
   - **Strategy:** Integrate with Spot Instances by configuring the Auto Scaling Group to use a mix of On-Demand and Spot Instances.

### Best Practices:

1. **Use Launch Templates:**
   - Leverage Launch Templates for flexibility and improved configuration management.

2. **Monitor and Set Alarms:**
   - Set up CloudWatch alarms to monitor key metrics and trigger scaling actions based on thresholds.

3. **Optimize Cooldown Periods:**
   - Adjust cooldown periods to prevent rapid and unnecessary scaling activities.

4. **Regularly Test Auto Scaling Policies:**
   - Simulate scaling events and test policies regularly to ensure they respond appropriately to changes in demand.

5. **Use Multiple AZs:**
   - Spread instances across multiple Availability Zones to enhance availability and fault tolerance.

6. **Understand Instance Termination Policies:**
   - Choose termination policies based on your priorities, such as cost savings or maintaining capacity.

Auto Scaling Groups are a fundamental building block for achieving elasticity and ensuring that your applications can automatically scale based on demand. By understanding the features, strategies, and best practices associated with Auto Scaling Groups, you can design resilient, cost-effective, and scalable architectures in the AWS cloud.

