# Custom-Automated-AMI
Creating AWS custom AMI in automated way using the SSM parameter store 

- SSM parameter Store : 
    Parameter Name: /TestAmi/ID/BaseAMi/Latest
    parameter value: 
- S3 Bucket with the file post-scripts
    Make sure bucket is accessible through VPC Endpoints.
- RoleName: lambda-ssm-role
    Permissions: AWSLambdaExecute & AmazonSSMFullAccess. 