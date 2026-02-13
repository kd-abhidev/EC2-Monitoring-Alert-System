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



Launch an EC2 instance

Open CloudWatch and select EC2 metrics

Create a CloudWatch alarm for CPU Utilization

Set threshold, for example CPU > 70%

Create an SNS topic

Subscribe your email to the topic

Confirm email subscription

Attach SNS topic to the CloudWatch alarm



Testing



Generate load on EC2

Alarm state changes to ALARM

Email notification received



Outcome

Implemented automated monitoring and alerting for EC2 to improve system visibility and response time.

