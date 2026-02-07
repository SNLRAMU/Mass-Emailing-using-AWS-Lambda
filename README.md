# Mass-Emailing-using-AWS-Lambda
This project demonstrates how to implement a serverless mass emailing system using AWS Lambda and Amazon Simple Email Service (SES). The solution is fully serverless, scalable, and cost-effective, making it suitable for sending bulk notifications, alerts, or informational emails
🧰 AWS Services Used
AWS Lambda – Executes serverless code to send emails
Amazon SES (Simple Email Service) – Sends bulk emails
Amazon CloudWatch (EventBridge) – Schedules and triggers Lambda
AWS IAM – Provides execution permissions via pre-created lab roles
Step 1: Creating IAM Role
In the AWS console search for IAM in the search bar and select the service
In that select roles and click on Create role
Select use cases as Lambda and click on next
In permission, policies choose CloudWatch full access and SES full access and then click on next
Give a suitable name for the role and click on Create role
The role will be created.
<img width="1472" height="704" alt="Gemini_Generated_Image_8epzog8epzog8epz" src="https://github.com/user-attachments/assets/348d4b37-7646-4c0b-bd79-25e53b5f8062" />
Step 2: Creating Lambda Function
In the AWS console search for Lambda in the search bar and select the service.
Provide the name of the function.
In the position of runtime, we must choose the language that we want. Here, I am choosing the most recent NodeJS 16.x version.
Choose whether to create a new or existing role as the executing role in the following step. I’m choosing the role that I already created in the previous phase.
Rest everything. We can keep it optional
Select Create a Function.
In the AWS console search for CloudWatch in the search bar and select the service.
In the left navigation pane, select Event in that select rules and then click on create rule.
Next, choose the schedule and click on the Cron expression to set it to a specific time.
Select add target and choose the lambda function I’m choosing the function that I already created in the previous phase.
Click on configure details.
Next, give a name to the rule and rest everything we can keep optional
Click on Create the rule.
Result:

Lambda is triggered and sent an email to the users at the scheduled time
<img width="925" height="379" alt="image" src="https://github.com/user-attachments/assets/9a097275-0aeb-4694-9394-ac999fe26fe4" />
