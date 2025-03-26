📌 **1. Project Overview**

**Title: File Upload Notification System**

Objective

Build an automated system that monitors an S3 bucket for new file uploads, triggers a Lambda function to process the files, sends a notification via SNS, and stores metadata in an SQS queue for further processing.

Technologies Used: AWS S3, AWS Lambda, AWS SNS, AWS SQS, AWS CloudWatch


🔍 **2. Problem Statement**

Businesses often need to process large volumes of uploaded files efficiently. Manual monitoring is time-consuming and prone to errors. This project automates file monitoring and notification using AWS services, ensuring real-time alerts and scalable processing.

⚙️**3. Solution Architecture**

✅ Workflow Process:

A user uploads a file to the S3 bucket.

An S3 Event Trigger initiates a Lambda function.

The Lambda function processes the file (e.g., extracts metadata).

The processed data is pushed to an SQS queue for further use.

An SNS notification is sent to alert users about the upload.

![image alt](https://github.com/Nungari-Miriam/Notification-System/blob/32fb7a19804d2f952ff9395fefde39d365a460d9/Architecture%20Diagram.png)

🧑‍💻**4. Implementation Steps**

Step 1: Set Up an S3 Bucket

  Enable event notifications for the bucket to trigger Lambda.

Step 2: Create a Lambda Function

Step 3: Set Up SQS Queue

  Create a queue for further data processing.

Step 4: Configure SNS

  Set up an SNS topic and subscribe your email notifications.
  

📈5. **Outcomes and Impact**

Efficiency: Automated file tracking and real-time notifications.

Scalability: Asynchronous message processing via SQS supports higher loads.

