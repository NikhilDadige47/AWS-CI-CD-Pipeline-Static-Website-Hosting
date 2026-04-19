**Project Title**  
AWS-CI-CD-Pipeline-Static-Website-Hosting

**Author**  
Nikhil Dadige  
[Your LinkedIn / Portfolio Link]

**Date**  
April 2026

**Live Demo**  
[http://nikhil-static-site-prod.s3-website-us-east-1.amazonaws.com/#contact]([http://nikhil-static-site-prod.s3-website-us-east-1.amazonaws.com/#contact))

**GitHub Repository**  
[https://github.com/NikhilDadige47/AWS-CI-CD-Pipeline-Static-Website-Hosting]([https://github.com/yourusername/your-repo-name](https://github.com/NikhilDadige47/AWS-CI-CD-Pipeline-Static-Website-Hosting))

---

## Executive Summary

I designed, built, and deployed a fully automated static website on Amazon Web Services (AWS) that updates automatically every time code is pushed to GitHub. The entire solution uses only the AWS Management Console (no CLI, no Terraform, no paid third-party tools).  

The system delivers production-grade continuous deployment with high security, low cost, and instant updates — completing the full deployment cycle in under 60 seconds.

This project demonstrates real-world cloud engineering skills, DevOps automation, secure infrastructure design, and cost-optimized architecture.

---

## Project Objectives

- Build a live static website hosted on AWS S3 with public access
- Implement fully automated deployment triggered by GitHub pushes
- Ensure zero-downtime updates and easy rollback capability
- Maintain strict least-privilege security and best practices
- Keep operational cost at $0 during AWS Free Tier (~$1.01/month afterward)
- Create a clean, reliable, and maintainable cloud solution

---

## System Architecture

The architecture follows a simple yet robust CI/CD pipeline pattern using native AWS services.

### High-Level Architecture Diagram

<img width="2816" height="1536" alt="Gemini_Generated_Image_mtpvdomtpvdomtpv" src="https://github.com/user-attachments/assets/a359a2bd-7169-4a7a-9666-9bc0b93b59d3" />



**Key Technical Decisions:**
- **AWS CodePipeline** chosen for native AWS integration and full visibility
- **S3 Static Website Hosting** selected for simplicity and lowest possible cost
- **CodeStar Connections** used for secure GitHub integration (no personal access tokens)
- **Custom least-privilege IAM role** created to follow security best practices
- **Bucket versioning + lifecycle rules** added for reliability and automatic cleanup

---

## What Was Implemented

The following production-ready components were successfully built and configured:

### Core Components
- **Public S3 Website Bucket** – Static website hosting enabled with `index.html` as index and error document
- **Private S3 Artifact Bucket** – Used by CodePipeline for temporary storage with automatic daily expiration
- **AWS CodePipeline** – End-to-end automation pipeline (Source stage + Deploy stage only)
- **Secure GitHub Connection** – Via AWS CodeStar Connections with webhook-based triggers
- **Least-Privilege IAM Role** – Custom inline policy granting only required permissions to S3 buckets and CodeStar
- **Bucket Policies & Security** – Public read access limited strictly to `GetObject` action
- **Versioning & Lifecycle Rules** – Enabled on website bucket for safe rollbacks and cost control on artifact bucket

### Automation Flow
1. Developer pushes code to GitHub `main` branch
2. CodePipeline is instantly triggered via webhook
3. Source code is pulled and stored temporarily in private artifact bucket
4. Files are automatically extracted and deployed to the public website bucket
5. Live website updates within 60 seconds with zero manual steps

---

## Technologies & Tools Used

| Category              | Technology                          | Purpose                              |
|-----------------------|-------------------------------------|--------------------------------------|
| Hosting               | Amazon S3 Static Website Hosting    | Serve static content                 |
| CI/CD                 | AWS CodePipeline (V2)               | Automated deployment pipeline        |
| Source Control        | GitHub + AWS CodeStar Connections   | Secure repository integration        |
| Security              | AWS IAM (Least-Privilege Role)      | Fine-grained access control          |
| Storage               | Amazon S3 (2 buckets)               | Website + Artifact storage           |
| Reliability           | S3 Versioning & Lifecycle Rules     | Rollback & cost optimization         |

---

## Key Features & Results

- ✅ **Instant Auto-Deployment** – Updates live in < 60 seconds after every `git push`
- ✅ **Zero Downtime** – New versions replace old ones atomically
- ✅ **Production Security** – Least-privilege IAM + strict bucket policies
- ✅ **Rollback Capability** – Full versioning allows instant restoration of previous versions
- ✅ **Cost Optimized** – $0 during Free Tier, ~$1.01/month afterward
- ✅ **Console-Only Solution** – No CLI or additional tools required
- ✅ **Fully Functional** – Ready for real-world use with a single HTML file (easily extendable to React, Vue, etc.)

---

## Challenges Overcome

- Designed secure GitHub-to-AWS connection without exposing credentials
- Created minimal IAM permissions while ensuring pipeline functionality
- Configured correct S3 behavior for static website hosting and ZIP extraction
- Balanced public access for the website with strict security controls

---

## Conclusion & Future Enhancements

This project successfully delivers a complete, automated, and production-ready static website infrastructure on AWS. It showcases strong understanding of cloud services, CI/CD pipelines, security principles, and cost management.

**Possible Future Enhancements:**
- Add custom domain name with Amazon Route 53 + SSL
- Integrate CloudFront CDN for faster global delivery
- Add monitoring with CloudWatch alarms
- Extend to support modern frameworks (React, Next.js, etc.)

This solution serves as an excellent foundation for any static or JAMstack application and demonstrates professional-level cloud deployment skills.

---

**Project Status:** Completed & Live  
**Deployment Time:** Under 60 seconds per change  
**Maintenance Effort:** Minimal (only `git push`)

---

*Built as a portfolio project to showcase practical AWS cloud engineering and DevOps automation expertise.*
```
