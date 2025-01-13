# AWS-SAM-template-serverless-data-pipeline
AWS SAM Template for serverless data pipeline with kinesis data stream,Lamda function and S3 bucket
xplanation:
Kinesis Data Stream:

The MyKinesisStream resource creates a Kinesis Data Stream with 1 shard.
S3 Bucket:

The MyS3Bucket resource creates an S3 bucket, with a name based on the stack name.
Lambda Function:

The MyLambdaFunction resource defines a Lambda function that is triggered by the Kinesis Data Stream.
The Lambda function's code is located in the ./src directory.
An environment variable BUCKET_NAME is set to the name of the S3 bucket.
The Events section sets up the Kinesis Data Stream as an event source for the Lambda function, starting from the earliest record (TRIM_HORIZON).
Outputs:

This section provides the outputs of the stack, which include the names of the S3 bucket, the Lambda function, and the Kinesis Data Stream.
Notes:
Make sure the ./src directory contains the index.js file with the handler function.
The nodejs14.x runtime is used in this example. You can change it to another runtime if required.
The BucketName in the MyS3Bucket resource should be unique across all of AWS. You may want to adjust the naming convention to ensure uniqueness.
This template sets up a basic serverless data pipeline. You can extend it with more resources and configurations as needed.

