# Highly Available Web Application

## AWS Capstone Project

**Undertaken at QwikSkills**  
**By: Vivek Singh**  
**Guided By: Mr. Suraj Verma**  
**Date: November 2023**

## Declaration

I, Vivek Singh, a student of the AWS Essentials Program, declare that the project report submitted by me is a bona fide work for the partial fulfilment of the requirement of the AWS Essentials project work. I have incorporated all the suggestions provided by my guide from time to time.

I further declare that to the best of my knowledge this dissertation contains my original work and does not contain any part of any work which has been submitted for any work entitlement either in this organisation or in any other university/Deemed university/institute organisation etc. without proper citation, and I shall be fully responsible for any plagiarism found at any stage.

---

**Signature:**

![image2](https://github.com/vivek2431/AWS-Highly-Available-Web-Application---Capstone-Project/assets/137812531/4a6115e7-8685-4aa6-991a-824b21231c01)

**Name:** Vivek Singh

## Capstone Project Approval Certificate

---

This is to certify that Mr/Ms. [Your Name], a student of "AWS Essentials" at QwikSkills, has successfully completed the project work entitled "Highly Available Web Application" as per guidance. I have thoroughly assessed the progress of the work and reviewed the end result. The student has incorporated all the suggestions provided by instructors in this dissertation. This dissertation is a bona fide piece of work of the standard of capstone project work carried out by the student under instructor’s supervision. Internal examination has been successfully completed.

---

**Name:** Mr. Suraj Verma  
**Designation:** AWS Cloud Engineer

## Table of Contents

1. [Introduction](#introduction)
2. [Background](#background)
3. [Requirements](#requirements)
4. [Overview](#overview)
5. [Description](#description)
6. [Data Flow Diagrams (DFD)](#data-flow-diagrams-dfd)
7. [Flowchart (Modules & Sub-Modules)](#flowchart-modules--sub-modules)
8. [Data Description (E-R diagrams)](#data-description-e-r-diagrams)
9. [Sample Code](#sample-code)
10. [Screenshots](#screenshots)
11. [Conclusion](#conclusion)
12. [Salient Features](#salient-features)
13. [Future Scope](#future-scope)
14. [Bibliography/References](#bibliographyreferences)

# Introduction

## Cloud Computing

Cloud computing is a model for enabling ubiquitous, convenient, on-demand network access to a shared pool of configurable computing resources (for example networks, servers, storage, applications, and services) that can be rapidly provisioned and released with minimal management efforts or service provider interaction.

Cloud computing is the on-demand delivery of computing services over the internet. These services include servers, storage, databases, networking, software, analytics, and intelligence. Instead of buying, owning, and maintaining physical data centres and servers, you can access technology services as needed, from anywhere in the world.

 **Architecture represents the cloud computing**
 
![image4](https://github.com/vivek2431/AWS-Highly-Available-Web-Application---Capstone-Project/assets/137812531/2ec0827d-1bd3-4bdf-87f4-a2ce97f7eb65)

# Components and Concepts of Cloud Computing

## 1. Service Model

### Infrastructure as a Service (IaaS)

Infrastructure as a Service (IaaS) is a cloud computing model that provides virtualized computing resources over the internet, allowing users to rent virtual machines, storage, and networking components. It eliminates the need for organizations to invest in and maintain physical hardware, as the cloud provider manages and maintains the underlying infrastructure. IaaS is particularly beneficial for businesses that require a dynamic and cost-effective solution, allowing them to focus on application development without the burden of hardware management. IaaS is a key component of the cloud computing ecosystem.

**For Example:** Amazon Web Services (AWS) provides EC2 virtual servers.

### Platform as a Service (PaaS)

Platform as a Service (PaaS) is a cloud computing model that simplifies the development, deployment, and management of applications without the need for infrastructure management. It offers a ready-made environment with tools like development frameworks, databases, and middleware, streamlining the process. PaaS allows developers to focus on code and functionalities, accelerating the development lifecycle. It promotes collaboration, enhances scalability, and ensures seamless integration with other cloud services. PaaS is advantageous for businesses seeking an agile and cost-effective solution, eliminating the need for infrastructure management. It allows developers to focus on core competencies, increasing efficiency and faster time-to-market.

**For Example:** Google’s Cloud App Engine.

### Software as a Service (SaaS)

Software as a Service (SaaS) is a cloud computing model that simplifies software delivery and consumption by hosting and maintaining applications by a third-party provider. This model eliminates the need for users to install, update, or manage the application, streamlining deployment and reducing upfront costs. SaaS applications cover various functionalities, from office productivity tools like Google Workspace to CRM systems like Salesforce. The scalability, flexibility, and cost-effectiveness of SaaS make it a popular choice for businesses, allowing them to focus on core operations while utilizing powerful, always-updated software solutions.

**For Example:** Gmail, Microsoft Office 365, and Salesforce.

## 2. Deployment Models

### Private Cloud

A private cloud is a cloud computing environment for a single organization, offering exclusive use and control over resources. Hosted on-premises or by a third-party service provider, it provides increased security, customization, and compliance adherence. Ideal for industries with stringent data privacy and regulatory requirements, private clouds require substantial initial investment and ongoing maintenance but offer greater control over infrastructure, ensuring tailored solutions.

**For Example:** VMware and VCloud.

### Public Cloud

A public cloud is a model where third-party providers offer computing resources like virtual machines and storage over the internet on a pay-as-you-go basis. Providers like AWS, Microsoft Azure, and Google Cloud Platform provide high scalability, cost efficiency, and broad accessibility. Public clouds are ideal for variable workloads, development environments, and applications with less sensitive data, minimizing upfront hardware investment and allowing users to scale resources according to demand.

**For Example:** AWS, Microsoft Azure, Google Cloud.

### Hybrid Cloud

Hybrid cloud is a computing model that combines private and public clouds, allowing data and applications to be shared. It offers flexibility, scalability, cost efficiency, and seamless data portability. This model is beneficial for businesses with fluctuating workloads, regulatory compliance concerns, or balancing control and scalability. Effective management and integration tools are essential for smooth operation in a hybrid cloud environment.

**For Example:** AWS Outposts, Azure Stack Arc, Google Anthos.

## Amazon Web Services(AWS)

Amazon Web Services (AWS) is a comprehensive cloud computing platform offered by Amazon.com. It provides a wide array of cloud services, including computing power, storage, databases, machine learning, analytics, content delivery, Internet of Things (IoT), and more. AWS allows organizations and individuals to access and use these services over the internet, providing flexibility, scalability, and cost-effectiveness for a wide range of applications and workloads.

![image5](https://github.com/vivek2431/AWS-Highly-Available-Web-Application---Capstone-Project/assets/137812531/75cf6957-f480-43a7-b92f-c7c7cea3611c)

## Key Components and Ideas of AWS

### 1. Compute Services
AWS offers a variety of compute services to meet different needs:
- **Amazon EC2 (Elastic Compute Cloud)**: Provides virtual servers.
- **AWS Lambda**: Enables serverless computing.
- **AWS Elastic Beanstalk**: Simplifies application deployment.

### 2. Storage Services
AWS provides scalable storage solutions:
- **Amazon S3 (Simple Storage Service)**: For object storage.
- **Amazon EBS (Elastic Block Store)**: For block storage.
- **Amazon Glacier**: For long-term archival storage.

### 3. Database Services
Fully managed database services offered by AWS:
- **Amazon RDS (Relational Database Service)**: For relational databases.
- **Amazon DynamoDB**: For NoSQL databases.
- **Amazon Aurora**: High-performance databases.

### 4. Networking
Networking services available on AWS:
- **Amazon VPC (Virtual Private Cloud)**: For creating isolated networks.
- **AWS Direct Connect**: For dedicated network connections.
- **Amazon Route 53**: Domain Name System (DNS) management.

### 5. Content Delivery and CDN
- **Amazon CloudFront**: Content delivery network service that accelerates delivery of websites, APIs, and streaming content globally.

### 6. IoT (Internet of Things)
- **AWS IoT**: Provides secure, scalable connectivity between IoT devices and the cloud, enabling device management, data processing, and interaction with other AWS services.

### 7. Analytics and Big Data
Services for big data processing and real-time data streaming:
- **Amazon EMR (Elastic MapReduce)**: Big data processing.
- **Amazon Kinesis**: Real-time data streaming.
- **Amazon Redshift**: Data warehousing solutions.

### 8. Machine Learning and AI
- **Amazon SageMaker**: For building, training, and deploying machine learning models.
- **Amazon Rekognition**: Image and video analysis.

### 9. Security and Identity
- **AWS Identity and Access Management (IAM)**: Controls access to your resources securely.
- Various security services and compliance options are available to ensure the protection of your data and applications.

### 10. Management and Monitoring
- **Amazon CloudWatch**: Monitoring service.
- **AWS CloudFormation**: Infrastructure as code.
- **AWS Trusted Advisor**: Resource optimization.

### 11. Developer Tools
Support for continuous integration and continuous delivery (CI/CD) workflows:
- **AWS CodeBuild**
- **AWS CodeDeploy**
- **AWS CodePipeline**

### 12. Migration and Transfer
Tools for migrating on-premises applications to the cloud:
- **AWS Database Migration Service**
- **AWS Server Migration Service**

### 13. Elasticity and Scalability
AWS services are designed to scale on demand, allowing you to adjust resources based on your needs and pay only for what you use.

### 14. Global Reach
AWS has data centers in multiple regions worldwide, enabling you to deploy applications and data close to your users for improved performance and redundancy.

### 15. Pricing Model
AWS offers a pay-as-you-go pricing model, making it cost-effective and scalable for businesses of all sizes.

---

# Background

Amazon Web Services (AWS), a subsidiary of Amazon.com, is a leading cloud computing platform that offers a range of services including computing power, storage, databases, machine learning, and analytics. Launched in 2006, AWS provides a scalable and cost-effective alternative to traditional on-premises infrastructure. With a global network of data centres, AWS has become popular among startups, enterprises, and government organizations. Its pay-as-you-go pricing model and extensive service offerings have made it a key player in digital transformation, innovation, and scalability for businesses across various industries. AWS caters to a diverse range of needs, from hosting simple websites to running complex machine learning algorithms and big data analytics.

Adam Selipsky, the CEO of Amazon Web Services (AWS), has led the company from a start-up to a multi-billion-dollar business. AWS began working on its cloud computing platform in the early 2000s, under the project code-named "Project A1." In 2002, foundational services like storage and compute were developed. AWS officially launched on March 14, 2006, with services like Amazon S3 and Amazon EC2. During the COVID-19 pandemic, AWS played a crucial role in supporting organizations by scaling their infrastructure for remote work and increased online demand. The company expanded its offerings in containers with Amazon EKS and server-less with AWS Lambda, allowing developers to build and deploy applications more efficiently. AWS also introduced the AWS Marketplace for third-party software and services. In 2021-2022, AWS launched Amazon Bracket, a quantum computing service, and committed to reducing its carbon footprint and achieving sustainability goals.


# Requirements

To launch a highly available web application on AWS, you need the following components and configurations:

### 1. Authorized AWS Account
Ensure you have an authorized AWS account with adequate permissions to configure and provide a robust highly available web application.

### 2. Multiple Availability Zones
Deploy your application across multiple AWS Availability Zones (AZs) within a region. This ensures that if one AZ experiences issues, your application can continue running in another AZ.

### 3. AWS VPC (Virtual Private Cloud)
Configure a new VPC with the following components:
- **Public Subnets**: For public-facing resources.
- **Internet Gateway**: To allow internet access.
- **Route Table**: To manage traffic routing within the VPC.

### 4. AWS EC2 (Elastic Cloud Compute)
- **Launch Template**: Create a launch template for EC2 instances.
- **Auto Scaling Group**: Set up an Auto Scaling group to manage instance scaling.
- **Elastic Load Balancer (ELB)**: Distribute traffic across multiple instances using one of the following:
  - Classic Load Balancer
  - Application Load Balancer
  - Network Load Balancer

### 5. Auto Scaling
Set up Auto Scaling groups to automatically adjust the number of instances in response to traffic demands. This helps ensure that your application can handle increased loads without manual intervention.

### 6. Amazon RDS Multi-AZ
If you use a relational database, configure Amazon RDS with Multi-AZ deployment for high availability. This replicates your database to a standby instance in another AZ for failover.

### 7. Security
Implement security best practices, including:
- **AWS Identity and Access Management (IAM)**: Manage user permissions and access.
- **Network Security Groups (NSGs)**: Control inbound and outbound traffic to your resources.
- **Encryption**: Ensure data is encrypted both at rest and in transit.

### 8. Content Delivery
Use Amazon CloudFront for content delivery. CloudFront is a content delivery network (CDN) that caches your content at edge locations, reducing latency and increasing availability.

### 9. Amazon S3 for Static Assets
Store static assets (e.g., images, CSS, JavaScript) in Amazon S3 for durability and scalability. You can also use S3 to host static websites.

### 10. High Availability Databases
Consider services like Amazon RDS, which provides high availability and scalability out of the box.

### 11. Monitoring and Alerts
Set up AWS CloudWatch for monitoring your resources and creating alarms for automated responses. CloudWatch can also be integrated with AWS Lambda for auto-scaling or other automated actions.

## Overview

AWS offers a wide range of services that can be used to build a scalable, resilient, and highly available web/application server. By leveraging services like Elastic Load Balancer (ELB), Auto Scaling, Elastic Compute Cloud (EC2), Simple Storage Service (S3), Relational Database Service (RDS), CloudFront, Virtual Private Cloud (VPC), and other AWS services, you can build a highly available and scalable infrastructure for your web server.

## Infrastructure Components

### 1. Amazon VPC (Virtual Private Cloud)
Create an Amazon VPC to host your infrastructure, ensuring isolation and control over your network environment.

### 2. Public Subnets
Create public subnets in different Availability Zones (AZs) to ensure high availability and redundancy, following AWS best practices.

### 3. Internet Gateway
Route public subnets through an Internet Gateway to allow inbound and outbound internet traffic.

### 4. Elastic Load Balancer (ELB)
Create an Application Load Balancer (ALB) to distribute incoming traffic across multiple EC2 instances running in your public subnets.

### 5. Auto Scaling Group
Configure an Auto Scaling Group to automatically launch new EC2 instances in response to changing traffic demands on the application, ensuring scalability and high availability.

### 6. Amazon RDS
Use Amazon RDS, a managed database service that provides high availability and scalability. Configure the RDS instance to run in a Multi-AZ configuration to automatically replicate data to a standby instance in a different AZ.

### 7. Amazon S3 and CloudFront
- Use Amazon S3 to store static content, such as images and videos.
- Serve static content through Amazon CloudFront, a global content delivery network (CDN), to ensure high availability, scalability, and low latency delivery to customers around the world.

### 8. AWS CloudWatch
Monitor performance metrics and cost usage of your resources with AWS CloudWatch. Set up notifications for when thresholds are exceeded.

### 9. AWS CloudTrail
Use AWS CloudTrail to store records of every event and API call logs on your AWS account for auditing and monitoring purposes.

Finally, AWS offers a powerful set of services that can be used to build a resilient, highly available and scalable web application server. By leveraging services like ELB, Auto Scaling, EC2, RDS, S3, and Cloud Front and so on, we can build an infrastructure that can handle high traffic and data processing requirements while maintaining high availability and scalability when properly configured, following AWS best practices.

## Description

AWS offers a wide range of services that can be used to build a scalable, resilient, and highly available web/application server. By leveraging services like Elastic Load Balancer (ELB), Auto Scaling, Elastic Compute Cloud (EC2), Simple Storage Service (S3), Relational Database Service (RDS), CloudFront, Virtual Private Cloud (VPC), and other AWS services, you can build a highly available and scalable infrastructure for your web server.

## Infrastructure Components

### 1. EC2 Instances
The first module comprises launching and configuring EC2 Instances to host the web application. EC2 instances are cloud-based virtual servers that supply computing resources. By launching multiple instances, we can distribute the workload and ensure availability even if a single instance fails. The configuration includes:
- Selecting the right Amazon Machine Image (AMI)
- Choosing instance type
- Setting storage options
- Configuring security settings
- Networking options such as VPC and subnets
- Adding additional storage volumes if needed

### 2. RDS Setup
The second segment focuses on configuring Amazon RDS to provide the web application with a managed database service. Amazon RDS is a reliable and scalable database service. This phase includes:
- Selecting the database engine (e.g., MySQL)
- Configuring instance parameters such as instance type, storage, and connectivity options
- Setting up the database's login, password, and authentication
- Configuring backup and maintenance options to ensure data durability and availability

### 3. Auto Scaling Group Configuration
This module creates an Auto Scaling group to automatically adjust EC2 instances based on demand. It ensures the application can handle varying traffic loads without manual intervention. The configuration includes:
- Creating scaling strategies based on CPU usage or network traffic
- Defining minimum, maximum, and desired capacity of instances
- Setting cooldown periods and notifications

### 4. Load Balancer Setup
The fourth component deals with configuring an Elastic Load Balancer to distribute incoming traffic across the EC2 instances. This improves the web application's availability and fault tolerance by ensuring no single instance becomes overloaded. The configuration includes:
- Selecting the appropriate load balancer type (Application Load Balancer or Network Load Balancer)
- Setting load balancer parameters such as listener ports and protocols
- Configuring SSL certificates if necessary
- Setting up availability zones and subnets
- Defining health checks to monitor the EC2 instances' health

### 5. CloudTrail Creation
CloudTrail enables tracking and logging of AWS API calls performed within the AWS account. It provides comprehensive records of actions carried out by users, services, or resources. CloudTrail is configured to store logs on Amazon S3, providing a long-term and scalable storage solution for log data.

### 6. S3 Usage
Amazon S3 is used for storing the CloudTrail logs produced by the web application. It ensures that log data is consistently saved and readily accessible by other AWS services, especially CloudWatch.

### 7. CloudWatch Utilization
AWS CloudWatch collects and tracks metrics, logs, and events from various AWS resources. In this project, CloudWatch is set up to retrieve logs from the S3 bucket where CloudTrail logs are maintained. It can detect if any EC2 instances in the application are terminated by monitoring these logs, allowing for preemptive actions to ensure the application's high availability.

### 8. SNS Alerts
SNS (Simple Notification Service) sends alerts to subscribed endpoints or clients. When CloudWatch detects a stopped EC2 instance, SNS is used to send email alerts to a specified destination. Integrating SNS with CloudWatch helps quickly alert the appropriate parties and take suitable actions to resolve any potential issues, ensuring the availability and reliability of the online service.

## Data Flow Diagram (DFD)

![image6](https://github.com/vivek2431/AWS-Highly-Available-Web-Application---Capstone-Project/assets/137812531/98745008-78a0-4895-bef0-cc461a686d82)

## Flowchart(Modules and Submodules) 

![image7](https://github.com/vivek2431/AWS-Highly-Available-Web-Application---Capstone-Project/assets/137812531/f34d192d-54ab-4e0c-a930-40dad96450cc)

## Data Description (E-R Diagram)

![image8](https://github.com/vivek2431/AWS-Highly-Available-Web-Application---Capstone-Project/assets/137812531/bbac61fb-39e0-4b3a-b875-c70be2d5b90a)


# Sample Code


## AWS RDS and EC2 Integration

This repository contains scripts to set up an AWS RDS instance, connect to it from an EC2 instance, insert dummy data, and fetch it using an Apache server.

## Prerequisites

- AWS EC2 instance
- AWS RDS instance
- MySQL client on EC2
- Apache server on EC2

### Script 1: RDS connection from EC2

```bash
#!/bin/bash
# Update and install MySQL client
sudo apt update
sudo apt-get install mysql-client -y
```

# Verify MySQL client installation
```mysql --version```

# Connect to RDS instance (replace with your actual endpoint, username, and password)
```mysql -h mydatabase.c5wym6zs3no9.us-east-1.rds.amazonaws.com -P 3306 -u admin -p```
# Enter password: admin123

### Script 2: RDS dummy data insertion
```
#!/bin/bash
# MySQL connection details
host="mydatabase.c5wym6zs3no9.us-east-1.rds.amazonaws.com"
username="admin"
password="admin123"
database="mydatabase"
```
# SQL query to create table
`create_table_query="CREATE TABLE IF NOT EXISTS Family (id INT PRIMARY KEY, name VARCHAR(50));"`

# SQL query to insert dummy data
`insert_data_query="INSERT INTO Family (id, name) VALUES (1, 'Saurabh'), (2, 'Nishant'), (3, 'Rohit'), (4, 'Azruddin');"`

# Connect to MySQL and execute queries
```mysql -h $host -u $username -p$password -D $database -e "$create_table_query" && \
mysql -h $host -u $username -p$password -D $database -e "$insert_data_query"

echo "Table created with dummy data."
```
### Apache server fetches data from RDS
```
#!/bin/bash
# Database configuration
host="mydatabase.c5wym6zs3no9.us-east-1.rds.amazonaws.com"
username="admin"
password="admin123"
database="mydatabase"
table="Family"
```
# Install required packages
```
sudo apt update
sudo apt install -y apache2 php libapache2-mod-php php-mysql

# Create a PHP script to fetch data from the database
sudo tee /var/www/html/index.php >/dev/null <<EOF
<?php
\$conn = new mysqli("$host", "$username", "$password", "$database");
if (\$conn->connect_error) {
    die("Connection failed: " . \$conn->connect_error);
}
\$sql = "SELECT * FROM $table";
\$result = \$conn->query(\$sql);
if (\$result->num_rows > 0) {
    echo "<table><tr><th>ID</th><th>Name</th></tr>";
    while(\$row = \$result->fetch_assoc()) {
        echo "<tr><td>" . \$row["id"] . "</td><td>" . \$row["name"] . "</td></tr>";
    }
    echo "</table>";
} else {
    echo "0 results";
}
\$conn->close();
?>
EOF
```
# Configure Apache to serve PHP files
`sudo sed -i "s/index.html/index.php/g" /etc/apache2/mods-enabled/dir.conf`

# Restart Apache
`sudo systemctl restart apache2`

# Display public IP
`echo "Web application is now accessible at: http://$(curl -s ifconfig.me)"`

### Usage
Connect to your EC2 instance.
- Run Script 1 to install the MySQL client and connect to your RDS instance.
- Run Script 2 to create a table and insert dummy data into your RDS instance.
- Run Script 3 to set up an Apache server, create a PHP script to fetch data from your RDS instance, and display the public IP of your 
  EC2 instance.











 

