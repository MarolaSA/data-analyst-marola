
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

  

