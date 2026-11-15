# aws-eks-helm-autoscaling

WordPress on Amazon EKS, deployed with Helm and autoscaled with a Horizontal Pod Autoscaler (HPA).

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

![GitHub Repository Landing Page](docs/screenshots/01-github-repo.png)

---

## Phase 2: AWS Foundations
- Verified least-privilege admin IAM user configuration in `us-east-1`.
- Installed and configured AWS CLI v2 inside WSL2 Ubuntu.
- Deployed an active AWS Budget (`aws-eks-helm-autoscaling-budget`) set to $10/month with automated email alerts.
- Created dedicated project IAM user: `aws-eks-helm-autoscaling-admin` with administrative privileges for infrastructure provisioning.
- Generated programmatic access keys for `aws-eks-helm-autoscaling-admin` with a descriptive project tag for WSL2 CLI usage.
- Installed AWS CLI v2 inside WSL2 Ubuntu and configured authentication using `aws-eks-helm-autoscaling-admin`.
- Deployed an active AWS Budget (`aws-eks-helm-autoscaling-budget`) set to $10/month with an 80% email alert threshold.

### Phase 2 Documentation

**Dedicated IAM User Created:**
![IAM User Created](docs/screenshots/02-iam-user-created.png)

**Access Key Configured:**
![Access Key Created](docs/screenshots/02-access-key-created.png)

**AWS CLI Authentication Verified:**
![AWS CLI Configured](docs/screenshots/02-aws-cli-configured.png)

**AWS Budget Active ($10/mo):**
![AWS Budget Created](docs/screenshots/02-aws-budget-created.png)