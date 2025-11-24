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


- **API Gateway** → **Lambda Functions** → **DynamoDB**
- Four endpoints: GET /tasks, POST /tasks, PUT /tasks/:id, DELETE /tasks/:id
- Serverless, auto-scaling, cost-effective

## 🚀 Implementation Progress

| Phase | Status | Date |
|-------|--------|------|
| Project Setup | ✅ | 23/11/2025 |
| Manual Deployment | 🔄 | |
| API Gateway Setup | ❌ | |
