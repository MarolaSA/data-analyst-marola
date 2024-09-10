
# <font color="green">Data Quality Control</font> 

Data Quality performed for the DAP of The University Canada West

### ***Data Quality Control Description***

Ensure data quality and data privacy by using AWS Glue Service and Trusted Zone, working with the datasets stored in the raw zone.

### ***Goal***

Define and enforce rules, through which it is determined whether the dataset passes or fails the rules, if the dataset passes will be stored in the Trusted Zone.

### ***Methodology***

**1. Trusted Zone Design and Implementation**
-  Design and implementation of the Trusted Zone to stored the dataset tha pass the quality control.

##### **Trusted Zone Design and Implementation**

![image](https://github.com/user-attachments/assets/8d36cf77-bfc5-4b88-938b-2d72d64ceec6)

![image](https://github.com/user-attachments/assets/b55b570c-7067-4dbc-a53f-dccc6d181c2d)


**2. Pipeline Implementation**
- Visual ETL will be created to configure the rules
- Privacy is prioritized, for which the Detect Sensitive Data function will be used in the transform section.
- The Evaluate data quality function will be used to assess the quality of the dataset, and for this purpose, the “inquirychannel” field has been chosen, and a threshold greater than 0.95 was established.
- The Conditional Router function, two groups “pass” and “fail” are created. With the change schema, the extra columns are eliminated to have the original dataset

##### **Pipeline Implementation**

![image](https://github.com/user-attachments/assets/85cc000e-e457-4ea6-b4d8-2acbb78c68a7)

![image](https://github.com/user-attachments/assets/ad8f7173-0902-4f11-8af5-ad714debc89e)




### ***Deliverables***
-  Dataset with quality control implemented by ensuaring 0.95 in the "Application" field.
