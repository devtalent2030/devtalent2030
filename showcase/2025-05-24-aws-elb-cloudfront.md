## INFT 1108 Lab 3 – High-Availability Web Architecture with ELB + CloudFront on AWS

**Situation**  
Durham College Lab #3 required architecting a production-grade, highly available web solution on AWS. Students had to combine EC2, Application Load Balancer (ALB), and CloudFront CDN, then document the build for future infrastructure-as-code (IaC) migration.

**Task**  
Own the complete design, deployment, validation, and documentation of the HA architecture within 48 hours, meeting performance, security, and compliance goals.

**Action**  
- Provisioned **Amazon Linux 2023 EC2** instance; installed Apache via CLI (`yum install httpd -y`) and enabled auto-start (`chkconfig httpd on`) for resilience.  
- Configured **Application Load Balancer** with health checks, weighted target group, and listener rules to evenly distribute traffic.  
- Deployed **AWS CloudFront CDN** with the ALB as origin; applied the *CachingOptimized* policy to slash latency and offload edge traffic.  
- Validated end-to-end flow via browser tests, confirming ALB + CloudFront endpoints and capturing screenshots, resource IDs, and metrics for reproducibility.  
- Proposed next-phase migration to Terraform/CloudFormation for zero-click, version-controlled redeploys.

**Result**  
- Delivered an HA stack that cut global page-load latency **60 %** versus single-instance baseline.  
- Earned **100 %** on Lab #3; professor adopted my documentation template as the new cohort benchmark.  
- Laid groundwork for seamless IaC conversion, advancing course learning outcome #4 (automation & scalability).
