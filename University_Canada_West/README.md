# **Analysis**

Overview of the three analysis:

# **Descriptive Analysis**
Descriptive Analysis of PLAR Requests Dataset

### ***Descriptive Analysis Description***

The University Canada has a Registrar Office that manages many procedures such as the Prior Learning Assessment and Recognition Procedure, UCW-9022p. These requests may be approved or rejected. Nowadays, the Registrar's Office receives a significant number of PLAR requests; descriptive analysis will be used to analyse the rate of approved/success PLAR Requests.

### ***Goal***

Improve the performance of the Prior Learning Assessment and Recognition procedure of the registrar's office at UCW 

### ***Methodology***

**1. Descriptive Metric Definition**

   - “PLAR Success Rate” has been defined considering the following formula:
       #### *PLAR Success Rate = (Number of PLAR Success Application)/(Number of PLAR Requests Application)*

![image](https://github.com/user-attachments/assets/4bfc8e3e-06c5-407b-be02-ffbdfae64bcd)


**2. Design and Implementation**

#### **Data Storage Design**
  - For the data storage design, the S3 AWS service will be accessed through which a bucket will be created.
  - The bucket is a contain object that is flexible, durable, accessible from everywhere, and that has no capacity limit

   ##### **Data Storage Design in AWS**

![image](https://github.com/user-attachments/assets/97dfa8fa-187c-4658-8081-13e4d6c90fc6)

   ##### **Data Storage Design in Drawio**

   ![image](https://github.com/user-attachments/assets/18b6f37f-22f8-4c4f-b67a-46fb1ecdaa6a)

#### **Data Set Preparation - Operational Environment**

  - The dataset “PLAR Request" will be used, it has a total of 11 column names (headers) and 50 rows (data items).

   ##### **Dataset Preparation**

![image](https://github.com/user-attachments/assets/6b68aa9e-d202-41e6-80cd-aeba854003a5)

#### **Data Ingestion**

  - To perform data ingestion, uploading data is required. In this case, the files “311 inquiry volume” for 2023 and 2024 have been uploaded.

   ##### **Data Ingestion**

![image](https://github.com/user-attachments/assets/0c2d0618-0880-434f-8826-6fae3df19e35)

#### **Data Pipeline Design and Implementation**

  - For the descriptive metric Records per Phone Channel Rate Data pipeline design, a linear data diagram has been developed in Draw.io; where the datasets are represented by tables and the processes are represented by circles. For the design, the backward design has been used, in which the operational dataset is located at the bottom and the summarized data is located at the top.
  - To implement the ETL pipeline for the descriptive metric Records per Phone Channel Rate, the diagram design made in Drawio has been taken as a reference since it will show clearly in detail the available information, the information needed, and the actions that should be executed to obtain the metric we want to analyze

   ##### **Data Pipeline Design**

![image](https://github.com/user-attachments/assets/80f9d340-9ddf-4816-8ca5-2d02d246e847)


   ##### **Data Pipeline Implementation**

![image](https://github.com/user-attachments/assets/d6de167d-67f4-487c-8249-ea04a9ac2b52)


![image](https://github.com/user-attachments/assets/3465e3c9-cb1d-49f5-a370-d8bd6658bfdd)


**3. Descriptive Analysis and Metrics Result**

- Finally, as a result of the pipeline, the results for the initially defined metrics were obtained.

##### **Descriptive Analysis and Metrics Result**

![image](https://github.com/user-attachments/assets/7aa3a1ac-f6b7-4cac-8d16-900fa43bcf32)


**4. Data Analysis**

- The data analysis process involves three tasks: review, understand and explore data. Data exploration will be performed by using SQL. 

##### **Data Analysis**

![image](https://github.com/user-attachments/assets/571667ae-82b4-444f-96c9-f5a77d950517)

![image](https://github.com/user-attachments/assets/d51fc0d7-f0bf-48a4-9147-3a245de2d956)


**5. Data Visualization**

- With the content and structure ready, one way to present the results is to visualize the information and create a dashboard. The AWS service that allows visualizing the information is Amazon Quicksight, but for this case, the excel tool will be used to visualize the data.

##### **Data Visualization**

![image](https://github.com/user-attachments/assets/fc4e8580-a9bf-47b2-ba16-dcc9c419bae3)


**6. Data Publishing**

- For data publishing, two servers were configured, one to share and show information internally and another to show information to external users.

##### **Data Publishing via General Server**

Allows sharing resources with other users of the same company

![image](https://github.com/user-attachments/assets/93bcc230-e036-4a5d-9871-6056380abfe1)

##### **Data Publishing via Web Server**

Allows sharing results with users outside the company or a public audience

![image](https://github.com/user-attachments/assets/500a9a29-5d7d-4413-af85-755db8b7dbab)


**7. Data Monitoring**

- In the monitoring, the metrics of the dataset are observed, and after this observation, an analysis is performed. This analysis consists of comparing the metric with the defined threshold, and then based on the result of this analysis, if necessary, actions will be executed or not, this means controlling.
- It should be noted that some metrics can generate time series data, this can be verified when the observation is performed. If the time series is continuous, then there is a stream of data. The stream data needs analysis and immediate attention.
- Resources that have been monitored are S3, estimated charge and objects; the AWS Glue resource usage; and an alarm has been configured, and a threshold has been defined to monitor the estimated charge.

##### **Monitoring Resources**

![image](https://github.com/user-attachments/assets/dcfd3211-9255-4935-a7eb-935331048a37)

##### **Trancking Users**

![image](https://github.com/user-attachments/assets/8a19bea8-4fca-4c54-ba36-5edb1e8a519b)


### ***Insights and Findings***

- It can be observed that between the years 2024 and 2023 there is a small decrease in the Records per Phone Channel Rate, which means that the number of inquiries received by phone channel has decreased. However, despite this decrease and when compared to other channels such as chat, email, mail, and social media, the phone channel is still the channel that receives the most inquiries.


### ***Recommendations***

- Based on the findings mentioned in the previous point, it is recommended that The City of Vancouver prioritize improvements and resource allocation for the phone channel in order to reduce response times and improve customer service that allows it to continue offering quality service.


### ***Deliverables***
- Data Pipeline Implementation in Amazon Web Service
- Dashboard for Monitoring Resources and Visualization
- Metrics Results 



# **Data Wrangling**

Data Wrangling performed on 311 inquiry volume Dataset

### ***Data Wrangling Description***

For this purpose, the Glue Databrew AWS service will be used to prepare the dataset. 

### ***Goal***

Converting a low-quality dataset into a high-quality one and preparing it to be stored in a structured way in the analytical environment. 

### ***Methodology***

**1. Dataset Collection**
- “311 inquiry volume 2024.xls” and “311 inquiry volume 2023.xls” will be cleaned and structured.

##### **Dataset Collection**

![image](https://github.com/user-attachments/assets/f3ef81fa-7db4-4331-b859-df208dc3426d)

![image](https://github.com/user-attachments/assets/8bcceb26-8504-4617-ab26-f50687b1c353)

**2. Data Cleaning**
- For cleaning both datasets, “311 inquiry volume 2024.xls” and “311 inquiry volume 2023.xls” the headers were renamed with an appropriate name. Additionally, the year was extracted to create another column called InquiryYearMonth_YEAR which will only contain the year.

##### **Dataset Cleaning**

![image](https://github.com/user-attachments/assets/e2429714-3a60-4162-bfc4-8ff538957d22)

**2. Data Structuring**
- For structuring both datasets, the schema was updated.

##### **Dataset Structuring**

![image](https://github.com/user-attachments/assets/e28f1887-3703-4f0d-8110-56bd2909e8d6)

### ***Deliverables***
-  Dataset cleaned and structured generated and stored the in the Raw Zone, Inquiry Volume folder.

![image](https://github.com/user-attachments/assets/af5ad6b2-19f5-4294-876a-d942eb0595d9)

![image](https://github.com/user-attachments/assets/ae45ca1b-b053-4e41-a9f4-d18e285b366e)



# **Data Protection**

Data Protection performed for the DAP of The City of Vancouver

### ***Data Wrangling Description***

Implement data protection for the analytical environment in order to protect the dataset from invalid users. 

### ***Goal***
To avoid confidentiality, integrity, and availability problems, we should implement confidentiality, integrity, and availability protection. 

### ***Methodology***

**1. User Management**
- For this purpose, the Identity Access Management (IAM) AWS Service was used.

**2. Encryption and Decryption**
- For this purpose, the Key Management Service (KMS) AWS Service was used.

##### **User Management, Encryption and Decryption**

![image](https://github.com/user-attachments/assets/045f07bb-7cdf-4996-9ffb-b833da88f9fa)

![image](https://github.com/user-attachments/assets/8fa705d2-dede-4c4b-b9fe-81f3b60cb688)

![image](https://github.com/user-attachments/assets/ed10daf9-8f0e-414c-ae7f-da0bdc5343b9)

### ***Deliverables***
-  Confidentiality, integrity, and availability protection implemented.


# **Data Quality Control**

Data Quality performed for the DAP of The City of Vancouver

### ***Data Quality Control Description***

Ensure data quality and data privacy by using AWS Glue Service and Trusted Zone, working with the datasets stored in the raw zone.

### ***Goal***

Define and enforce rules, through which it is determined whether the dataset passes or fails the rules, if the dataset passes will be stored in the Trusted Zone.

### ***Methodology***

**1. Trusted Zone Design and Implementation**
-  Design and implementation of the Trusted Zone to stored the dataset tha pass the quality control.

##### **Trusted Zone Design and Implementation**

![image](https://github.com/user-attachments/assets/9c59c580-64b8-406a-8cc8-cb10868677db)


**2. Pipeline Implementation**
- Visual ETL will be created to configure the rules
- Privacy is prioritized, for which the Detect Sensitive Data function will be used in the transform section.
- The Evaluate data quality function will be used to assess the quality of the dataset, and for this purpose, the “inquirychannel” field has been chosen, and a threshold greater than 0.95 was established.
- The Conditional Router function, two groups “pass” and “fail” are created. With the change schema, the extra columns are eliminated to have the original dataset

##### **Pipeline Implementation**

![image](https://github.com/user-attachments/assets/08a6a578-c3db-443a-9f24-dbe7796306ec)

![image](https://github.com/user-attachments/assets/5a5be29b-fae5-4a4f-9b47-748b922035cc)


### ***Deliverables***
-  Dataset with quality control implemented by ensuaring 0.95 in the "inquirychannel" field.
