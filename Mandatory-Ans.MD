## DevOps Interview Preparation

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

1️⃣ Architecture (3-tier + microservices)  
2️⃣ CI/CD (Jenkins pipeline)  
3️⃣ Build & Quality (Maven + SonarQube + Trivy)  
4️⃣ Containerization (Docker)  
5️⃣ Deployment (K8s + Helm + ArgoCD)  
6️⃣ Infrastructure (Terraform + AWS)  
7️⃣ Monitoring (Prometheus + Grafana)  
8️⃣ Troubleshooting (real issues)

### 💥 Pro Tip (Say if needed)

“We focused on automation and zero-downtime deployments to improve reliability and release speed.”

</details>

<details>
<summary><b>3. Explain your CI/CD pipeline</b></summary>

<br>

### ✅ Answer (Interview Ready)

Sure. In our project, the CI/CD pipeline starts when a developer pushes code to the Git repository. This triggers a Jenkins pipeline automatically using a webhook.

In the CI phase, Jenkins pulls the latest code and performs a build using Maven or npm depending on the application.

After the build, we run code quality checks using SonarQube to identify code issues and enforce quality gates.

Once the code passes quality checks, we perform security scanning using Trivy to detect vulnerabilities in dependencies and container images.

After that, we build a Docker image and push it to a container registry like Docker Hub or AWS ECR.

In the CD phase, we follow a GitOps approach using ArgoCD. The updated image tag is pushed to a Git repository that contains Kubernetes manifests or Helm charts.

ArgoCD automatically detects the changes and deploys the new version to the Kubernetes cluster (EKS).

Post-deployment, we monitor the application using Prometheus and Grafana, with alerts configured for failures and performance issues.

This pipeline helped us automate deployments, reduce manual errors, and significantly improve deployment speed and reliability.

---

### 🧠 Easy Structure to Remember

1️⃣ Code Commit (Git)  
2️⃣ Trigger (Webhook → Jenkins)  
3️⃣ Build (Maven/npm)  
4️⃣ Code Quality (SonarQube)  
5️⃣ Security Scan (Trivy)  
6️⃣ Docker Build + Push  
7️⃣ Deploy (ArgoCD → Kubernetes)  
8️⃣ Monitor (Prometheus + Grafana)

### 💥 Real-World Add-On (Important)

- Implemented rollback strategy for failed deployments  
- Used versioned Docker images for traceability  
- Ensured zero-downtime deployments using Kubernetes rolling updates  

### 🎯 Follow-Up Ready

If interviewer asks:

👉 “What happens if SonarQube fails?”

“Pipeline will stop, and we won’t proceed to Docker build until quality gate is passed.”

👉 “How do you rollback?”

“We use previous stable Docker image or revert Git changes in ArgoCD.”

</details>

<details>
<summary><b>4. What are your day-to-day activities as a DevOps Engineer?</b></summary>

<br>

### ✅ Answer (Interview Ready)

As a DevOps engineer, my day-to-day activities involve managing CI/CD pipelines, deployments, infrastructure, and monitoring and supporting development teams to ensure smooth application delivery.

I usually start my day by checking monitoring dashboards like Grafana and Prometheus to see if there are any alerts, failures, or performance issues in the system.

Then I look into Jenkins pipelines to verify if any builds or deployments have failed. If there are failures, I troubleshoot and fix them to keep the pipeline stable.

I work closely with developers to support code deployments, help resolve build issues, and ensure their changes are properly integrated into the CI/CD pipeline.

For deployments, I manage applications on Kubernetes using Helm, making sure releases are smooth and there is no downtime.

I also handle infrastructure tasks using Terraform, like provisioning or updating AWS resources when required.

Apart from this, I spend time troubleshooting issues such as pod failures, service communication problems, or performance bottlenecks.

If there are no major issues, I focus on improving automation, optimizing pipelines, and enhancing monitoring or security.

Overall, my goal is to ensure reliable, fast, and smooth delivery of applications.

---

### 🧠 Easy Structure to Remember

👉 Think in this flow:

1️⃣ Monitoring (Grafana / alerts)  
2️⃣ CI/CD (Jenkins pipelines)  
3️⃣ Collaboration (Dev support)  
4️⃣ Deployment (Kubernetes + Helm)  
5️⃣ Infrastructure (Terraform + AWS)  
6️⃣ Troubleshooting (issues fixing)  
7️⃣ Improvement (automation + optimization)

### 💥 Pro-Level Add-On

“I also ensure proper communication between Dev and QA teams so that releases are not delayed and issues are resolved quickly.”

### 🎯 Follow-Up Ready

👉 If interviewer asks:
“What if there is no issue?”

Say:

“I focus on improving automation, optimizing pipelines, and reducing manual effort to make the system more efficient.”

</details>

## Collaboration with Dev and QA Teams

<details>
<summary><b>5. What do you do when you collaborate with Dev and QA teams?</b></summary>

When I collaborate with development and QA teams, my focus is to ensure smooth and reliable releases.

With the development team, I work closely on integrating their code changes into the CI/CD pipeline. I help them fix build issues, manage dependencies, and ensure proper Dockerization of applications. I also guide them on best practices like writing environment-agnostic code and using proper configuration management.

With the QA team, I ensure that deployment environments are stable and consistent. I support them in setting up test environments, trigger deployments for testing, and help debug any issues they encounter during validation.

If any issues arise during testing or deployment, I work with both teams to identify the root cause—whether it is code-related, configuration-related, or infrastructure-related—and resolve it quickly.

Overall, my role is to act as a bridge between development and QA teams to ensure faster, smoother, and more reliable releases.

---

### 🧠 Simple Way to Remember

🔵 With Developers:
- Help in CI/CD integration  
- Fix build issues  
- Support Docker/image creation  
- Guide best practices  

🟢 With QA:
- Provide stable environments  
- Deploy builds for testing  
- Help debug issues  


### 💥 Real Examples

- If a build fails due to dependency issues, I coordinate with developers to fix it and update the pipeline.  
- If QA finds a bug in staging, I help analyze logs, configurations, and deployments to identify the issue.

### 🔥 Pro-Level Add-On

“I ensure smooth communication between teams so that issues are resolved quickly and releases are not delayed.”  

### 🎯 Quick Fallback Answer

“I help developers with builds and deployments, and QA with testing environments and debugging issues.”

</details>


## Zero Downtime Deployment

<details>
<summary><b> How do you handle zero-downtime deployment in production?</b></summary>

<br>

To achieve zero-downtime deployments, we use deployment strategies and Kubernetes features that ensure the application remains available during updates.

In our project, we primarily used rolling updates in Kubernetes Deployments. This ensures that new pods are created gradually while old pods are terminated only after the new ones become ready.

We configure parameters like maxUnavailable and maxSurge to control how many pods can go down or be added during the update, ensuring no service interruption.

We also define readiness and liveness probes so that traffic is only routed to healthy pods.

In some cases, we use Blue-Green or Canary deployment strategies.  
In Blue-Green, we deploy a new version alongside the old one and switch traffic only after validation.  
In Canary, we release the new version to a small percentage of users and gradually increase traffic.

Additionally, we use tools like ArgoCD for controlled deployments and quick rollback in case of failures.

Overall, by combining rolling updates, health checks, and proper deployment strategies, we ensure zero downtime and high availability in production.

---

### 🧠 Simple Way to Remember

**4 Pillars:**
1. Rolling Updates (default in Kubernetes)
2. Health Checks (Readiness probe is critical)
3. Deployment Strategies (Blue-Green, Canary)
4. Rollback (quick recovery)

### 💥 Real Example

In our project, we used rolling updates with readiness probes to ensure new pods were ready before terminating old ones, which helped us achieve zero downtime during deployments.

### 🔥 Pro-Level Add-On

We also ensured backward compatibility of APIs and database changes to avoid breaking running traffic during deployments.

### 🎯 Follow-up Question

**Q: What can break zero downtime?**

- Missing readiness probe
- Breaking DB changes
- Sudden traffic switch
- Wrong deployment configuration

</details>

<details>
<summary><b>Can you explain Blue-Green deployment and how you implemented it?</b></summary>

<br>

Blue-Green deployment is a release strategy where we maintain two identical environments:

- **Blue** → current live (production) version  
- **Green** → new version to be deployed  

Instead of updating the existing environment, we deploy the new version to the Green environment and test it.

Once validated, we switch traffic from Blue to Green with minimal or zero downtime.

### 🧠 How I Implemented in My Project

In our Kubernetes setup, we implemented Blue-Green deployment using separate deployments and services.

- We created two versions of deployments: `app-blue` and `app-green`
- The Kubernetes Service was used to route traffic

**Flow:**

1. Existing version runs on **Blue**
2. Deploy new version on **Green**
3. Test Green environment (smoke testing / QA validation)
4. Update Service selector to point from Blue → Green
5. Monitor application
6. Keep Blue as backup for quick rollback

### 💥 Real Example

In one release, we deployed the new version as Green and performed validation.  
After successful testing, we switched the service traffic to Green.  
When a minor issue was detected, we quickly rolled back by pointing traffic back to Blue.

### 🎯 Easy Way to Remember

**4 Steps:**

1. Deploy → Green  
2. Test → Green  
3. Switch → Traffic  
4. Rollback → If needed  

</details>

<details>
<summary><b>Can you explain Canary deployment and how you implemented it in your project?</b></summary>

<br>

Canary deployment is a strategy where we release a new version of the application to a small subset of users first, instead of all users at once.

This helps us test the new version in production with real traffic while minimizing risk.

If everything works fine, we gradually increase traffic to the new version. If any issue occurs, we can quickly roll back without impacting all users.

### 🧠 How I Implemented in My Project

In our Kubernetes setup, we implemented Canary deployment using multiple deployments and controlled traffic routing.

- We had two versions:
  - Stable version (v1)
  - Canary version (v2)

**Flow:**

1. Deploy new version as **Canary (v2)** with fewer replicas  
2. Keep stable version (v1) handling most traffic  
3. Use Kubernetes Service or Ingress (NGINX) to split traffic  
4. Monitor metrics (errors, latency, CPU usage)  
5. Gradually increase traffic to v2  
6. If stable → promote v2 fully  
7. If issues → rollback to v1  

### 💥 Real Example

In our project, we deployed a new version to 10% of traffic using canary deployment.  
We monitored application logs and metrics using Prometheus and Grafana.  
Once everything was stable, we gradually increased traffic to 100%.

---

### 🔥 Pro-Level Add-On

We used automated monitoring alerts to detect failures early and stop canary rollout if error rates increased.

### 🎯 Easy Way to Remember

**4 Steps:**

1. Deploy → Small traffic  
2. Monitor → Metrics  
3. Increase → Gradually  
4. Rollback → If needed  

### 🎯 Follow-up Question

**Q: When to use Canary vs Blue-Green?**

- Canary → When you want gradual rollout and testing with real users  
- Blue-Green → When you want instant switch with full validation  

</details>

<details>
<summary><b>When do you use Rolling, Blue-Green, and Canary deployment?</b></summary>

<br>

### 🧠 Interview-Ready Answer

The choice of deployment strategy depends on risk, application criticality, and testing requirements.

- **Rolling Updates** → Used for regular deployments where the application is stateless and we want simple, zero-downtime updates.

- **Blue-Green Deployment** → Used when we need a full environment switch with quick rollback, especially for critical releases where we want to test the entire setup before going live.

- **Canary Deployment** → Used when we want to release features gradually, monitor real user behavior, and minimize risk by exposing only a small percentage of users initially.

**Summary:**  

Rolling → simplicity  
Blue-Green → safe full switch  
Canary → controlled gradual release  

---

### 🎯 Easy Way to Remember (Decision Logic)

🔵 **Rolling Update → Default**
- Normal deployments  
- Stateless apps  
- No major risk  

🟢 **Blue-Green → Full Switch + Quick Rollback**
- Critical applications  
- Need instant rollback  
- Full validation before release  

🟡 **Canary → Test with Real Users**
- New features  
- Risky changes  
- Gradual rollout  

### 💥 Real-Time Examples

- Bug fixes → Rolling update  
- Major release → Blue-Green  
- New features → Canary deployment  

</details>

<details>
<summary><b>Application is down in production – How will you troubleshoot?</b></summary>

<br>

# 🔥 Perfect Answer (Production-Level)

“If the application is down in production, I would approach it in a structured way.

First, I would try to understand the impact—whether it’s a complete outage or partial degradation, and check if any alerts were triggered in monitoring tools like Prometheus or Grafana.

Next, I would check the application layer by verifying pod status using `kubectl get pods` and inspect logs using `kubectl logs` to identify any runtime errors.

If pods are not running, I would check Kubernetes events and describe the pod using `kubectl describe pod` to see if there are issues like resource limits, image pull errors, or crash loops.

Then, I would verify the infrastructure layer by checking node status using `kubectl get nodes` and ensure the cluster is healthy.

I would also check the networking layer—like service endpoints, ingress configuration, or load balancer health—to ensure traffic is correctly routed.

If the issue is due to a recent deployment, I would quickly rollback to the previous stable version using ArgoCD or Kubernetes rollout undo.

Once the application is restored, I would perform root cause analysis using logs and monitoring data, and implement preventive measures like better alerts, resource tuning, or pipeline checks to avoid similar issues in future.”

---

### 🧠 How to Remember (Simple Framework)

👉 Always follow:

### 1. Impact

* Full down or partial?

### 2. Application Layer

* Pods  
* Logs  

### 3. Kubernetes Layer

* Events  
* Describe  

### 4. Infrastructure Layer

* Nodes  
* Cluster health  

### 5. Network Layer

* Service / Ingress / LB  

### 6. Immediate Fix

* Restart / Rollback  

### 7. Prevention

* Alerts / Monitoring / RCA  

# 🔥 Pro Upgrade Line (Add this at end)

> “My priority would always be to restore service quickly first, and then focus on root cause analysis.”

</details>

### Rollback Strategy (Kubernetes + ArgoCD + Helm)

<details>
<summary><b>How did you handle rollback in your project?</b></summary>

### 🧠 Interview-Ready Answer

In our project, we implemented rollback strategies at multiple levels to quickly recover from failures and ensure minimal downtime.

---

### 🔧 Kubernetes Level Rollback

Kubernetes automatically maintains previous ReplicaSets during rolling updates.

Rollback command:

```bash
kubectl rollout undo deployment <deployment-name>
```

Check rollout history:

```bash
kubectl rollout history deployment <deployment-name>
```

Rollback to a specific revision:

```bash
kubectl rollout undo deployment <deployment-name> --to-revision=<revision-number>
```

---

### 🚀 Helm Rollback

Helm maintains version history for each deployment (release revisions).

Check release history:

```bash
helm history <release-name>
```

Rollback to previous version:

```bash
helm rollback <release-name> <revision-number>
```

Verify status:

```bash
helm status <release-name>
```

---

### 🔄 ArgoCD Rollback (GitOps)

We followed GitOps, where Git is the source of truth.

#### Method 1: Git Revert (Preferred)

```bash
git revert <commit-id>
git push origin main
```

👉 ArgoCD automatically syncs and restores the previous stable state.


#### Method 2: ArgoCD CLI

Check application history:

```bash
argocd app history <app-name>
```

Rollback to previous revision:

```bash
argocd app rollback <app-name> <revision-id>
```

#### Method 3: ArgoCD UI

- Open ArgoCD Dashboard  
- Select application  
- Go to **History and Rollback**  
- Choose previous revision → Click **Rollback**

---

### 💥 Real Production Scenario

In one release, a new deployment caused high error rates.

- Detected via Prometheus alerts  
- Checked logs and identified issue  
- Performed Helm rollback  
- ArgoCD synced automatically  
- Service restored within minutes  

---

### 🔥 Pro-Level Add-On

We ensured backward compatibility for APIs and database changes to avoid issues during rollback.

### 🎯 Easy Way to Remember

**3 Levels of Rollback:**

1. Kubernetes → `kubectl rollout undo`  
2. Helm → `helm rollback`  
3. ArgoCD → `git revert` / `argocd rollback`  

👉 **“Undo → Helm → Git”**

---

### 🎯 Follow-up Question

**Q: Which rollback is fastest?**

- Helm rollback → fastest and controlled  
- ArgoCD Git revert → best for GitOps consistency  

</details>

### CI/CD - Jenkins 

<details>
<summary><b>Jenkins Pipeline Failed — How do you troubleshoot?</b></summary>

<br>

In case a Jenkins pipeline fails, I follow a structured troubleshooting approach to quickly identify and resolve the issue.

First, I check the Jenkins console output logs to identify at which stage the failure occurred—whether it is during code checkout, build, test, or deployment.

If the issue is during the build stage, I verify dependencies, build tools like Maven or npm, and check for any compilation errors.

If the failure is related to code quality or security stages, I review SonarQube quality gate results or Trivy scan reports to understand the reason.

If the issue occurs during Docker build or push, I check the Dockerfile, image tagging, and registry authentication.

For deployment failures, I verify Kubernetes configurations, such as manifests, Helm charts, and check pod status using commands like kubectl get pods and kubectl describe pod.

I also check if there are any environment variable or credential issues configured in Jenkins.

If needed, I try to reproduce the issue locally or re-run the failed stage to confirm if it is a transient issue.

Overall, I follow a step-by-step debugging approach to quickly identify the root cause and fix the pipeline.

---

🧠 Easy Way to Remember (Use this in mind)

👉 LOG → STAGE → TOOL → FIX

- Console output Logs check
- Stage identify - Build, Test, Docker Build
- Tool-specific issue
- Fix
- Re-run

Additionally, If the failed pipeline logs are not clear. I will check the previous success pipeline logs.

</details>
