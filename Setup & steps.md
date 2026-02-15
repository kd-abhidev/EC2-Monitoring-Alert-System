EC2 Monitoring and Alert System Setup Guide



Prerequisites



1. AWS account
2. Basic knowledge of AWS Console
3. Verified email address for notifications
4. Step 1. Launch EC2 Instance
5. Login to AWS Management Console
6. Open EC2 service
7. Click Launch Instance
8. Choose Amazon Linux 2
9. Select t2.micro or t3.micro
10. Allow SSH in Security Group
11. Launch the instance



Step 2. Verify EC2 Metrics in CloudWatch



1. Go to CloudWatch service
2. Click Metrics
3. Select EC2
4. Select Per Instance Metrics
5. Confirm CPUUtilization metric is available



Step 3. Create SNS Topic



1. Open SNS service
2. Click Topics
3. Click Create topic
4. Choose Standard
5. Name the topic, example ec2-alert-topic
6. Click Create



Step 4. Subscribe Email to SNS



1. Open the created topic
2. Click Create subscription
3. Protocol: Email
4. Enter your email address
5. Click Create subscription
6. Open your email and confirm the subscription



Step 5. Create CloudWatch Alarm



1. Go to CloudWatch
2. Click Alarms
3. Click Create Alarm
4. Select Metric
5. Choose EC2 → Per Instance Metrics
6. Select CPUUtilization for your instance
7. Click Select metric



Step 6. Configure Alarm Condition



1. Statistic: Average
2. Period: 5 minutes
3. Threshold type: Static
4. Condition: CPUUtilization greater than 70 percent
5. Click Next



Step 7. Configure Notification



1. Select existing SNS topic
2. Choose ec2-alert-topic
3. Click Next



Step 8. Name and Create Alarm



1. Alarm name: High-CPU-EC2
2. Click Create Alarm



Step 9. Test the Alarm



1. Connect to EC2 using SSH
2. Run this command to create load 
3. Wait a few minutes
4. Alarm state changes to ALARM
5. Email notification is received



Step 10. Stop Test Load



Run this command -> killall 



Result

CloudWatch monitors EC2 CPU usage and sends email alerts through SNS when the threshold is exceeded.

