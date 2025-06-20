# Serverless-Image-Watermarking-System-using-AWS-Lambda-S3

Built a fully automated, serverless image processing pipeline that applies watermarks to user-uploaded images using AWS Lambda, S3, and Python.

Features
Users upload images via a responsive HTML/JavaScript frontend integrated with the AWS SDK.

Uploads trigger an AWS Lambda function using S3 PutObject event notifications.

The Lambda function retrieves the uploaded image, applies a custom watermark using the Pillow library, and saves the result in a separate S3 bucket.

Both original and processed images are displayed in the frontend after processing.

Configured S3 lifecycle rules to automatically delete all images every 24 hours.

Full error handling with structured CloudWatch logging for monitoring and debugging.

Technologies Used
AWS Lambda (Python 3.9)

Amazon S3 (Event-based triggers, Lifecycle Rules)

AWS IAM (Custom execution role with scoped permissions)

Python (Pillow library for image editing)

HTML, CSS, JavaScript (Client-side UI)

Architecture Highlights
Trigger-based Lambda execution upon image upload to S3.

Stateless, fully serverless design with no backend server dependencies.

Secure IAM role enforcing least-privilege access to required AWS services.

Dynamic frontend preview of both original and watermarked images.

Automated cleanup of stored files via S3 lifecycle policy.
