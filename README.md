ContentIQ: AI-Powered Compliance Platform
Overview
ContentIQ is a scalable, cloud-native platform designed to analyze compliance documents for healthcare (HIPAA), supply chain, and ESG use cases. Built with a microservices architecture, it leverages AWS EKS, FastAPI, Django, LangChain, and React to deliver intelligent document processing, real-time Q&A, and compliance insights. This project showcases advanced skills in AI/ML, cloud computing, DevOps, and full-stack development, tailored for FAANG-level engineering roles.
Key Features

Document Upload: Supports multi-format files (PDF, DOCX, TXT) with asynchronous processing via SQS and Celery.
AI Insights: Uses LangChain for Retrieval-Augmented Generation (RAG) and fine-tuned DistilBERT for HIPAA compliance checks.
Intelligent Q&A: Enables natural language queries about documents, powered by pgvector for vector search.
Real-Time Collaboration: Facilitates document sharing with WebSocket notifications.
Analytics Dashboard: Provides compliance and usage metrics via a React frontend.
Scalability & Security: Deploys on AWS EKS with auto-scaling, IAM, KMS, and Kubernetes network policies.

Tech Stack

Backend: Django (User Service), FastAPI (Document, AI, Notification Services), Flask (Analytics)
AI/ML: LangChain, fine-tuned DistilBERT, PostgreSQL with pgvector
Cloud: AWS EKS, RDS, ElastiCache, S3, Amplify
DevOps: Jenkins, Kubernetes, Docker
Frontend: React, Tailwind CSS

Getting Started
Prerequisites

Python 3.10+, Node.js 18+
Docker and Docker Compose
AWS CLI (for deployment)
Git

Installation

Clone the repository:git clone https://github.com/your-username/contentiq.git
cd contentiq


Install dependencies:pip install -r requirements.txt
npm install


Configure environment variables (see .env.example):cp .env.example .env


Start services:docker-compose -f docker-compose.local.yml up



Running Tests
pytest --cov=. --cov-report=html
npm test

Development Standards

Code Style: PEP 8, enforced via pre-commit with flake8 and black.
Testing: >80% coverage with pytest (unit, integration) and Cypress (end-to-end).
Documentation: OpenAPI/Swagger for APIs, architecture diagrams in docs/.
CI/CD: Jenkins pipeline for automated builds, tests, and deployments.

Project Structure
contentiq/
├── backend/
│   ├── user_service/       # Django-based authentication
│   ├── document_service/   # FastAPI for document processing
│   ├── ai_service/         # FastAPI for AI and RAG
│   ├── analytics_service/  # Flask for metrics
│   ├── notification_service/ # FastAPI for WebSocket notifications
├── frontend/               # React dashboard
├── kubernetes/             # Helm charts and manifests
├── docs/                   # Architecture diagrams, API specs
├── tests/                  # Pytest and Cypress tests
├── .gitignore
├── LICENSE
├── README.md

Contributing
Contributions are welcome! Please follow the contributing guidelines and submit pull requests.
License
This project is licensed under the MIT License - see the LICENSE file for details.
Contact
For questions, reach out via GitHub Issues or your-email@example.com.
