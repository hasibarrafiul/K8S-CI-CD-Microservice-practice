# 🚀 Cloud-Native Microservices Platform with Kubernetes & GitOps
A production-style cloud-native microservices project demonstrating modern DevOps and fullstack deployment practices using Kubernetes, GitOps, and Infrastructure as Code.
This repository simulates a real-world enterprise environment where applications are built, containerized, deployed, and continuously delivered to a Kubernetes cluster using a GitOps workflow.
---
# 🏗 Architecture Overview
## High-Level Flow
Developer Push → GitHub Actions (CI) → Docker Image Build → Container Registry → GitOps (Argo CD) → Kubernetes Cluster (AKS)
---
## System Components
### 🔹 Application Layer
- Frontend (React)
- Backend Microservices (Node.js / NestJS)
- REST-based service communication
- Stateless containerized services
### 🔹 Infrastructure Layer
- Kubernetes manifests
- Docker containerization
- Terraform for Infrastructure as Code
- Argo CD for GitOps-based deployment
### 🔹 CI/CD Layer
- GitHub Actions for Continuous Integration
- Argo CD for Continuous Deployment
- Declarative Kubernetes configuration
---
# ⚙️ Technology Stack
## Application
- Node.js
- NestJS
- React
- TypeScript
## Infrastructure
- Kubernetes (AKS compatible)
- Docker
- Terraform
- Argo CD
## CI/CD
- GitHub Actions
- GitOps deployment workflow
---
# 🎯 Project Goals
This project demonstrates:
- Designing microservices for containerized environments
- Automating CI pipelines for Docker-based applications
- Implementing GitOps-based CD using Argo CD
- Managing infrastructure declaratively with Terraform
- Enabling scalable and reproducible deployments
- Separating CI and CD responsibilities clearly
---
# 🔍 Key Design Decisions
## Why Microservices?
To simulate independently deployable services with clear domain boundaries and improved scalability.
## Why Kubernetes?
To manage container orchestration, enable scaling, rolling deployments, and self-healing capabilities.
## Why GitOps (Argo CD)?
- Declarative deployment model
- Automatic cluster reconciliation
- Version-controlled infrastructure and deployment history
- Safer rollback capability
## Why Terraform?
- Infrastructure reproducibility
- Version-controlled provisioning
- Environment consistency across deployments
## Why Separate CI and CD?
CI:
- Builds and validates code
- Builds Docker images
- Pushes images to registry
CD:
- Syncs Kubernetes manifests
- Deploys changes automatically
- Maintains desired cluster state
This separation reflects modern production-grade DevOps practices.
---
# 📂 Repository Structure
apps/ → Application services (frontend + backend)
k8s/ → Kubernetes manifests
terraform/ → Infrastructure provisioning scripts
.github/workflows/ → GitHub Actions CI pipelines
docker-compose.yml → Local development environment
---
# 🔄 CI/CD Workflow
## Continuous Integration (CI)
1. Developer pushes code
2. GitHub Actions pipeline:
   - Install dependencies
   - Build application
   - Build Docker images
   - Push images to container registry
## Continuous Deployment (CD)
1. Kubernetes manifests updated in repository
2. Argo CD detects change
3. Cluster state reconciled automatically
4. Rolling update performed in Kubernetes
---
# 📈 Scalability & Reliability Concepts
- Stateless microservices
- Containerized deployments
- Rolling update strategy
- Horizontal scaling capability (HPA-ready structure)
- Health check support (liveness/readiness probes)
- Declarative infrastructure management
---
# 🧪 Local Development
Run the full stack locally using Docker Compose:
```bash
docker-compose up --build
```
This allows local testing without requiring Kubernetes.
☁️ Deployment to Kubernetes (AKS Example)
1. Provision infrastructure using Terraform
2. Configure Kubernetes context
3. Install Argo CD in cluster
4. Connect repository to Argo CD
5. Sync application
6. All deployments follow a declarative GitOps workflow.

🚀 What This Project Demonstrates
1. Real-world CI/CD implementation
2. GitOps deployment workflow
3. Kubernetes-based application architecture
4. Infrastructure as Code best practices
5. Production-style system design thinking
6. Clear separation of build and deployment responsibilities

🔮 Future Improvements
1. Add automated testing in CI pipeline
2. Add monitoring (Prometheus + Grafana)
3. Add distributed tracing
4. Implement blue-green or canary deployment
5. Multi-environment (dev / staging / prod) setup
   
👤 Author
Hasib Ar Rafiul Fahim
Full-Stack Engineer | Cloud-Native Systems <br>
Tokyo, Japan<br>
GitHub: https://github.com/hasibarrafiul<br>
LinkedIn: https://linkedin.com/in/hasibarrafiul
