<h1 align="center">AWS Project 2</h1>

## Project Title: AWS Data Analytic Platform for the City of Vancouver - Part 2
## Project Description:
- The City of Vancouver requires a robust and secure data platform to manage and monitor data associated with 3-1-1 inquiries
* This project aims to design and implement a Data Analytics Platform (DAP) using Amazon Web Services (AWS) to Data Protection, Governance, and Monitoring
## Project Objective:
- The City of Vancouver is implementing a Data Analytics Platform on AWS to enhance its 3-1-1 inquiry system. This initiative aims to improve data processing efficiency, enable real-time analytics, and optimize resource allocation for better service delivery. By leveraging cloud technology, the city seeks to transform its approach to managing citizen inquiries and ultimately enhance the overall quality of municipal services.
* Designing & Implementing DAP.
## Methodology:
* The process of providing Data Protection, Governance, and Monitoring for DAP designed as follows.
### 1. Data Protection
- The primary goal of this phase was to ensure data protection within the AWS S3 environment. The screenshots below demonstrate the configuration of security features such as bucket policies, encryption, and replication, which strengthen secure data management on the platform.
  
- Created a key for data protection in AWS using the Key Management Service (KMS). The key is named "Key_0797," I will use it for data encryption and decryption. It is a symmetric key.

![image](https://github.com/user-attachments/assets/a0331a1b-2f91-4883-ba7c-b24ebf1d87e4)
![image](https://github.com/user-attachments/assets/b61298fb-f910-4f22-8046-7cd0d5015264)
![image](https://github.com/user-attachments/assets/de31069f-91bf-4d95-a515-b2424376dfea)

The images above show the key used for data protection in my project. The registered project name for the key is "key_0797." The encryption settings are configured to enable default encryption for the bucket using an AWS Key Management Service (KMS) key, ensuring that any new items added to the bucket are automatically encrypted. Additionally, I have created a backup folder where the data backup will be stored.	


### 2. Data Governance
- AWS CloudTrail was employed to monitor and log all API requests and changes in the AWS environment. AWS Glue and S3 were used to ensure proper resource utilization and restricted access to sensitive data.

![image](https://github.com/user-attachments/assets/492fe52b-584f-400a-88d9-aef0a4e602b9)
![image](https://github.com/user-attachments/assets/ace9e656-13b4-49bf-b135-515d78871273)

- Created a pipeline incorporating an S3 bucket for data storage using AWS Glue. I also implemented a detection system to identify suspicious data using Canadian example data. Afterward, I used the Evaluate Data Quality feature within the ETL pipeline. I applied row-level transformations to modify the data, using a conditional router to filter the data based on specific conditions. Additionally, a schema was applied to remove extra columns added during the row-level transformation stage. Finally, the processed data was saved in the Trusted folder using the S3 service.

![image](https://github.com/user-attachments/assets/d261b178-08f5-4148-acec-af5b31f61e5e)

### 3. Data Monitoring
* AWS CloudWatch was set up to monitor the system's health and consumption statistics. A personalized dashboard tracked key metrics such as:
- Estimated Costs: Monitored the cost of AWS services used.
- Number of Objects: Tracked the total number of objects in the S3 bucket.
An alarm system was also configured to send notifications if any predefined thresholds were exceeded.

![image](https://github.com/user-attachments/assets/51eb601a-4c8d-4183-9ffd-c498ae1addbd)

The dashboard, named "group2-govfin-311iv-dashboard-arun," was set up using CloudWatch. The first graph shows the estimated costs, while the second displays the number of objects. Additionally, I demonstrated an alarm configured within the system, which sends an email notification when a certain threshold is exceeded.



