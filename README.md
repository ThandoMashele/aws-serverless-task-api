# 🚀 AWS Serverless Task Management API

## 📖 The Project Story

This repository documents my journey of building a production-ready serverless REST API on AWS. This is **Project #3** from the guide ["5 AWS Projects To Get You Hired"](https://learn.thecloudengineers.com/5-aws-projects-to-get-you-hired) by Lefteris Karageorgiou.

After mastering traditional three-tier architecture in Project 2, I'm now diving into the world of serverless computing - the future of cloud development. This project demonstrates modern cloud patterns that scale infinitely, cost pennies to operate, and require zero server maintenance.

## 🏗️ Architecture


**Components:**
- **API Gateway**: REST API endpoints
- **Lambda Functions**: 4 functions for CRUD operations  
- **DynamoDB**: NoSQL database for task storage

## 📋 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/tasks` | List all tasks |
| POST | `/tasks` | Create a new task |
| PUT | `/tasks/{id}` | Update a task |
| DELETE | `/tasks/{id}` | Delete a task |

## 🚀 Implementation Progress

| Phase | Status | Date | Notes & Learnings |
| :--- | :---: | :---: | :--- |
| **Phase 0: Project Setup** | ✅ | 23/11/2025 | Created GitHub repository with complete documentation and code structure. Ready for manual deployment. |
| **Phase 1: Manual Deployment** | 🔄 | | *Creating DynamoDB table and Lambda functions...* |
| **Phase 2: API Gateway Setup** | ❌ | | |
| **Phase 3: Testing & Validation** | ❌ | | |
| **Phase 4: Terraform Conversion** | ❌ | | |

## 🛠️ Technologies & AWS Services

- **Compute:** AWS Lambda
- **API Management:** Amazon API Gateway  
- **Database:** Amazon DynamoDB
- **Infrastructure:** Terraform (Future)
- **Runtime:** Node.js 18.x

## 📂 Repository Structure
aws-serverless-task-api/
├── docs/

│ ├── ARCHITECTURE.md

│ └── DEPLOYMENT.md

├── src/

│ ├── lambda-get-tasks/index.js

│ ├── lambda-create-task/index.js

│ ├── lambda-update-task/index.js

│ ├── lambda-delete-task/index.js

│ └── package.json

├── infrastructure/

│ ├── providers.tf

│ ├── variables.tf

│ ├── main.tf

│ └── outputs.tf

├── README.md

└── .gitignore
