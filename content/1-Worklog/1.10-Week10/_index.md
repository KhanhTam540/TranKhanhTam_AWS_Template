---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---



### Week 10 Objectives:

* Build the core AWS infrastructure for the SmartHospital P2TB system using AWS CDK.  

* Configure authentication, backend APIs, database storage, frontend hosting, and CloudFront distribution.  

* Prepare the initial dataset and verify the connection between frontend, backend, Cognito, and DynamoDB.  

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - AWS CDK Setup: Configure the main AWS resources in CDK, including Lambda functions, DynamoDB table, Cognito User Pool, API Gateway routes, S3 bucket, and CloudFront distribution.                                                                                                   | 22/06/2026 | 22/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   | - Cognito Configuration: Set up user authentication, create Cognito groups, and verify the login flow for Admin, Doctor, Medical Staff, and Patient accounts.                                             |23/06/2026 | 23/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - Backend API Deployment: Deploy initial Lambda APIs for user profile, patient information, doctor information, appointment data, and medical record access. | 24/06/2026 | 24/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Frontend Deployment: Build the React frontend, upload static files to S3, configure CloudFront, and test access through the production domain.                            | 25/06/2026 | 25/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Dataset Seeding and Verification: Create demo data for users, patients, doctors, appointments, records, tests, invoices, and verify that the frontend can load data from DynamoDB.                                                                                     | 26/06/2026 | 26/06/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Week 10 Achievements:

* Successfully configured the main AWS infrastructure using CDK.

* Completed Cognito authentication and role group setup.

* Deployed the first backend APIs with Lambda and API Gateway.

* Published the frontend through S3 and CloudFront.

* Created the first dataset for system testing.
