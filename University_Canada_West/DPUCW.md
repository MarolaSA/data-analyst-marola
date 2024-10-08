# <font color="green">Data Protection</font> 

Data Protection performed for the DAP of The University Canada West

### ***Data Protection Description***

Implement data protection for the analytical environment in order to protect the dataset from invalid users. 

### ***Goal***
To avoid confidentiality, integrity, and availability problems, we should implement confidentiality, integrity, and availability protection. 

### ***Methodology***

**1. User Management**
- For this purpose, the Identity Access Management (IAM) AWS Service was used.
- Following are the roles, the policies (permissions) that are currently available

##### **Identity Access Management, User Management**

![image](https://github.com/user-attachments/assets/df269410-3513-4c2d-abab-3b5a66f79055)

**2. Encryption and Decryption**
- For this purpose, the Key Management Service (KMS) AWS Service was used.
- A key will be created for symmetric (uses the same key for encryption and decryption). Asymmetric have different keys for encryption and decryption. For this case, the key “registraroffice-plar-key-marola” has been created and the role LabRole has been assigned to it.

##### **Key Management Service, drawio**

![image](https://github.com/user-attachments/assets/7052277a-08c5-408a-bcf9-de2b1a75a206)


##### **Key Creation**

![image](https://github.com/user-attachments/assets/8fa705d2-dede-4c4b-b9fe-81f3b60cb688)

##### **Encryption for registraroffice-plar-marola Bucket**

The bucket will be encrypted, which means that landing, raw, curated, trusted zone, and any dataset stored in the bucket will be encrypted. In addition, any dataset downloaded from the bucket will need the key to be decrypted.

![image](https://github.com/user-attachments/assets/e409c649-4906-49f0-88ef-ea52c07bd033)


### ***Deliverables***
-  Confidentiality, integrity, and availability protection implemented.
-  Bucket encrypted

