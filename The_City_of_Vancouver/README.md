# <font color="red">Analysis</font>

Overview of the three analysis:

## Descriptive Analysis
Descriptive Analysis of 311 inquiry volume Dataset

### Analysis Description

The City of Vancouver has a 3-1-1 Contact Center that handles inquiries from the community through various channels such as chat, phone, email, and social media. These inquiries are categorized into different types and are managed by other departments depending on their category.
Currently, the 3-1-1 Contact Center receives a considerable number of inquiries, the descriptive analysis will be used to analyze the performance of the Phone channel and thus answer the question “What happens in my company?”

### Goal

Improve the efficiency and performance of the 3-1-1 Contact Centre for attending inquiries in The City of Vancouver by analyzing the rate of inquiries received through the Phone channel so it will be possible to determine if the number of operators handling the telephone inquiries is sufficient or whether it is necessary to reassign staff or make new hires. For this purpose, a Data Pipeline will be created.

### Methodology

**1. Descriptive Metric Definition**

   - “Records per Phone Channel Rate” has been defined considering the following formula:
       #### *Records per Phone Channel Rate=(Number of Phone Inquiries)/(Number of Received Inquiries)*

![image](https://github.com/user-attachments/assets/e7df1637-7ea4-4987-85bd-8542dc7b3d2e)


**2. Design and Implementation**

#### **Data Storage Design**
  - For the data storage design, the S3 AWS service will be accessed through which a bucket will be created.
  - The bucket is a contain object that is flexible, durable, accessible from everywhere, and that has no capacity limit

   ##### **Data Storage Design in AWS**

![image](https://github.com/user-attachments/assets/97dfa8fa-187c-4658-8081-13e4d6c90fc6)

   ##### **Data Storage Design in Drawio**

   ![image](https://github.com/user-attachments/assets/18b6f37f-22f8-4c4f-b67a-46fb1ecdaa6a)

#### **Data Set Preparation - Operational Environment**

  - The dataset “311 inquiry volume 2024.xls” and “311 inquiry volume 2023.xls” obtained from The City of Vancouver will be used, each dataset has a total of 6 column names (headers) and 2277 rows (data items); however, for this analysis 500 rows (data items) was processed. 

   ##### **Dataset Preparation**

![image](https://github.com/user-attachments/assets/e458e994-b207-4209-acde-80cafc35c935)

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


**8. Insights and Findings**

- Finally, as a result of the pipeline, the results for the initially defined metrics were obtained.


**9. Recommendations**



## Data Wrangling





## Data quality control

