# WildRydesDemo
(Link to the Application) https://master.deiph8ir0guor.amplifyapp.com/

https://github.com/touristdave69/WildRydesDemo/assets/145601015/e553ef57-a9c1-47ed-a9fe-a58f2dda5669

# Technologies used
CodeCommit, Amplify, Cognito, Lambda, IAM, API Gateway and DynamoDB AND ArcGIS for map funtionality 

# ( Project code and files are in a Public S3 Bucket)
Steps to Retrieve Project Code
1)  create an empty repositiry in code commit
2)  add a policy to your IAM user to acces commit code
3)  create git credentials for IAM user to allow HTTPS connections to code commit
4)  clone the repository (create an empty folder for code)
5)  copy the project from S3 bucket and commit into new repo

# 
1) set up amazon cognito for user authentication
   - create a new user pool in amazon cognito
   - Update the app configuration file to use to use the congnito user pool
   - test the congnito integration by doing user registration and logins
  
2) implement ride sharing functionality with Lambda and DynamoDB
   - Create a new DynamoDB table
   - create an IAM to be used for a lambda function execution role, allowing putitem on DynamoDB table
   - Deploy Lambda code and execute a test event
   - test that items are saved into the DynamoDB table

3) Set up API Gateway to invoke the rideshare Functionality
   - Create a Rest API in API Gateway to invoke a lambda function
   - create an authorizer so API Gateway can work with cognito
   - create a resource and post method in API Gateway for lambda integration
   - Deply the API from Api Gateway
 - update the config file for the new invoke URL from API Gateway in CODE COMMIT
 - update the ARCgis Version number in the ride.html file (4.3 -> 4.6) (lines 16 and 95)
