# Apogee-hybrid-installation-


Enabling Required APIs for Apigee Hybrid v1.9
Overview
To deploy Apigee Hybrid v1.9, specific Google Cloud APIs must be enabled. This guide provides step-by-step instructions to activate these APIs using the gcloud command-line interface (CLI).

Prerequisites
Before proceeding, ensure you meet the following requirements:

You have a Google Cloud project with necessary permissions to enable APIs.

The gcloud CLI tool is installed and configured on your system.

Steps to Enable Required APIs
1. Authenticate with Google Cloud
Run the following command to log in:

bash
Copy
Edit
gcloud auth login
This will open a browser window where you need to sign in with your Google Cloud account.

2. Set Your Google Cloud Project
Specify the project in which you want to enable the APIs:

bash
Copy
Edit
gcloud config set project PROJECT_ID
Replace PROJECT_ID with your actual Google Cloud project ID.

3. Enable Essential APIs
Execute the following commands to enable the required APIs for Apigee Hybrid:

bash
Copy
Edit
gcloud services enable apigee.googleapis.com
gcloud services enable compute.googleapis.com
gcloud services enable iam.googleapis.com
gcloud services enable cloudresourcemanager.googleapis.com
gcloud services enable apigeeconnect.googleapis.com
These APIs support core Apigee functionalities, resource management, and connectivity.

4. Verify Enabled APIs
To confirm that the necessary APIs are enabled, use:

bash
Copy
Edit
gcloud services list --enabled
Check the output to ensure that all the required APIs are listed.

Additional Information
For more details on Apigee Hybrid installation, refer to the official documentation.

If you encounter permission issues, ensure your account has the roles/owner or roles/editor role in the Google Cloud project.

Following these steps ensures your project is correctly configured for deploying Apigee Hybrid v1.9.
