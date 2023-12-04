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