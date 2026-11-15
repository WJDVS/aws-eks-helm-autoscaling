# aws-eks-helm-autoscaling

WordPress on Amazon EKS, deployed with Helm and autoscaled with a Horizontal Pod Autoscaler (HPA).

**Tools:** eksctl · kubectl · Helm · AWS (EKS, EC2, ELB, EBS, ACM) · GitHub

## Project Phases
1. VS Code, Git & GitHub
​2. AWS Foundations
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

## Phase 2: AWS Foundations
- Verified least-privilege admin IAM user configuration in `us-east-1`.
- Installed and configured AWS CLI v2 inside WSL2 Ubuntu.
- Deployed an active AWS Budget (`aws-eks-helm-autoscaling-budget`) set to $10/month with automated email alerts.