## DevOps Interview Preparation

---

<details>
<summary><b>1. Tell me about your-self</b></summary>

<br>

Hi, thanks for the opportunity.  

I’m Naveen Thrukapally, and I have around 4 years of experience as a DevOps Engineer, focusing on building scalable and automated deployment systems.

In my current role, I work extensively with Docker and Kubernetes, where I containerize applications and manage production deployments, helping improve scalability and maintain high availability.

I’ve built and maintained CI/CD pipelines using Jenkins, automating build, testing, and deployment processes, which reduced deployment time by around 40–50% and improved release reliability.

I’ve also integrated tools like SonarQube and Trivy for code quality and security checks within the pipeline.

On the infrastructure side, I use Terraform to provision and manage AWS resources like VPC, EKS, and load balancers, enabling consistent and repeatable environment setups

On the cloud side, I have experience with AWS services such as VPC, ELB, Route 53 for networking, IAM for access control, and services like S3, DynamoDB, and EKS for storage and container orchestration.

Additionally, I’m involved in production support—handling issues like failed deployments, pod restarts, and performance bottlenecks to ensure system stability.

Overall, my focus is on automation, reliability, and smooth delivery of applications.

</details>

<details>
<summary><b>2. Explain your project in detail</b></summary>

<br>

Sure. In my recent role, I worked on a banking domain application which follows a 3-tier architecture with multiple microservices.

The frontend was developed using React, backend services were built using Java-based microservices, and the database layer used MySQL.

From a DevOps perspective, I was responsible for designing and managing the CI/CD pipeline and infrastructure.

We used Git for version control, and Jenkins pipelines were triggered on every code push.

The pipeline included:
- Build using Maven
- Code quality check using SonarQube
- Security scan using Trivy

After successful build:
- Docker image was created
- Pushed to container registry

For deployment:
- Kubernetes (EKS)
- Helm charts for configuration
- ArgoCD for GitOps-based deployment

Infrastructure:
- Provisioned using Terraform (VPC, EKS, IAM, Load Balancer)

Monitoring:
- Prometheus + Grafana for metrics and alerts

I was also involved in production troubleshooting like pod failures, deployment issues, and performance bottlenecks.

Overall, my role was to ensure smooth, automated, and reliable deployments.

---

### 🧠 Easy Structure to Remember

👉 Use this flow:

1️⃣ Architecture (3-tier + microservices)  
2️⃣ CI/CD (Jenkins pipeline)  
3️⃣ Build & Quality (Maven + SonarQube + Trivy)  
4️⃣ Containerization (Docker)  
5️⃣ Deployment (K8s + Helm + ArgoCD)  
6️⃣ Infrastructure (Terraform + AWS)  
7️⃣ Monitoring (Prometheus + Grafana)  
8️⃣ Troubleshooting (real issues)

---

### 💥 Pro Tip (Say if needed)

“We focused on automation and zero-downtime deployments to improve reliability and release speed.”

</details>
