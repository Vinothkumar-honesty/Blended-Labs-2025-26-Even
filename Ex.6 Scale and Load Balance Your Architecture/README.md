# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture
Author : your name   Reg no : yours   Date :

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

First, I reviewed the existing EC2 architecture that was created in previous experiments to understand how the application was deployed and how instances were configured.

Next, I created a Launch Template by selecting the required AMI, instance type, key pair, and security group. I also added user data to automatically install and run the application when the instance starts.

After that, I created an Auto Scaling Group using the launch template. I configured the minimum, maximum, and desired number of instances to ensure the application can scale automatically based on demand.

Then, I set up an Application Load Balancer (ALB) to distribute incoming traffic across multiple EC2 instances. I also created a target group and configured health checks to monitor instance status.

Next, I attached the Auto Scaling Group to the target group so that all instances created by the scaling group can receive traffic through the load balancer.

After that, I configured scaling policies using Amazon CloudWatch. I set rules to automatically increase or decrease the number of instances based on CPU utilization.

Finally, I tested the setup by generating traffic to the application and observed how the load balancer distributed traffic and how the Auto Scaling Group automatically added or removed instances based on demand.

## Output Screenshots 


---
<img width="1174" height="1045" alt="Screenshot 2026-03-18 135022" src="https://github.com/user-attachments/assets/4016a85d-078c-45ee-ba00-aeffcbb00299" />
<img width="1171" height="975" alt="Screenshot 2026-03-18 135950" src="https://github.com/user-attachments/assets/e3b2ade8-f8a4-4633-8dbc-0924260e5628" />

<img width="953" height="990" alt="Screenshot 2026-03-20 152803" src="https://github.com/user-attachments/assets/b1982761-6df7-47b2-8cc8-2301858d5338" />
<img width="928" height="910" alt="Screenshot 2026-03-20 153318" src="https://github.com/user-attachments/assets/2ec448e4-9605-4f70-97c0-7c626fc538f0" />

<img width="1230" height="1043" alt="Screenshot 2026-03-20 154343" src="https://github.com/user-attachments/assets/7c1ad99b-b42d-40fc-ba33-3b3adceab792" />


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
