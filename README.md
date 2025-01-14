# Hotel Food Order Webpage

This project is a responsive webpage for ordering food at a hotel. It includes a fixed navbar, collapsible left menu, main content area, right panel, and footer. The page adjusts its layout and scaling based on screen width.

## Features
1. **Fixed Navbar**: The navbar remains at the top when scrolling.
2. **Responsive Layout**:
   - Left menu
   - Main content
   - Right panel
   - Footer
3. **Collapsible Left Menu**: Click the "Toggle Menu" button to show/hide the menu.
4. **Dynamic Scaling**:
   - Shrinks the page width dynamically based on screen size.


## Instructions
1. Clone or download the repository.
2. Open `index.html` in any modern browser.
3. Resize the browser window to see responsive behavior and dynamic scaling.
4. Use the "Toggle Menu" button to collapse or expand the left menu.


### CREATE AWS LAMBDA FOR ADDING TWO NUMBERS
1.Set Up AWS CLI or Console:

Log in to your AWS account and go to the Lambda service.
Click "Create Function" and select "Author from scratch".
Name the function, select Python as the runtime, and create the function.
Deploy the Code:

Copy and paste the code into the Lambda function editor under the "Code" tab.
Click "Deploy" to save the changes.
Test the Function:

2.Create a test event with the following structure:
json output:
{
  "num1": 10,
  "num2": 20
}



3.Run the test, and you should receive the result:
json
Copy code
{
  "statusCode": 200,
  "body": "{\"message\": \"Addition successful\", \"result\": 30}"
}


4.Trigger the Lambda Function:

Use the AWS Management Console, API Gateway, or CLI to invoke the function with the required inputs.
Notes
The function expects num1 and num2 to be part of the event payload.
Add proper IAM roles if this Lambda function needs to interact with other AWS services.


### LAMBDA FUNCTION TO STORE A DOCUMENT OR PDF IN S3 BUCKET

1.Steps to Set Up
Create the S3 Bucket:

Go to the AWS S3 console.
Create a new bucket (e.g., my-pdf-storage).
Note the bucket name for use in the Lambda function's environment variables.
Set Up the Lambda Function:

2.In the AWS Lambda console, create a new function.
Use Python 3.x as the runtime.
Copy and paste the code into the editor.
Set Environment Variables:

3.Under the "Configuration" tab, add an environment variable:
Key: S3_BUCKET_NAME
Value: The name of your S3 bucket (e.g., my-pdf-storage).
Attach Permissions:

4.Attach the AmazonS3FullAccess policy to the Lambda execution role or create a custom policy with permissions to put objects into the specific bucket:
json
Copy code
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:PutObject",
      "Resource": "arn:aws:s3:::my-pdf-storage/*"
    }
  ]
}


5.Test the Function:

Create a test event in the Lambda console:
json
Copy code
{
  "body": "{\"file_content\": \"<base64_encoded_content>\", \"file_name\": \"example.pdf\"}"
}


6.Replace <base64_encoded_content> with the base64-encoded representation of a sample PDF file.
Run the test and verify that the file is uploaded to the specified S3 bucket.
Deploy with API Gateway (Optional):

NOTE:
Create an API Gateway to expose the Lambda function as an HTTP endpoint.
Use a POST method to send the file and its metadata.
Example cURL Command to Test with API Gateway
bash
Copy code
curl -X POST https://<API_GATEWAY_ENDPOINT> \
-H "Content-Type: application/json" \
-d '{"file_content": "<base64_encoded_content>", "file_name": "example.pdf"}'
Replace <API_GATEWAY_ENDPOINT> and <base64_encoded_content> as necessary.

## Compatibility
Tested on modern browsers like Chrome, Firefox, and Edge.

## Author
Developed by [sruthika T].

