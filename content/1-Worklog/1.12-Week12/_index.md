---
title: "Week 12 Worklog"
date: 2025-11-24
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Learn automated deployment workflows for frontend apps on AWS Amplify and S3 + CloudFront.  
* Configure CI/CD pipelines for stable and reproducible deployments.  
* Implement environment-based configurations (dev, staging, prod) for frontend.  
* Improve reliability through monitoring, rollback strategies, and version management.  
* Finalize frontend integration with AWS backend services for production readiness.  

---

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
|-----|------|-------------|------------------|--------------------|
| 2 | - Study how AWS Amplify Hosting works.<br>- Configure project to use multiple environments (dev/staging/prod).<br>- Set up proper environment variables.<br><br>→ Establish consistent deployment environments. | 24/11/2025 | 24/11/2025 | AWS Amplify Hosting Docs |
| 3 | - Create CI/CD pipeline using Amplify or GitHub Actions.<br>- Automate build, test, and deploy steps.<br>- Add branch-based deployment rules.<br><br>→ Ensure automated and repeatable deployment workflows. | 25/11/2025 | 25/11/2025 | GitHub Actions Docs |
| 4 | - Deploy frontend to S3 + CloudFront as an alternative architecture.<br>- Configure invalidation strategies and caching behavior.<br>- Set custom error pages and redirect rules.<br><br>→ Understand multi-option hosting strategies. | 26/11/2025 | 26/11/2025 | AWS CloudFront Docs |
| 5 | - Implement monitoring for production build using CloudWatch and Amplify logs.<br>- Analyze errors, build issues, and performance charts.<br>- Apply fixes to eliminate deployment instability.<br><br>→ Strengthen production monitoring capability. | 27/11/2025 | 27/11/2025 | AWS CloudWatch Docs |
| 6 | - Review full workflow: frontend → API Gateway → Lambda → DynamoDB.<br>- Conduct integration tests for all environments.<br>- Document deployment procedure and rollback plan.<br><br>→ Achieve production-readiness and operational stability. | 28/11/2025 | 28/11/2025 | Internal Project Docs |

---

### Week 12 Achievements

#### 1. Multi-Environment Frontend Setup  
- Successfully configured dev/staging/prod environments on Amplify.  
- Standardized environment variables for secure builds.

#### 2. Automated CI/CD Pipeline  
- Implemented automated deploy pipeline using GitHub Actions + Amplify.  
- Enabled branch-based deployment (e.g., dev → dev environment, main → production).  
- Reduced manual deployment errors significantly.

#### 3. Advanced Hosting Architecture  
- Deployed alternative version using S3 + CloudFront to compare latency and scalability.  
- Configured caching, invalidations, and custom redirects based on user flows.

#### 4. Monitoring & Reliability Improvements  
- Enabled CloudWatch logs for deployment and runtime monitoring.  
- Identified build bottlenecks and optimized build scripts.  
- Improved overall stability of the frontend deployment pipeline.

#### 5. Full Integration Validation  
- Validated end-to-end flow across AWS services (API Gateway, Lambda, DynamoDB).  
- Documented testing, deployment, and rollback procedures for future team use.  
