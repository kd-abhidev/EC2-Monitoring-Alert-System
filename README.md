EC2 Monitoring and Alert System



Project Overview

This project monitors an AWS EC2 instance using Amazon CloudWatch and sends email alerts when resource usage exceeds defined thresholds.



Architecture

EC2 → CloudWatch Metrics → CloudWatch Alarm → SNS → Email Notification



Services Used

* Amazon EC2
* Amazon CloudWatch
* Amazon SNS



What This Project Does



->Monitors EC2 CPU utilization

->Creates CloudWatch alarms based on threshold values

->Sends real time email alerts using SNS when threshold is exceeded



Setup Steps



1. Launch an EC2 instance
2. Open CloudWatch and select EC2 metrics
3. Create a CloudWatch alarm for CPU Utilization
4. Set threshold, for example CPU > 70%
5. Create an SNS topic
6. Subscribe your email to the topic
7. Confirm email subscription
8. Attach SNS topic to the CloudWatch alarm









Testing



Generate load on EC2

Alarm state changes to ALARM

Email notification received



Outcome

Implemented automated monitoring and alerting for EC2 to improve system visibility and response time.

