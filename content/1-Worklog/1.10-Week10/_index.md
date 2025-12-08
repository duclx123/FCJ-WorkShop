---
title: "Week 10 Worklog"
date: 2025-11-10
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Learn how frontend interacts with **real serverless workflows** (Lambda → DynamoDB → API Gateway).  
* Implement advanced data handling (pagination, filtering, optimistic UI).  
* Understand Amplify Hosting pipelines and CI/CD for frontend deployment.  
* Improve app reliability with logging, error boundaries, and retry logic.  
* Strengthen cloud-ready UI architecture for production projects.

---

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
|-----|------|-------------|------------------|--------------------|
| 2 | - Explore Fetch + Axios advanced configurations.<br>- Implement request interceptors (auth, retry).<br>- Evaluate API performance and caching options.<br><br>→ Build robust API communication. | 10/11/2025 | 10/11/2025 | Axios Docs |
| 3 | - Build CRUD UI for AWS backend data.<br>- Connect UI actions with API Gateway + Lambda + DynamoDB.<br>- Add pagination & filtering in the UI.<br><br>→ Achieve full data integration. | 11/11/2025 | 11/11/2025 | AWS Study Group |
| 4 | - Study Amplify’s hosting pipeline (build, deploy, preview).<br>- Configure automatic build previews for feature branches.<br>- Push multiple versions (dev/staging/prod).<br><br>→ Understand cloud deployment lifecycle. | 12/11/2025 | 12/11/2025 | Amplify Hosting Docs |
| 5 | - Add UI error boundaries for React.<br>- Implement retry logic for failed API calls.<br>- Track errors via CloudWatch logs (Lambda side) to adjust frontend logic.<br><br>→ Increase fault tolerance. | 13/11/2025 | 13/11/2025 | React Docs |
| 6 | - Stress test UI with fake delays, failures, and API throttling simulations.<br>- Improve UX with skeleton loading, optimistic UI, and graceful fallback states.<br><br>→ Prepare UI for real-world cloud behaviour. | 14/11/2025 | 14/11/2025 | Cloud Design Patterns |

---

### Week 10 Achievements

#### 1. Strengthened API Communication Strategy
- Configured Axios interceptors to handle auth and auto-retry.  
- Improved request consistency and reduced API failure rates.

#### 2. Full CRUD Frontend on AWS Backend
- Built UI that interacts fully with API Gateway + Lambda + DynamoDB.  
- Implemented pagination & filtering that sync correctly with backend limitations.

#### 3. Mastered Amplify Hosting Workflow
- Understood CI/CD pipeline for frontend deployment.  
- Used Amplify preview builds to validate features before release.

#### 4. Enhanced Reliability and Error Handling
- Implemented global React error boundaries.  
- Added retry and fallback patterns for unstable APIs.  
- Used CloudWatch logs to adjust error responses in frontend.

#### 5. Real-World UX Improvements
- Simulated real latency and throttling to refine UI performance.  
- Added loading skeletons and optimistic UI for smoother user experience.