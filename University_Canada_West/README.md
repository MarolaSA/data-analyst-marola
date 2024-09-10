
# <font color="green">Descriptive Analysis</font> 

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

![image](https://github.com/user-attachments/assets/1aa57e15-db6f-43da-a00c-6c2eb285a2e7)


 ##### **Data Storage Design in Drawio**

  ![image](https://github.com/user-attachments/assets/8357cf0c-eb31-4e97-ba52-d81a0872946b)


#### **Data Set Preparation and Data Ingestion - Operational Environment**

  - The dataset “PLAR Request" will be used, it has a total of 11 column names (headers) and 50 rows (data items).
  - To perform data ingestion, uploading data is required. In this case, the file “PLAR Requests” have been uploaded.

##### **Dataset Preparation and Data Ingestion**

![image](https://github.com/user-attachments/assets/f2751f7b-7ab1-48c3-bd63-3a96bd456fbe)


![image](https://github.com/user-attachments/assets/9a974b95-3c37-437b-9dd7-a36cceaa9eca)


#### **Data Pipeline Design and Implementation**

  - For the descriptive metric PLAR Success Rate Data pipeline design, a linear data diagram has been developed in Draw.io; where the datasets are represented by tables and the processes are represented by circles. For the design, the backward design has been used, in which the operational dataset is located at the bottom and the summarized data is located at the top.
  - To implement the ETL pipeline for the descriptive metric PLAR Success Rate, the diagram design made in Drawio has been taken as a reference since it will show clearly in detail the available information, the information needed, and the actions that should be executed to obtain the metric we want to analyze

##### **Data Pipeline Design**

![image](https://github.com/user-attachments/assets/27500bc2-d296-4b79-a675-4dcc50c16e1a)
![image](https://github.com/user-attachments/assets/7ed5a872-6283-403b-8eee-8ce7853d9a9b)
![image](https://github.com/user-attachments/assets/63a45c5f-0ccb-4a51-b4a0-793d5ab1f251)



##### **Data Pipeline Implementation**

![image](https://github.com/user-attachments/assets/3d44c10e-0721-46de-aa1e-83fbd3a98650)


**3. Descriptive Analysis and Metrics Result**

- Finally, as a result of the pipeline, the results for the initially defined metrics were obtained.

##### **Descriptive Analysis and Metrics Result**

![image](https://github.com/user-attachments/assets/150fee10-fb09-4b1d-acd1-fc0751fad765)


**4. Data Analysis**

- The data analysis process involves three tasks: review, understand and explore data. Data exploration will be performed by using SQL. 

##### **Data Analysis**

![image](https://github.com/user-attachments/assets/78f3ca28-20b5-441f-8719-3e336b8d8e16)

![image](https://github.com/user-attachments/assets/1e070eb5-5d8b-4d71-898a-62f6048bcb14)



**5. Data Visualization**

- With the content and structure ready, one way to present the results is to visualize the information and create a dashboard. The AWS service that allows visualizing the information is Amazon Quicksight, but for this case, the excel tool will be used to visualize the data.

##### **Data Visualization**

![image](https://github.com/user-attachments/assets/da7bbe46-af4c-4e2c-886c-84afe4cbfb09)


**6. Data Publishing**

- For data publishing, two servers were configured, one to share and show information internally and another to show information to external users.

##### **Data Publishing via General Server**

Allows sharing resources with other users of the same company

![image](https://github.com/user-attachments/assets/75f9c681-089b-44b1-a908-25c095df87bd)


##### **Data Publishing via Web Server**

Allows sharing results with users outside the company or a public audience

![image](https://github.com/user-attachments/assets/dc8068ea-e1e3-4618-a310-f6187e872e20)



**7. Data Monitoring**

- In the monitoring, the metrics of the dataset are observed, and after this observation, an analysis is performed. This analysis consists of comparing the metric with the defined threshold, and then based on the result of this analysis, if necessary, actions will be executed or not, this means controlling.
- It should be noted that some metrics can generate time series data, this can be verified when the observation is performed. If the time series is continuous, then there is a stream of data. The stream data needs analysis and immediate attention.
- Resources that have been monitored are S3, estimated charge and objects; the AWS Glue resource usage; and an alarm has been configured, and a threshold has been defined to monitor the estimated charge.

##### **Monitoring Resources**

![image](https://github.com/user-attachments/assets/7089c458-81b5-433c-8fb8-81fc02ff27c7)


##### **Trancking Users**

![image](https://github.com/user-attachments/assets/b56c329e-6480-4838-8044-791ff9b49a9f)



### ***Insights and Findings***

- It can be observed that between the years 2024 and 2023 there is a small decrease in the PLAR Success Rate, which means that the number of PLAR Requests Application Successful has decreased a little.


### ***Recommendations***

- Based on the findings mentioned in the previous point, it is recommended that The UCW conduct a diagnostic analysis to identify the causes that are generating this decrease, for example, incomplete supporting documentation, incomplete portfolios, or failed interview.

### ***Deliverables***
- Data Pipeline Implementation in Amazon Web Service
- Dashboard for Monitoring Resources and Visualization
- Metrics Results 
