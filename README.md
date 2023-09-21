# s3-event-triggering
S3 Event Triggering used by top companies like: Amazon, Netflix, Pinterest, slack etc

Goal:Let’s take Netflix, When someone uploads something, everyone gets updated for this new content. So, How is everyone getting updated ? 

Now, here comes the S3 event triggering. They use s3 bucket for storing data. So,whenever a new file is uploaded, s3 bucket triggers a lambda function. Why a lambda function ? Because Lambda functions are designed for short-lived, event-driven tasks. They can run for a maximum of 15 minutes per invocation (though most tasks are much shorter). You pay only for the compute time consumed during execution. Unlike EC2 instances which run continuously as long as they are powered on. You pay for the entire time an instance is running.

After Lambda, this info is sent to SNS (a simple notification service). After SNS is inovked, email notification is sent to all the users. 
