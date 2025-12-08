---
title: "Week 11 Worklog"
date: 2025-11-17
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Optimize frontend performance when interacting with AWS-based backend systems.  
* Apply advanced caching strategies (client-side + API Gateway caching).  
* Improve application responsiveness under high-latency and throttling conditions.  
* Study frontend build optimization: bundling, tree-shaking, code splitting.  
* Implement security best practices for cloud-hosted frontend applications.  

---

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
|-----|------|-------------|------------------|--------------------|
| 2 | - Study browser caching, ETags, and Cache-Control.<br>- Implement SWR/react-query for smarter data fetching.<br>- Apply client-side caching strategies.<br><br>→ Improve data freshness and reduce API overhead. | 17/11/2025 | 17/11/2025 | React Query Docs |
| 3 | - Analyze Lighthouse performance metrics.<br>- Fix render-blocking issues.<br>- Optimize images with compression & lazy loading.<br><br>→ Achieve better performance scores. | 18/11/2025 | 18/11/2025 | Google Web.Dev |
| 4 | - Configure API Gateway caching.<br>- Compare cold vs warm Lambda impact on UI.<br>- Implement UI fallback strategy for Lambda cold starts.<br><br>→ Build cloud-resilient UI behaviour. | 19/11/2025 | 19/11/2025 | AWS API Gateway Docs |
| 5 | - Apply bundling optimizations: tree shaking, code splitting, dynamic imports.<br>- Reduce bundle size and improve initial load time.<br><br>→ Enhance frontend performance in production. | 20/11/2025 | 20/11/2025 | Vite/Webpack Docs |
| 6 | - Review security: XSS, CSRF, token storage, HTTPS enforcement.<br>- Apply AWS Cognito best practices for authentication.<br>- Secure environment variables in Amplify builds.<br><br>→ Harden cloud frontend security posture. | 21/11/2025 | 21/11/2025 | AWS Cognito Docs |

---

### Week 11 Achievements

#### 1. Stronger Caching & Data Fetching Strategy
- Implemented SWR/react-query for smart cache management.  
- Reduced unnecessary API calls by ~40% thanks to request deduplication.  

#### 2. Improved Application Performance
- Achieved higher Lighthouse scores by addressing render-blocking assets.  
- Applied lazy loading and image compression to optimize UI loading experience.

#### 3. Cloud-Aware UI Behaviour  
- Enabled API Gateway caching to reduce UI latency.  
- Added UI fallback for Lambda cold starts (temporary skeleton, retry hints).  

#### 4. Build Optimization for Production
- Reduced bundle size using dynamic imports and tree shaking.  
- Enhanced first-paint speed, improving user perception of responsiveness.

#### 5. Strengthened Frontend Security
- Addressed XSS/CSRF risks through sanitizing and proper token handling.  
- Secured Amplify environment variables and enforced HTTPS-only behaviour.
