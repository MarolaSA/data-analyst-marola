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

**1. Define the descriptive metric**

   - “Records per Phone Channel Rate” has been defined considering the following formula:
       #### *Records per Phone Channel Rate=(Number of Phone Inquiries)/(Number of Received Inquiries)*

![image](https://github.com/user-attachments/assets/e7df1637-7ea4-4987-85bd-8542dc7b3d2e)


**2. Data Storage Design**
  - For the data storage design, the S3 AWS service will be accessed through which a bucket will be created.
  - The bucket is a contain object that is flexible, durable, accessible from everywhere, and that has no capacity limit

   #### **Data Storage Design in AWS**

![image](https://github.com/user-attachments/assets/97dfa8fa-187c-4658-8081-13e4d6c90fc6)

   #### **Data Storage Design in Drawio**

   ![image](https://github.com/user-attachments/assets/18b6f37f-22f8-4c4f-b67a-46fb1ecdaa6a)

**3. Data Set Preparation - Operational Environment**

  - The dataset “311 inquiry volume 2024.xls” and “311 inquiry volume 2023.xls” obtained from The City of Vancouver will be used, each dataset has a total of 6 column names (headers) and 2277 rows (data items); however, for this analysis 500 rows (data items) was processed. 

#### **Dataset Preparation**

![image](https://github.com/user-attachments/assets/e458e994-b207-4209-acde-80cafc35c935)

**4. Data Ingestion**

  - To perform data ingestion, uploading data is required. In this case, the files “311 inquiry volume” for 2023 and 2024 have been uploaded.

#### **Data Ingestion**

![image](https://github.com/user-attachments/assets/0c2d0618-0880-434f-8826-6fae3df19e35)

**5. Data Pipeline Design and Implementation**

  - For the descriptive metric Records per Phone Channel Rate Data pipeline design, a linear data diagram has been developed in Draw.io; where the datasets are represented by tables and the processes are represented by circles. For the design, the backward design has been used, in which the operational dataset is located at the bottom and the summarized data is located at the top.
  - To implement the ETL pipeline for the descriptive metric Records per Phone Channel Rate, the diagram design made in Drawio has been taken as a reference since it will show clearly in detail the available information, the information needed, and the actions that should be executed to obtain the metric we want to analyze

#### **Data Pipeline Design**

![image](https://github.com/user-attachments/assets/d9df6838-ac71-41f1-96bf-64ec1cc92744)


#### **Data Pipeline Implementation**

![image](https://github.com/user-attachments/assets/d6de167d-67f4-487c-8249-ea04a9ac2b52)


![image](https://github.com/user-attachments/assets/3465e3c9-cb1d-49f5-a370-d8bd6658bfdd)


Finally, as a result of the pipeline, the results for the initially defined metrics were obtained.

#### **Metrics Result**

![image](https://github.com/user-attachments/assets/7aa3a1ac-f6b7-4cac-8d16-900fa43bcf32)


## Data Wrangling
## Data quality control

