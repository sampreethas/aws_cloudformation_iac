# 🌩 AWS CloudFormation IaC with a simple template

This guide demonstrates how to use **AWS CloudFormation** for **Infrastructure as Code (IaC)** to provision and manage AWS resources using the **AWS CLI**.




##  Features  

-  **Declarative Infrastructure** – Define resources using YAML  
-  **Automated Deployment** – Use ```aws cloudformation deploy``` 
-  **Change Management** – Update stacks with version control  
-  **Rollback Support** – Automatic rollback on failure  



##  Prerequisites  

Before you begin, ensure you have:  

- **AWS CLI** → [Install Here](https://aws.amazon.com/cli/)  
- **AWS IAM Permissions** (To create and manage CloudFormation stacks)  
- **An S3 Bucket** (For storing CloudFormation templates if needed)  
- **YAML/JSON CloudFormation Template**  



##  Getting Started  
IAC can be provisioned using AWS Console or AWS CLI

### 1. Create a CloudFormation Template  
Save the **YAML** template as `template.yaml`.  

### 2. Run the following command to create the stack

```
aws cloudformation create-stack --stack-name MySimpleApp --template-body file://template.yaml --capabilities CAPABILITY_NAMED_IAM
```

### 3. Use the following to update the stack 
```
aws cloudformation update-stack --stack-name MySimpleApp --template-body file://template.yaml
```

### 4. Delete the stack using this command
**Note**: Do not forget to delete the resources after usage
```
aws cloudformation delete-stack --stack-name MySimpleApp
```

## Console output - Stack created based on the template

![image](https://github.com/user-attachments/assets/54563c12-4b1d-4815-892c-ce3742e409ef)
