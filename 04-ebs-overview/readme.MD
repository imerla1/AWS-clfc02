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