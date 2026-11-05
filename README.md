# Cloud-Based-Student-Attendance-Management-System
This is a secure, serverless application that enables educational institutions to manage students, courses, lecturers, and attendance records.

This project uses AWS services in its implementation. The AWS services and their respective roles are listed below: 
* Amazon S3 - Frontend hosting and report storage
* Amazon CloudFront	- Secure website delivery
* Amazon Cognito	- User authentication
* Amazon API Gateway	- REST API endpoints
* AWS Lambda	- Python backend processing
* Amazon DynamoDB -	Student, course, and attendance database
* Amazon CloudWatch -	Logs and monitoring
* AWS IAM -	Permissions and security

<h3>Main application users</h3>
User        &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;    Responsibilities <br> 
Administrator  -	Register students, lecturers, and courses <br>
Lecturer	     - Record and manage attendance <br>
Student	       - View attendance history and percentages
  
<h3>Application workflow</h3> 
 1. The user accesses the website through cloudfront <br>
 2. The frontend files are delivered from the Amazon S3 bucket <br>
 3. Amazon Cognito authenticates the user<br>
 4. The frontend sends request to API Gateway with an authentication token<br>
 5. API Gateway Invokes the relevant lambda function<br>
 6. Lambda validates the request and accesses the DynamoDB<br>
 7. DynamoDB stores or retrieve the attendance information<br>
 8. Cloudwatch captures application logs and errors<br>




  
