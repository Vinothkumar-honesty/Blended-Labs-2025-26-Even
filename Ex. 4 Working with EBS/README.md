# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: VINOTHKUMAR R
* **Register Number**: 212224040361
* **Date of Submission**: 27.02.2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

First, I logged in to the AWS Management Console.

I navigated to the EC2 Dashboard.

I explored the Elastic Block Store (EBS) section under EC2.

I observed different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

I clicked on “Volumes” and selected “Create Volume.”

I chose the required volume type (General Purpose SSD – gp3).

I entered the desired storage size (for example, 8 GB).

I selected the same Availability Zone as my running EC2 instance.

I clicked on “Create Volume” to create the EBS volume.

After the volume was created, I selected the volume and clicked on “Attach Volume.”

I selected my running EC2 instance and attached the volume as a new device (for example, /dev/xvdf).

I connected to my EC2 instance using SSH from the terminal.

I checked the attached disk using the command lsblk to verify the new volume.

I formatted the attached volume using the command:
sudo mkfs -t ext4 /dev/xvdf

I created a directory to mount the volume using:
sudo mkdir /mnt/ebs

I mounted the volume to the directory using:
sudo mount /dev/xvdf /mnt/ebs

I verified that the volume was mounted successfully using the df -h command.

I created sample files inside the mounted directory using:
sudo touch /mnt/ebs/sample.txt

I stored some sample data inside the file.

I rebooted the EC2 instance from the AWS Console.

After rebooting, I reconnected to the instance using SSH.

I checked the mounted directory and verified that the stored data was still available.

This confirmed that the EBS volume provides persistent storage even after instance reboot.

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="954" height="1028" alt="Screenshot 2026-02-27 163032" src="https://github.com/user-attachments/assets/63a17edf-2eed-4503-846f-6487983252a2" />

---

### Screenshot 2: EBS Volume Attached to EC2

<img width="956" height="1031" alt="Screenshot 2026-02-27 163200" src="https://github.com/user-attachments/assets/6025133c-23a2-45a0-9cae-1a1f5797f368" />
<img width="960" height="1044" alt="Screenshot 2026-02-27 163520" src="https://github.com/user-attachments/assets/20ef1511-245f-427a-abd6-db6196d7b5fb" />

---

### Screenshot 3: Mounted Volume with Data
<img width="957" height="1048" alt="Screenshot 2026-02-27 163744" src="https://github.com/user-attachments/assets/7a793991-2afe-407d-bd53-e8d7173d9a01" />
<img width="959" height="1046" alt="Screenshot 2026-02-27 164037" src="https://github.com/user-attachments/assets/db550deb-7b7d-415a-909e-a2713bce2126" />


---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
