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

Auto Scaling Groups are a fundamental building block for achieving elasticity and ensuring that your applications can automatically scale based on demand. By understanding the features, strategies, and best practices associated with Auto Scaling Groups, you can design resilient, cost-effective, and scalable architectures in the AWS cloud.1