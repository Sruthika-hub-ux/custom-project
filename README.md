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

## Compatibility
Tested on modern browsers like Chrome, Firefox, and Edge.

## Author
Developed by [sruthika T].

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




