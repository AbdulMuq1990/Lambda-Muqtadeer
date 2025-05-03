Lambda Function integrated with API Gateway & DynamoDB

Create a Lambda Role 
-----------------------------
Select Lambda and in permission allow
AWSLambdaBasicExecutionRole
AmazonDynamoDBFullAccess


Create a Lambda Function 
Name: My-lambda
Runtime: Python
Arch: x86_64
Use Existing Role: Select the role we created
Create Function 

After creation

Upload the Source code zip file 
Upload zip 


Create a DynamoDB table (only with below names)
--------------------------------------------------
Table name: muqtadeer
partion key: email 

Create Rest API in API Gateway 
-------------------------------
API name: my-api
Regional
IPv4
create API

Create 2 methods (GET and PUT)
-------------------------------
Method type: GET
select Lambda function
enable: Lambda proxy integration
Chose lambda ARN
Create 

Method type: PUT
select Lambda function
enable: Lambda proxy integration
Chose lambda ARN
Create  

Deploy the API 
Take the Invoke URL and hit in the Browser 
Enter details and submit 

IT will write the data in dynamodb you can verify by going to the Table
