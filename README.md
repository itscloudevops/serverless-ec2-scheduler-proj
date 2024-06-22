# Serverless EC2 Instance Scheduler for Company Working Hours 
## Scenario :
In some companies, there is no need to run their EC2 instances 24/7; they require instances to operate during specific time periods, such as company working hours, from 8:00 AM in the morning to 5:00 PM in the evening. To address this scenario, I will implement two Lambda functions responsible for starting and stopping instances. These Lambda functions will be triggered by two CloudWatch Events in the morning and evening. This solution is fully serverless.

![266763781-287063a4-964a-4f8b-b88e-25535b7f4691](https://github.com/itscloudevops/serverless-ec2-scheduler-proj/assets/172890207/1a5fc611-4010-4d79-84e2-417135e27fd0)


## STEPS :

We have now created a schedule for starting the instance every day at 8:00 AM

Next, we need to create a schedule for stopping instances

To create the schedule for stopping instances, follow the same steps as for starting instance scheduling with a few changes, Keep your rule name as "stop-ec2-rule"

The changes include modifying the scheduled time and selecting the appropriate scheduling function

We need to change the schedule time to 17:00 because it will stop the Lambda function at 17:00 IST (5:00 PM).

We have to Change the Function as Stop-EC2-demo

Now, we have successfully created two schedules: one to start the instance every day at 8:00 AM and the other to stop the instance every day at 5:00 PM.

