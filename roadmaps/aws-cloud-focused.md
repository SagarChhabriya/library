# AWS Learning Roadmap (With Hands-On Labs)


## 1. IAM – Identity and Access Management

Service: AWS Identity and Access Management (IAM)

| Topic                   | Concepts to Learn              | Hands-On Exercises                   | Outcome                           |
| ----------------------- | ------------------------------ | ------------------------------------ | --------------------------------- |
| IAM Basics              | Users, Groups, Roles, Policies | Create IAM users and groups          | Understand access management      |
| Security Best Practices | MFA, Root account protection   | Enable MFA on root and IAM user      | Secure AWS account                |
| Policies                | AWS managed vs custom policies | Create custom least-privilege policy | Fine-grained permissions          |
| IAM Roles               | Role assumption, service roles | Attach role to EC2                   | Service-to-service authentication |
| Cross-Account Access    | Trust relationships            | Create cross-account role            | Multi-account access              |

---

## 2. VPC – Networking Foundation

Service: Amazon Virtual Private Cloud (VPC)

| Topic                | Concepts to Learn    | Hands-On Exercises                | Outcome                |
| -------------------- | -------------------- | --------------------------------- | ---------------------- |
| VPC Basics           | CIDR blocks, subnets | Create custom VPC                 | Networking foundation  |
| Subnets              | Public vs private    | Create public and private subnets | Network segmentation   |
| Routing              | Route tables         | Configure route tables            | Traffic control        |
| Internet Access      | Internet Gateway     | Attach IGW and test connectivity  | Public internet access |
| Private Connectivity | NAT Gateway          | Configure NAT for private subnet  | Secure outbound access |

---

## 3. EC2 – Compute Services

Service: Amazon EC2

| Topic           | Concepts to Learn      | Hands-On Exercises            | Outcome                |
| --------------- | ---------------------- | ----------------------------- | ---------------------- |
| EC2 Basics      | AMI, instance types    | Launch EC2 instance           | Virtual server setup   |
| Security Groups | Inbound/outbound rules | Configure SSH and HTTP access | Secure instance access |
| Remote Access   | SSH connection         | Connect to EC2 via SSH        | Server management      |
| Web Hosting     | Install Apache/Nginx   | Deploy simple HTML site       | Run web server         |
| AMI & Scaling   | Create AMI             | Create custom image           | Instance backup        |

---

## 4. S3 – Object Storage

Service: Amazon S3

| Topic          | Concepts to Learn      | Hands-On Exercises                 | Outcome              |
| -------------- | ---------------------- | ---------------------------------- | -------------------- |
| Buckets        | Object storage model   | Create S3 bucket                   | Storage fundamentals |
| Versioning     | Object version control | Enable versioning and restore file | Data recovery        |
| Static Hosting | Website hosting        | Host static website                | Deploy frontend      |
| Security       | Bucket policies        | Configure public/private access    | Secure storage       |
| Lifecycle      | Storage classes        | Create lifecycle rule to Glacier   | Cost optimization    |

---

## 5. Databases – RDS and DynamoDB

Services: Amazon RDS and Amazon DynamoDB

| Topic           | Concepts to Learn     | Hands-On Exercises             | Outcome                |
| --------------- | --------------------- | ------------------------------ | ---------------------- |
| RDS Setup       | Managed relational DB | Launch MySQL/Postgres instance | Managed database       |
| Connectivity    | Security group rules  | Connect EC2 to RDS             | App–DB communication   |
| Backup          | Snapshots             | Create and restore snapshot    | Disaster recovery      |
| DynamoDB Basics | NoSQL concepts        | Create DynamoDB table          | NoSQL fundamentals     |
| Scaling         | Read/write capacity   | Test scaling behavior          | Performance management |

---

## 6. Load Balancing and Auto Scaling

Services: Elastic Load Balancing and EC2 Auto Scaling

| Topic          | Concepts to Learn | Hands-On Exercises               | Outcome                |
| -------------- | ----------------- | -------------------------------- | ---------------------- |
| ALB Basics     | Target groups     | Create Application Load Balancer | Traffic distribution   |
| Health Checks  | Instance health   | Configure health checks          | High availability      |
| Auto Scaling   | Scaling policies  | Create Auto Scaling Group        | Dynamic scaling        |
| Stress Testing | CPU thresholds    | Trigger scaling event            | Resilient architecture |

---

## 7. Route 53 – DNS Management

Service: Amazon Route 53

| Topic            | Concepts to Learn | Hands-On Exercises    | Outcome                 |
| ---------------- | ----------------- | --------------------- | ----------------------- |
| Hosted Zones     | Public DNS        | Create hosted zone    | Domain management       |
| DNS Records      | A, CNAME, Alias   | Map domain to ALB     | Public access           |
| Routing Policies | Simple, weighted  | Test routing policies | Traffic routing control |

---

## 8. CloudFront – Content Delivery

Service: Amazon CloudFront

| Topic        | Concepts to Learn | Hands-On Exercises             | Outcome                 |
| ------------ | ----------------- | ------------------------------ | ----------------------- |
| CDN Basics   | Edge locations    | Create CloudFront distribution | Global performance      |
| Origin Setup | S3/ALB origin     | Connect S3 to CloudFront       | Optimized delivery      |
| HTTPS        | SSL certificates  | Enable HTTPS                   | Secure content delivery |

---

## 9. Lambda – Serverless Compute

Service: AWS Lambda

| Topic           | Concepts to Learn  | Hands-On Exercises           | Outcome              |
| --------------- | ------------------ | ---------------------------- | -------------------- |
| Lambda Basics   | Event-driven model | Create simple function       | Serverless execution |
| Triggers        | S3, API Gateway    | Trigger Lambda via S3 upload | Automation           |
| API Integration | REST APIs          | Deploy API with Lambda       | Serverless backend   |
| Monitoring      | Logs               | View logs in CloudWatch      | Observability        |

---

## 10. ECS – Containers

Service: Amazon Elastic Container Service (ECS)

| Topic            | Concepts to Learn     | Hands-On Exercises      | Outcome                 |
| ---------------- | --------------------- | ----------------------- | ----------------------- |
| Container Basics | Docker concepts       | Build Docker image      | Containerization        |
| ECR              | Image registry        | Push image to ECR       | Image management        |
| ECS Deployment   | Task definitions      | Deploy container on ECS | Container orchestration |
| Fargate          | Serverless containers | Deploy on Fargate       | Managed containers      |

---

## 11. Monitoring and Auditing

Services: CloudWatch and CloudTrail

| Topic           | Concepts to Learn | Hands-On Exercises      | Outcome              |
| --------------- | ----------------- | ----------------------- | -------------------- |
| Metrics         | CPU, network      | Monitor EC2 metrics     | Resource visibility  |
| Alarms          | Threshold alerts  | Create CloudWatch alarm | Proactive monitoring |
| SNS Alerts      | Notifications     | Send email alerts       | Incident awareness   |
| CloudTrail Logs | API tracking      | View activity history   | Audit capability     |

---

## 12. Infrastructure as Code

Service: AWS CloudFormation

| Topic            | Concepts to Learn     | Hands-On Exercises         | Outcome             |
| ---------------- | --------------------- | -------------------------- | ------------------- |
| Templates        | YAML/JSON structure   | Write basic EC2 template   | IaC fundamentals    |
| Stack Deployment | Resource provisioning | Deploy stack               | Automated infra     |
| Parameters       | Dynamic configuration | Add parameters to template | Flexible deployment |
| Updates          | Stack modifications   | Update stack safely        | Change management   |

---

## 13. AI Services (Advanced)

Services: Amazon SageMaker and Amazon Bedrock

| Topic            | Concepts to Learn | Hands-On Exercises    | Outcome             |
| ---------------- | ----------------- | --------------------- | ------------------- |
| SageMaker Basics | ML workflow       | Train simple model    | Managed ML          |
| Model Deployment | Endpoints         | Deploy model endpoint | Production ML       |
| Bedrock          | Foundation models | Invoke model via API  | Generative AI usage |

---

# Final Capstone Project

| Component  | Implementation Task             | Goal                   |
| ---------- | ------------------------------- | ---------------------- |
| Networking | VPC with public/private subnets | Secure architecture    |
| Compute    | EC2 in private subnet           | Application layer      |
| Database   | RDS in private subnet           | Data layer             |
| Scaling    | ALB + Auto Scaling              | High availability      |
| DNS        | Route 53 domain mapping         | Public access          |
| CDN        | CloudFront in front of ALB      | Global performance     |
| Automation | CloudFormation template         | Infrastructure as Code |

---

