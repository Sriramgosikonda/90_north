# Project Overview

This project includes implementations for three key tasks:
1. **Frontend Development**: A responsive webpage with a fixed navbar, collapsible left menu, and dynamic scaling based on screen width.
2. **Django Chat Application**: A real-time chat application with user authentication, message persistence, and WebSocket integration.
3. **AWS Lambda Functions**: Serverless functions for arithmetic operations and file uploads to an S3 bucket.

## Frontend Development

### Features
- Fixed navbar.
- Layout with left menu, main content, and right panel.
- Collapsible left menu.
- Responsive scaling for various screen sizes.

### How to Run
1. Open `frontend_task.html` in any modern web browser.
2. Resize the browser window to test responsive scaling and collapsible menu functionality.

## Django Chat Application

### Features
- User authentication (sign-up and login).
- List of all registered users.
- Persistent chat with message history.
- WebSocket for real-time communication.

### Setup Instructions
1. Install Django and other dependencies:
   ```bash
   pip install django channels
   ```
2. Create and apply migrations:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```
3. Run the development server:
   ```bash
   python manage.py runserver
   ```
4. Access the application at `http://127.0.0.1:8000/`.

### Notes
- WebSocket integration requires Django Channels setup. Refer to the official [Django Channels documentation](https://channels.readthedocs.io/en/stable/) for configuration.

## AWS Lambda Functions

### Features
1. **Addition Function**: Adds two numbers and returns the result.
2. **File Upload Function**: Uploads a base64-encoded file to an S3 bucket.

### Setup Instructions
1. Navigate to the AWS Lambda console.
2. Create a new Lambda function.
3. Copy and paste the respective function code into the Lambda console.
4. For the file upload function:
   - Add an S3 bucket name in the `BUCKET_NAME` variable.
   - Set up IAM permissions to allow access to the S3 bucket.
5. Test the function using the following JSON payloads:
   - **Addition Function**:
     ```json
     {
         "num1": 5,
         "num2": 10
     }
     ```
   - **File Upload Function**:
     ```json
     {
         "file_name": "example.txt",
         "file_content": "<base64-encoded content>"
     }
     ```

### Notes
- Ensure the IAM role for the Lambda functions has permissions for S3 access.

## Submission Guidelines
1. Add all code files to a GitHub repository.
2. Include this README file in the repository.
3. Host the Django project on PythonAnywhere or AWS.
4. Email the GitHub repository link and hosted project URL to `Hr@enfund.io`.

## Deadline
Submission deadline: **16/01/2025 by 8 PM**.

