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