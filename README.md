# Custom-Automated-AMI
Creating AWS custom AMI in automated way using the SSM parameter store 

* SSM Parameter Store:
    Parameter Name: /GoldenAMI/Linux/RedHat-7/latest
    Parameter Value: Any linux based AMI of your choice
* Optional: An S3 bucket with the file Post-Update-Scripts
    Make sure this bucket is publicly accessible or having VPC Endpoint
    RoleName: lambda-ssm-role:
* Permissions: Managed Policies AWSLambdaExecute and AmazonSSMFullAccess
    RoleName: ManagedInstanceRole:
    An EC2 Role to allow SSM to start instances, create images etc,
* Permissions: Managed Policies AmazonEC2RoleforSSM
    RoleName: AutomationServiceRole:
* An EC2 Role to Allow SSM to run documents and allow it to assume ManagedInstanceRole we just created.
    Permissions: Managed Policies AmazonSSMAutomationRole