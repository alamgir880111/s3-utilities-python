AWS S3 Utilities Using Python and Boto3

A Python-based AWS utility tool that uses Object-Oriented Programming (OOP) and Boto3 to interact with Amazon S3. The application supports listing S3 buckets, creating buckets, and uploading files.

Features

List S3 Buckets: Retrieve and display bucket names from an AWS account.

Create S3 Buckets: Create a new S3 bucket in a specified AWS Region.

Upload Files: Upload local files to an S3 bucket.

OOP-Based Design: Organize AWS operations into a reusable AWSUtils class.

Boto3 Integration: Interact with AWS S3 through the AWS SDK for Python.

Technology Stack

Python 3

Boto3

Amazon S3

AWS CLI (recommended for credential configuration)

Project Structure

python-s3-utilities/
├── s3_utilities2.py
├── app2.log
└── README.md

app2.log is an example local file used for the upload operation.

Prerequisites

Before running the application, make sure you have:

Python 3 installed.

An AWS account.

AWS credentials configured securely.

Appropriate IAM permissions for listing buckets, creating buckets, and uploading objects.

A globally unique S3 bucket name.

Installation

1. Clone the repository

git clone YOUR_GITHUB_REPOSITORY_URL

Replace YOUR_GITHUB_REPOSITORY_URL with your actual GitHub repository URL.

2. Navigate to the project directory

cd python-s3-utilities

3. Create a virtual environment

python -m venv myenv

Activate it on Windows PowerShell:

.\myenv\Scripts\Activate.ps1

4. Install Boto3

pip install boto3

To save the dependency:

pip freeze > requirements.txt

AWS Configuration

Configure your AWS credentials using the AWS CLI:

aws configure

Provide your AWS access key, secret access key, default Region, and output format when prompted.

Verify that your credentials work:

aws sts get-caller-identity

Security: Never commit AWS access keys, secret keys, or other credentials to GitHub. Prefer IAM roles or temporary credentials when available.

Usage

Run the script:

python s3_utilities2.py

The script attempts to:

List existing S3 bucket names.

Create a bucket named new-lullu-pullu1 in eu-north-1.

Upload app2.log to the bucket named rahman-ki-ldk with the object key lala.

Important: These are the bucket names currently hardcoded in the example script. Update them to match your own AWS resources before running it.

Code Overview

AWSUtils Class

The class groups AWS S3 operations into reusable methods.

Method

Purpose

__init__()

Initializes the S3 client.

get_connection(service)

Creates a Boto3 client for the specified AWS service.

show_buckets()

Lists and prints bucket names.

create_buckets(bucket_name, region)

Attempts to create an S3 bucket.

upload_file(file_name, bucket_name, object_name)

Uploads a local file to S3.
