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
