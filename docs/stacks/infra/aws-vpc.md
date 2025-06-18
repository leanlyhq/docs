---
sidebar_label: AWS Virtual Private Cloud (VPC)
---

# AWS Virtual Private Cloud (VPC)

## VPC

Amazon Virtual Private Cloud (VPC) is a fundamental AWS networking service that enables you to create isolated, private network environments within the AWS cloud. It provides complete control over your virtual networking environment, including IP address ranges, subnets, route tables, and network gateways:

- **Network Isolation**: Create logically isolated sections of the AWS cloud where you can launch AWS resources in a virtual network that you define
- **Security Control**: Use security groups and network access control lists (ACLs) to control inbound and outbound traffic at the instance and subnet level
- **Multi-tier Applications**: Deploy web, application, and database tiers in separate subnets with different security requirements
- **Compliance**: Meet regulatory requirements by creating isolated network segments with specific security controls
- **Development and Testing**: Create isolated environments for development, testing, and production workloads

Whether you're building a simple web application or a complex enterprise architecture, AWS VPC provides the networking foundation you need to deploy your applications securely and efficiently in the cloud. The Leanly AWS VPC Stack enables you to deploy a production-ready VPC in just a few minutes.

### NAT Gateways

NAT Gateways enable resources in private subnets to connect to the internet for updates, patches, or external API calls while maintaining security by preventing inbound connections from the internet. This is essential for applications that need internet access for package management, software updates, or external service integration.

The Leanly AWS VPC Stack provides flexible NAT Gateway deployment options:

- **Optional Deployment**: NAT Gateways can be deployed optionally based on your workload requirements
- **Single NAT Gateway (not recommended for production workloads)**: Deploy one NAT Gateway to serve all private subnets, reducing costs
- **High Availability**: For production workloads, deploy NAT Gateways across multiple availability zones for redundancy

### Database Subnets Internet Access

> Attention: Not recommended for production workloads!

Database subnets are dedicated network segments designed specifically for database resources, providing enhanced security and high availability. These subnets are typically placed in private subnets to isolate database instances from direct internet access, ensuring data security while maintaining connectivity to application tiers.

For development purposes, you can enable direct database connectivity to allow access from your local development machine.

## Change Log

### 0.1.0 - Preview release
