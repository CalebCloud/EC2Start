# EC2Start
Lambda function to start AWS EC2 Server

Instructions:
- Replace line 2 and lne 3 with your region and EC2 instance id. 
- Create an IAM role and give it AmazonEC2FullAccess (or create one like [this](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_ec2_tag-owner.html)) and assign the role to the lambda function. 
- In API Gateway create an HTTP API add the lambda function as an integration when making the API. 
- Go to your lambda functions and click on the function that you created. Click on the function name and click add trigger. Select API Gateway and then select the api that you created. Leave the next options as default and open. 
- Click on API Gaeway under the Lambda triggers, underneath find the gateway you just created and click on details. Under details, copy the API endpoint. 
- Whenever you want to turn on the server, activate that endpoint. You can do this by attaching it to a button with simple html on a webpage or just loading the URL. 

Taking it Further
- This can be taken further by integrating cognito autorization so that only logged in or authorized users from the user pool will be able to invoke the API and turn on the server.
