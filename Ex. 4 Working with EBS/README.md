# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Sushmitha Gembunathan 
* **Register Number**: 212224040342
* **Date of Submission**: 27/02/26

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

1. Logged in to the AWS Management Console and navigated to the EC2 Dashboard.
2. Explored the Elastic Block Store (EBS) section and reviewed available volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.
3. Created a new EBS volume by selecting the gp3 type, specifying the required storage size, and choosing the same Availability Zone as the running EC2 instance.
4. Attached the newly created volume to the running EC2 instance as a secondary device.
5. Connected to the EC2 instance using SSH and verified the attached disk using the lsblk command.
6. Formatted the new volume with the ext4 file system, created a mount directory, and mounted the volume to the instance.
7. Verified the successful mount using the df -h command and created sample files in the mounted directory to store test data.
8. Rebooted the EC2 instance, reconnected via SSH, and confirmed that the mounted volume and stored data were still available.
9. Validated that the EBS volume provides persistent storage across instance reboots.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1920" height="1200" alt="Screenshot 2026-02-27 211918" src="https://github.com/user-attachments/assets/f92bf0d7-b621-42c0-805f-0b2e6a92178f" />


---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1920" height="1200" alt="Screenshot 2026-02-27 212531" src="https://github.com/user-attachments/assets/62bc597d-2c03-4d8c-af0c-b300963c96ec" />

<img width="1920" height="1200" alt="Screenshot 2026-02-27 213002" src="https://github.com/user-attachments/assets/5a8bc6f8-3db7-4ac1-8dff-4677e0b494f7" />

<img width="1920" height="1200" alt="Screenshot 2026-02-27 212422" src="https://github.com/user-attachments/assets/7cfeab73-2ef5-4a6d-8b3c-cd80d37b8f7e" />


---

### Screenshot 3: Mounted Volume with Data

<img width="1920" height="1200" alt="Screenshot 2026-02-27 213205" src="https://github.com/user-attachments/assets/7c52450b-d6f9-4e91-ad32-395715dd4702" />

<img width="1920" height="1200" alt="Screenshot 2026-02-27 213614" src="https://github.com/user-attachments/assets/cf7ec8ca-a556-49ec-ac6a-b60b6e3e9cef" />



---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
