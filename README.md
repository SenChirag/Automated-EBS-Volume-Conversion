# Automated EBS VOlume Conversion

The EBS Volume Converter project is a Python Script that converts GP2 (General Purpose SSD) EBS volumes to GP3 (General Purpose SSD) volumes. It utilizes the Boto3 library and AWS Lambda to automate the conversion process, providing a seamless transition between storage types. The project also triggers CloudWatch logs to track EBS volume creation events. 

## Features

- Conversion of GP2 EBS volumes to GP3 for improved performance and cost optimization.
- Utilization of the Boto3 library to interact with AWS services and manage EBS volumes.
- Integration with AWS Lambda for serverless execution of the conversion process.
- Triggering of CloudWatch logs to track EBS volume creation events.
- IAM policy configuration to grant the necessary permissions for EBS volume conversion.

## Requirements

- Python 3.x
- Boto3 library
- AWS Lambda
- AWS CloudWatch
- IAM role or user with appropriate permissions

## Installation

1. Clone the project repository:

   ```bash
   git clone https://github.com/SenChirag/Automated-EBS-Volume-Conversion.git
   ```

2. Navigate to the project directory:

   ```bash
   cd EBS_Volume_convertor
   ```

3. Install the required dependencies:

   ```bash
   pip install boto3
   ```

## Usage

1. Configure the AWS credentials on your local machine to grant access to your AWS account.

2. Customize the configuration settings in the `config.py` file to match your specific requirements. Specify the source GP2 volume IDs and other parameters related to the conversion process.

3. Set up the necessary IAM policy to allow the EBS volume conversion. 

4. Deploy the Python code to an AWS Lambda function:

   - Create a new Lambda function in the AWS Management Console.
   - Upload the Python code to the function.
   - Set the appropriate runtime and permissions for the Lambda function.
   - Configure the required environment variables and triggers, such as CloudWatch Events.

5. Test the EBS volume conversion by creating new GP2 EBS volumes. The Lambda function will automatically trigger the conversion process and output logs in CloudWatch.

6. Monitor the CloudWatch logs to track the status and progress of the EBS volume conversion.

7. Customize the project as needed, such as adding error handling or incorporating additional features.


## Contributing

Contributions are welcome! If you have any ideas, improvements, or bug fixes, please submit a pull request. Make sure to follow the existing code style and provide clear documentation for your changes.
