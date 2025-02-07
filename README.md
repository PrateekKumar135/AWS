# AWS
**Accessing Excel Data from Amazon S3 Using AWS Lambda and Converting It to JSON**


**We will create an AWS Lambda function that**:

1. Reads an Excel file from an S3 bucket.
2. Extracts the data from the Excel file.
3. Converts the extracted data into JSON format.
4. Returns the JSON output.
# Step 1: Prerequisites
*Before proceeding, ensure you have the following*: 

✅ AWS Account – To use AWS services.

✅ Amazon S3 Bucket – To store the Excel file.

✅ IAM Role for AWS Lambda – With S3 read permissions.

✅ AWS Lambda Function – To process the data.

✅ Python Libraries – boto3, pandas, and openpyxl for data extraction.
# Step 2: Upload Excel File to Amazon S3
1. Go to AWS S3 Console: Navigate to S3 Service.

2. Create a Bucket: Click "Create Bucket" → Set a unique name → Choose a region → Click "Create".

3. Upload Your Excel File: Inside the bucket, click "Upload" and select your .xlsx file. Assume the file is named "data.xlsx".
# Step 3: Create an IAM Role for AWS Lambda
1. Go to AWS IAM Console → "Roles".

2. Click "Create Role" → Choose AWS Lambda as the trusted entity.

3. Attach Policies: AmazonS3ReadOnlyAccess (to read data from S3). AWSLambdaBasicExecutionRole (for Lambda execution logs).

4. Give a Role Name (e.g., LambdaS3ReadRole) → Click "Create Role".

# Step 4: Create AWS Lambda Function
1. Go to AWS Lambda Console → Click "Create Function".

2. Choose "Author from Scratch"

3. Set Function Name (e.g., ProcessExcelFromS3).

4. Choose Runtime: Python 3.9 or above.

5. Choose Execution Role → Select "Use an existing role" → Choose LambdaS3ReadRole.

6. Click "Create Function".
# Step 5: Install Dependencies (boto3, pandas, openpyxl)
*Since AWS Lambda has a limited environment, we need to upload the required libraries in a deployment package.*
*Upload Layer to AWS Lambda:*
1. Go to AWS Lambda → "Layers" → "Create Layer".

2. Upload pandas_layer.zip.

3. Attach the layer to your Lambda function.
# Step 6: Write the AWS Lambda Function Code (Lambda Code: Read Excel from S3 & Convert to JSON)

