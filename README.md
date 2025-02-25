# Health-Hub-Vision-AI

## Implementation of a Machine Learning Solution Capable of Identifying Diseases in Medical Images (X-Rays and Others) Using the Google Cloud Vision AI Service

<p align="center">
<img src="https://i.imgur.com/v7sJN9A.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

## Project Description
The Health Hub AI project integrates serverless technologies, cloud computing, and machine learning to enhance medical care efficiency. Utilizing AWS services, Google Cloud Vision AI, and secure data workflows, this solution automates medical image analysis, improves record management, and accelerates diagnostics for patients and healthcare providers.

<p align="center">
<img src="https://i.imgur.com/Vhh0Mxs.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

It integrates AWS and Google Cloud services for scalability and efficiency. Amazon Cognito ensures secure authentication, while Amazon S3 hosts the frontend.
The backend, managed via API Gateway and AWS Lambda, processes requests and integrates with Google Cloud Vision for image analysis.
Results are stored in DynamoDB, and the workflow is monitored using CloudWatch Logs. This hybrid approach leverages multi-cloud capabilities for enhanced medical diagnostics.

## Objectives
1. **Build a secure, scalable Health Hub application** integrating backend and frontend services.
2. **Enable image analysis** using Google Cloud Vision AI for medical records.
3. **Validate AI-powered functionalities**, including medical image processing and text-to-speech for enhanced patient-doctor interactions.
4. **Deploy and demonstrate** a complete serverless architecture while ensuring proper resource cleanup to prevent unnecessary costs.

## Project Solution

### Part 1: Backend Implementation

#### Step 1: Environment Setup
- Access AWS EC2 to create a virtual workstation.
- Download Health Hub application files and organize the backend folder.
- Install dependencies using npm install and other required commands.

#### Step 2: Enable Google Cloud Vision API
- Access Google Cloud Console and enable the Cloud Vision API for analyzing medical images.

#### Step 3: Create Google Cloud Service Account
- Set up a service account with Cloud Vision API Service Agent roles.
- Generate and save a JSON key (e.g., GoogleCredentials.json).

#### Step 4: Credential Integration
- Create a google-credentials.json file within the application, copying the JSON key content.
- Validate backend configurations in serverless.yml for smooth integration.

#### Step 5: Deploy Backend Services
- Execute serverless deployment commands (sls deploy) for multiple modules, creating backend services for AI speech, transcription, and image analysis.
- Use AWS CloudFormation to validate successful deployment of resources like Lambda functions and API Gateway endpoints.

### Part 2: Frontend Implementation

#### Step 1: Preparing Dependencies
- Navigate to the frontend directory of the application.
- Review dependencies (package.json) and install them using npm install.

#### Step 2: Configuring API Gateway
- Retrieve the API Gateway endpoint URL from AWS.
- Update the .env file in the frontend folder with the API Gateway URL.

#### Step 3: Launching the Application
- Start the Health Hub application using the public IP of the EC2 instance.
- Access the application via a browser using the appropriate port number.

#### Step 4: Image Analysis Validation
- Log in as a doctor to utilize the Image Analysis feature.
  - Example workflow: Select a patient (e.g., Ava Brown) → Upload an X-ray image → Run Cloud Vision AI analysis.
- Confirm accurate AI-generated image insights.
- Log in as a patient to view results integrated within their medical records.

## Tools and Technologies

### Cloud Platforms and AI Services:
- **AWS**: EC2, API Gateway, Lambda, Cognito, S3, DynamoDB, and CloudFormation.
- **Google Cloud**: Cloud Vision AI, IAM, and Service Accounts.

### Programming & Frameworks:
- Node.js, NPM, and Serverless Framework.

### Monitoring and Security:
- CloudWatch for log monitoring.
- Secure authentication and permission configurations via Cognito and IAM roles.

## Step-By-Step Directions

### Solution Part 1: Backend Implementation

#### Step 1: Setup and File Preparation
1. Access the AWS EC2 workstation environment.

<p align="center">
<img src="https://i.imgur.com/Vhh0Mxs.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

2. Download the necessary application files.
   - Organize these files within the virtual machine.

<p align="center">
<img src="https://i.imgur.com/qAX9Qj7.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

3. Run the commands to prepare the backend services.
   - Navigate to the backend folder.

<p align="center">
<img src="https://i.imgur.com/05kiEbb.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
   - Execute npm install to install required packages.

<p align="center">
<img src="https://i.imgur.com/Y2nq2Kc.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
   - Use the Linux 4 command loop to run npm install for other services.

<p align="center">
<img src="https://i.imgur.com/DgN28Bb.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
#### Step 2: Enabling GCP Services
1. Log in to the Google Cloud Console and enable the required APIs:
   - Navigate to API & Services.
   - Search for Cloud Vision API Service and enable it.

<p align="center">
<img src="https://i.imgur.com/Y6UtrWY.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

#### Step 3: Create a Service Account in GCP
1. Navigate to IAM & Admin > Service Accounts and create a new service account:
   - Name the account appropriately (e.g., tcb-hh-sa).

<p align="center">
<img src="https://i.imgur.com/eSy5XLA.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
   - Assign the Cloud Vision API Service Agent role.

<p align="center">
<img src="https://i.imgur.com/Zbyr5Gd.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
2. Generate a JSON key for the service account:
   - In the service account, navigate to Keys, click Add Key > Create New Key (select JSON format).
   - Save the generated JSON file as GoogleCredentials.json.

<p align="center">
<img src="https://i.imgur.com/dDOolj5.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/1f2GHzp.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

#### Step 4: Integrate Credentials into the Application
1. Copy the JSON key contents into a new file:
   - Create a file google-credentials.json within the application.
   - Paste the key data and save it.

<p align="center">
<img src="https://i.imgur.com/ODNNKCG.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/634HfXj.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

#### Step 5: Deploy Backend Services
1. Execute the deployment commands from the backend folder:
   - Utilize serverless framework commands to deploy services 

<p align="center">
<img src="https://i.imgur.com/frQxDF3.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

2. Monitor the deployment status via AWS CloudFormation.
   - Validate the creation of resources, particularly the new medical image service.

<p align="center">
<img src="https://i.imgur.com/HJlCqN3.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/oNjWldV.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
#### Step 6: Code Validation
1. Inspect the backend code:
   - Check serverless.yml for variable configurations using google-credentials.json.
   - Ensure smooth integration for image analysis.

<p align="center">
<img src="https://i.imgur.com/7QfCaTL.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
2. Review exception handling mechanisms for robust error management.

<p align="center">
<img src="https://i.imgur.com/C5KxUc2.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
### Solution Part 2: Frontend Implementation

#### Step 1: Prepare the Frontend
1. Navigate to the frontend folder:

<p align="center">
<img src="https://i.imgur.com/KvDhyoS.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
   - Use the cat command to review dependencies in package.json.

<p align="center">
<img src="https://i.imgur.com/GKkVRZT.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
   - Use tree to confirm added services for the medical records module.

<p align="center">
<img src="https://i.imgur.com/2ACn50N.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

2. Install frontend dependencies:

<p align="center">
<img src="https://i.imgur.com/c87Hhp0.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

#### Step 2: Configure API Gateway
1. Retrieve the API Gateway URL from AWS:

<p align="center">
<img src="https://i.imgur.com/7515XYe.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/7uWG6P1.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />
 
   - Copy the URL of the deployed endpoint.

<p align="center">
<img src="https://i.imgur.com/cA7ZWsr.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/SRSWLPk.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/tz3Kd7J.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

2. Update the .env file in the frontend folder:
   - Create a copy of the .env file.

<p align="center">
<img src="https://i.imgur.com/DiJLETQ.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

#### Step 3: Launch the Application
1. Start the Health Hub serverless application:
   - Use the public IP of the EC2 instance with the appropriate port.
   - Open the frontend application in a web browser.

<p align="center">
<img src="https://i.imgur.com/51GD4Zl.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/YcElQTq.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

2. Register doctor and patient profiles:
   - Example: Register a patient named Ava Brown.

<p align="center">
<img src="https://i.imgur.com/95FlJRn.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/KqrMtKY.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

#### Step 4: Test Image Analysis Feature
1. Log in as the doctor:
   - Navigate to the Image Analysis feature.

<p align="center">
<img src="https://i.imgur.com/XpJTPGQ.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

<p align="center">
<img src="https://i.imgur.com/XrQqRra.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

   - Select the patient (e.g., Ava Brown) and upload an X-ray image.

<p align="center">
<img src="https://i.imgur.com/uQ2Oir2.png" height="80%" width="80%" alt="Pic"/>
<br />
<br />

This project highlights the transformative role of AI and cloud solutions in healthcare, enabling faster diagnosis, enhanced patient outcomes, and streamlined workflows for medical professionals. Congratulations on a successful implementation!

## Conclusion

### Challenges Encountered
1. Synchronizing multi-cloud service configurations (AWS and Google Cloud).
2. Validating secure communication between backend, frontend, and AI services.
3. Ensuring smooth deployment and cleanup of serverless resources.

### Lessons Learned
- Importance of precise API and service configuration for multi-cloud solutions.
- Practical strategies for implementing AI features in healthcare.
- Enhanced understanding of serverless architecture and its benefits.

### Future Improvements
1. Incorporate advanced AI models trained on larger datasets for diverse imaging scenarios.
2. Add multi-language support to broaden accessibility for international healthcare providers.
3. Optimize the system to integrate with real-time streaming X-rays for critical care..
