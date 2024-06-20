Problem Statement
Create a serverless image processing application that automatically resizes and optimizes images uploaded to an Amazon S3 bucket.
Creating buckets
1.	Login to AWS console.
2.	Make sure you are in US East (N. Virginia)
3.	Navigate to S3 service using search bar.
4.	Navigate to bucket section. Create source and destination buckets.
5.	Add an image to source bucket.

 
Creating IAM policy
1.	Go to IAM and select Polices.
2.	Create a new policy.
3.	Go to JSON tab and update policy to- 
4.	Make sure to update ARN of your bucket in this policy.
5.	Give policy name-image-resize-policy.
6.	Create policy.
                                                                                                      








Creating Lambda function
1.	Navigation to lambda.
2.	Create a function. Set function name Lambfunction.
3.	Set runtime to Node.js 18.x
4.	Change default execution role to select existing one.
5.	Select image-resize-policy.
6.	Create function.
7.	Navigate to test section and update Event JSON- 
8.	Make sure to enter your source bucket and enter your image name in key.
9.	 Go to configuration tab and select environmental variable.
10.	Add a environmental variable. Set Key to DEST_BUCKET and enter you destination bucket name in value section.
11.	Test the event.
12.	 
13.	Add a trigger, go to trigger select S3.
14.	 
15.	In bucket select source bucket.
16.	Leave rest as default. And add .
17.	You can see an resize image in destination bucket.
Result-
Source Bucket- 
Destination Bucket-
 

