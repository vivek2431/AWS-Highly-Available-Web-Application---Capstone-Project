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
`


 

