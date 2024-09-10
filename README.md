# <font color="green">Projects</font>

Different types of analysis carried out for the two projects are detailed below:
- Data Analytic Platform for the ***University Canada West***
- Data Analytic Platform for the ***City of Vancouver***
 
## <font color="blue">Project 1: Data Analytic Platform for the University Canada West</font>

### *Background:*
The University Canada West is an Educational Institution focused on providing high-quality eduction for which gathering, collecting and storing information generated from it operational activities is essential to obtain statistics. However, all this data needs to be processed in order to obtain valuable insights that allow the UCW to maintain its high-quality education.

### *Goal:*
Improve the performance of the Prior Learning Assessment and Recognition procedure of the registrar's office at UCW

### *Analysis Performed:*

#### ***[Project 1.1: Descriptive Analysis](University_Canada_West/README.md)***
##### *Tools and Technologies*
  - All Design, *Draw.io*
  - Implementation, *Amazon Web Services*
   - For Data discovery, tools such as *Athena and AWS Glue Data Catalog*, can be used to explore in more detailed data
   - For Data Storage and Ingestion, *S3*
   - For Data Pipeline Implementation and Descriptive Analysis and Metrics Result, *AWS Glue*
   - For Data Analysis, *Athena*
   - For Data Visualization, *Excel* or *Amazon Quicksight*
   - For Data Publishing, *EC2*
   - For Data Monitoring, *CloudWatch*
#### ***[Project 1.2: Data Wrangling](University_Canada_West/DW)***
##### *Tools and Technologies*
- All Design, *Draw.io*
- Implementation, *Amazon Web Services*
  - For Data Cleaning, *Glue Databrew, Grid*
  - For Data Structuring, *Glue Databrew, Schema*

#### ***[Project 1.3: Data Protection](University_Canada_West/DP)***
##### *Tools and Technologies*
- All Design, *Draw.io*
- Implementation, *Amazon Web Services*
  - For User Management, *Identity Access Management (IAM)*
  - For encryption and decryption, *Key Management Service (KMS)*

#### ***[Project 1.4: Data Quality Control](University_Canada_West/DQC)***
##### *Tools and Technologies*
- All Design, *Draw.io*
- Implementation, *Amazon Web Services*
   - For Data Quality and Data Privacy, *AWS Glue Service and Trusted Zone Storage, S3*

### *Dataset:*
The dataset contains the records of the applications made for the PLAR process for the years 2024 and 2023. The fields contained in this dataset are detailed below:

- *Application ID:* Unique Identification for each PLAR Request
- *Student ID:* Unique Identification for each UCW Student
- *Full Name:* UCW Student Name
- *Application Request Date:* Date of the application
- *Program Applied For:* Program that the UCW Student is currently studying
- *Course Code:* Unique Identification for each Course
- *Course Title:* Official name of the academic course
- *Credits Requested:* Number of academic credits being requested
- *Credits Granted:* Number of academic credits that have been approved or awarded
- *Evaluation Status:* Current status of the course or credit request evaluation
- *Decision Date:* The date of the final decision was made

### *Deliverables*
- Drawiou Design
- Data Analytic Platform Implementation in Amazon Web Service
 

![image](https://github.com/user-attachments/assets/0c9b011f-320b-4127-b21c-bb335146ce1a)



## [Project 2: Data Analytic Platform for the City of Vancouver](The_City_of_Vancouver/README.md)

### *Background:*
The City of Vancouver has generated, collected and stored information from urban management that it has been carrying out during the last years to record its operational activities and obtain statistics. However, this data should be processed to obtain structured data by which the City of Vancouver can obtain valuable insight for improving the urban management and providing a high-quality service. 

### *Goal:*
Improve the efficiency and performance of the 3-1-1 Contact Centre for attending inquiries in The City of Vancouver by analyzing the rate of inquiries received through the Phone channel.

### *Dataset:*
The dataset contains the records of the inquiries that were received in the 311 contact center for the years 2024 and 2023. The fields contained in this dataset are detailed below:

- *Department:* Name of the department that attends the inquiry
- *Type:* Inquiry Type that has been attended
- *Year Month:* Year and month of the inquiry
- *Channel:* Type of channel through which the inquiry was received
- *Number of Records:* Number of inquiries that were received by a specific channel
- *BI_ID:* Unique Identification for each inquiry

### *Analysis Performed:*
- *Descriptive Analysis*
- *Data Wrangling*
- *Data Protection*
- *Data Quality Control*

### *Tools and Technologies*

#### Descriptive Analysis
- All Design, *Draw.io*
- Implementation, *Amazon Web Services*
  - For Data discovery, tools such as *Athena and AWS Glue Data Catalog*, can be used to explore in more detailed data
  - For Data Storage and Ingestion, *S3*
  - For Data Pipeline Implementation and Descriptive Analysis and Metrics Result, *AWS Glue*
  - For Data Analysis, *Athena*
  - For Data Visualization, *Excel* or *Amazon Quicksight*
  - For Data Publishing, *EC2*
  - For Data monitoring, *CloudWatch*
 
#### Data Wrangling    
- Implementation, *Amazon Web Services*
  - For Data Cleaning, *Glue Databrew, Grid*
  - For Data Structuring, *Glue Databrew, Schema*

#### Data Protection
- Implementation, *Amazon Web Services*
  - For User Management, *Identity Access Management (IAM)*
  - For encryption and decryption, *Key Management Service (KMS)*

#### Data Quality Control
- Implementation, *Amazon Web Services*
   - For Data Quality and Data Privacy, *AWS Glue Service and Trusted Zone Storage, S3*

### *Deliverables*
- Drawiou Design
- Data Analytic Platform Implementation in Amazon Web Service
- Written Report Phase 1
- Written Report Phase 2 


![image](https://github.com/user-attachments/assets/cfdc58bb-843e-4c9a-aafd-6bcef89830ba)




