# Cloud & Infrastructure Skill

AWS, GCP, Azure expertise with DevOps and IaC.

## Multi-Cloud Architecture

### AWS
**Core Services:**
- Compute: EC2, Lambda, ECS, EKS
- Storage: S3, EBS, EFS, S3 Glacier
- Database: RDS, DynamoDB, Aurora
- Networking: VPC, CloudFront, Route 53
- Security: IAM, KMS, GuardDuty, WAF

**Well-Architected Framework:**
1. Operational Excellence
2. Security
3. Reliability
4. Performance Efficiency
5. Cost Optimization
6. Sustainability

### GCP
- Compute: Compute Engine, Cloud Run, GKE
- Storage: Cloud Storage, Persistent Disk
- Big Data: BigQuery, Dataflow
- ML: Vertex AI, AutoML

### Azure
- Compute: VMs, App Service, AKS
- Storage: Blob, Files, Queues
- AI: OpenAI Service, Cognitive Services

## Infrastructure as Code

### Terraform
```hcl
# AWS EC2
resource "aws_instance" "web" {
  ami           = "ami-12345678"
  instance_type = "t3.micro"

  tags = {
    Name = "WebServer"
  }
}
```

### Ansible
```yaml
- name: Configure web server
  hosts: webservers
  tasks:
    - name: Install nginx
      apt:
        name: nginx
        state: present
```

### Pulumi
```python
import pulumi
from pulumi_aws import s3

bucket = s3.Bucket("my-bucket")
```

## Kubernetes

### Core Concepts
- Pods: Smallest deployable unit
- Services: Network abstraction
- Deployments: Declarative updates
- ConfigMaps/Secrets: Configuration
- Ingress: External access

### Commands
```bash
kubectl get pods
kubectl apply -f deployment.yaml
kubectl logs -f pod-name
kubectl port-forward svc/service 8080:80
```

### Patterns
- Sidecar: Additional container in pod
- Ambassador: Proxy for service
- Adapter: Standardize output

## CI/CD

### GitHub Actions
```yaml
name: Deploy
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: make build
      - run: make deploy
```

### Best Practices
- Immutable infrastructure
- GitOps (ArgoCD, Flux)
- Shift-left testing
- Automated rollback

## Commands

- `/deploy` - Deployment automation
- `/infrastructure` - IaC generation
- `/monitor` - Monitoring setup
- `/cost` - Cost analysis
- `/scale` - Scaling strategies

## Multi-Agent Cloud

```
Kimi: Architecture decisions, cost optimization
GLG5: Deep infrastructure design, security
MiniMax: Quick service selection, pattern matching
```
