# aws-eks-helm-autoscaling

WordPress on Amazon EKS, deployed with Helm and autoscaled with a Horizontal Pod Autoscaler (HPA).

> **Simple version.** This project is the lean, cost-optimized build. For the production-grade version of the same app (Terraform, Multi-AZ RDS, EFS, CloudFront + WAF, Redis, CI/CD with OIDC), see [aws-eks-wordpress-enterprise](https://github.com/WJDVS/aws-eks-wordpress-enterprise).

**Tools:** eksctl · kubectl · Helm · AWS (EKS, EC2, ELB, EBS, ACM) · GitHub

## Architecture

![Project Architecture](docs/screenshots/architecture.png)

*Note: Solid borders represent the core build, while dashed borders represent planned Phase 2 upgrades.*

## Project Phases
1. VS Code, Git & GitHub
2. AWS Foundations
3. Kubernetes Concepts and Tools
4. Amazon EKS Cluster
5. WordPress with Helm
6. Autoscaling
7. Load Testing
8. Auth-Key Secret & EBS
9. HTTPS via ALB
10. Documentation, Polish & Comparison

> 🚧 In progress

---

## Phase 1: Environment Setup & Version Control
- Configured WSL2 Ubuntu development environment on Windows 11.
- Initialized Git version control with strict `.gitignore` security filters.
- Established a standardized project directory structure (`eksctl/`, `helm/`, `k8s/`, `scripts/`, `docs/`).
- Captured project folder structure and GitHub repository landing page documentation.

### Phase 1 Documentation

**Project Folder Structure (VS Code):**

![Project Structure](docs/screenshots/01-project-structure.png)

**GitHub Repository Landing Page:**

![GitHub Repository Landing Page](docs/screenshots/01-github-repo.png)

---

## Phase 2: AWS Foundations
- Created dedicated project IAM user `aws-eks-helm-autoscaling-admin` in `us-east-1` with administrative privileges for infrastructure provisioning, avoiding root account usage.
- Generated programmatic access keys for `aws-eks-helm-autoscaling-admin` tagged for WSL2 CLI usage.
- Installed AWS CLI v2 inside WSL2 Ubuntu and verified authentication via `aws sts get-caller-identity`.
- Deployed an active AWS Budget (`aws-eks-helm-autoscaling-budget`) set to $10/month with an 80% email alert threshold.
  - The budget is a spending guardrail, not the project's running cost. The EKS control plane alone is about $0.10/hour (roughly $73 for a full month), so the alert is there to catch resources left running.

### Phase 2 Documentation

**1. Dedicated IAM User Created:**

![IAM User Created](docs/screenshots/02-iam-user-created.png)

**2. Access Key Configured:**

![Access Key Created](docs/screenshots/02-access-key-created.png)

**3. AWS CLI Authentication Verified:**

![AWS CLI Configured](docs/screenshots/02-aws-cli-configured.png)

**4. AWS Budget Active ($10/mo spend guardrail):**

![AWS Budget Created](docs/screenshots/02-aws-budget-created.png)
