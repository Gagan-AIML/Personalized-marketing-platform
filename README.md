# Personalized-Marketing-Platform
📌 Project Overview

The AI-Driven Personalized Marketing Platform is a full-stack web application designed to deliver targeted marketing campaigns to customers based on their behavior and profile data. The platform enables marketers to create, launch, and analyze personalized campaigns while ensuring scalability, security, and cloud readiness using AWS services.

The system is first developed and validated locally, then extended to an AWS-compatible architecture using DynamoDB, SNS, and boto3, with local AWS testing supported via Moto.

🎯 Project Goals
Increase user engagement
Improve conversion rates
Enhance customer retention
Deliver the right message to the right user at the right time

🧠 Where AI Is Used
This project is AI-driven by design:
Customer behavior and campaign history are analyzed
A recommendation logic (rule-based / ML-ready) selects the most relevant campaign
Campaign performance metrics feed back into future decisions

In the local prototype, personalization logic simulates ML behavior.
In production, this can be replaced with:
Scikit-learn models
AWS SageMaker
Real-time inference via Lambda

🏗️ System Architecture
Local Version
Frontend: HTML, CSS (Jinja templates)
Backend: Flask

Data Storage: In-memory / local structures
AI Logic: Rule-based personalization (ML-ready)
AWS-Compatible Version
Compute: Flask app (EC2 / Elastic Beanstalk ready)
Database: Amazon DynamoDB
Messaging: Amazon SNS (email/SMS/push notifications)
Security: IAM roles and policies
Testing: Moto (mock AWS services locally)

🧩 Features
User Side
User registration and login
Dashboard view
Campaign notifications
Personalized campaign delivery
Admin / Marketing Manager
Create campaigns
Launch campaigns for specific customers
View analytics
Delete customers or campaigns
Analytics
Campaign performance tracking
Filter/search analytics by customer
Engagement metrics (sent, opened, clicked – simulated)

📂 Project Structure
AWS Project/
│
├── app.py                     # Local (non-AWS) version
├── app_aws.py                 # AWS-compatible Flask app
├── test_app_aws_moto.py       # Moto test runner (no real AWS)
│
├── templates/                 # HTML templates
├── static/                    # CSS, assets
│
├── requirements.txt
├── README.md
├── .gitignore
│
└── venv/                      # Local virtual environment (ignored)

🧪 Local AWS Testing (Without Real AWS)

The project uses Moto to mock AWS services.

Run AWS version locally:
python test_app_aws_moto.py


This:
Creates mock DynamoDB tables
Creates a mock SNS topic
Runs the Flask app locally
Does not require AWS credentials or billing

📊 DynamoDB Tables Used
Table Name	Purpose	Primary Key
MarketingUsers	Platform users	username
MarketingCustomers	Marketing customers	customer_id
MarketingCampaigns	Campaign data & analytics	campaign_id

🔐 Security Considerations
AWS credentials are never committed
.env, venv/, and model files are ignored via .gitignore
IAM roles recommended for production deployment

🚀 Future Enhancements
Real ML model integration (SageMaker)
Real-time event streaming (Kinesis)
Multi-channel delivery (Email, SMS, Push)
Campaign A/B testing
Advanced customer segmentation

🛠️ Technologies Used
Python
Flask
HTML / CSS
AWS DynamoDB
AWS SNS
boto3
Moto

Git & GitHub
👤 Author
Gagan
AI & ML Student
GitHub: https://github.com/Gagan-AIML
