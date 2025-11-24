# 🚀 AWS Serverless Task Management API

## 📖 The Project Story

This repository documents my journey of building a production-ready serverless REST API on AWS. This is **Project #3** from the guide ["5 AWS Projects To Get You Hired"](https://learn.thecloudengineers.com/5-aws-projects-to-get-you-hired) by Lefteris Karageorgiou.

After mastering traditional three-tier architecture in Project 2, I'm now diving into the world of serverless computing - the future of cloud development. This project demonstrates modern cloud patterns that scale infinitely, cost pennies to operate, and require zero server maintenance.

## 🏗️ Architecture

```mermaid
graph TB
    classDef client fill:#1e40af,stroke:#3b82f6,color:#ffffff
    classDef api fill:#b91c1c,stroke:#dc2626,color:#ffffff  
    classDef lambda fill:#047857,stroke:#059669,color:#ffffff
    classDef db fill:#7e22ce,stroke:#9333ea,color:#ffffff

    CLIENT[🌐 Web/Mobile Clients]
    
    APIGW[API Gateway<br/>REST API Endpoints]
    
    LAMBDA_GET[Lambda Function<br/>GET /tasks]
    LAMBDA_CREATE[Lambda Function<br/>POST /tasks]
    LAMBDA_UPDATE[Lambda Function<br/>PUT /tasks/:id]
    LAMBDA_DELETE[Lambda Function<br/>DELETE /tasks/:id]
    
    DYNAMO[(DynamoDB<br/>NoSQL Database)]

    CLIENT --> APIGW
    APIGW --> LAMBDA_GET
    APIGW --> LAMBDA_CREATE
    APIGW --> LAMBDA_UPDATE
    APIGW --> LAMBDA_DELETE
    LAMBDA_GET --> DYNAMO
    LAMBDA_CREATE --> DYNAMO
    LAMBDA_UPDATE --> DYNAMO
    LAMBDA_DELETE --> DYNAMO

    class CLIENT client
    class APIGW api
    class LAMBDA_GET,LAMBDA_CREATE,LAMBDA_UPDATE,LAMBDA_DELETE lambda
    class DYNAMO db



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
