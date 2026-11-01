# Task 32: Static Website Deployment on AWS S3 and CloudFront

## Project Overview

This project demonstrates the deployment of a responsive static portfolio website using Amazon Web Services (AWS).

The website is hosted in Amazon S3 and delivered globally through Amazon CloudFront with HTTPS support and CDN caching.

## Live Website

**Live URL:** https://d2tdlpp3n6uukx.cloudfront.net

## AWS Architecture

```text
             GitHub Repository
             (HTML, CSS, JS)
                    |
                    | Manual upload
                    v
              Amazon S3
           (Private Bucket)
                    |
                    | Origin Access Control
                    v
             Amazon CloudFront
              (CDN + HTTPS)
                    |
                    v
             Live Portfolio
```

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Git and GitHub
- Amazon S3
- Amazon CloudFront
- HTTPS

## AWS Configuration

### Amazon S3
- Bucket name: `veda-task32-pooja-portfolio`
- Region: Asia Pacific (Mumbai) – `ap-south-1`
- Bucket type: General Purpose
- Object ownership: Bucket owner enforced
- Block all public access: Enabled
- Server-side encryption: SSE-S3
- Uploaded files: `index.html`, `style.css`, `script.js`

### Amazon CloudFront
- Distribution name: `veda-task32-portfolio-cdn`
- Distribution ID: `E2V2QHCOJOM0ZX`
- Origin: Amazon S3
- Origin access: CloudFront private bucket access (OAC)
- Default root object: `index.html`
- Cache configuration: Recommended S3 cache settings
- HTTPS: Enabled through the CloudFront domain
- AWS WAF: Not enabled

## Website Features

- Responsive portfolio design
- Home section
- About section
- Technical skills section
- Featured projects
- Contact section
- Mobile navigation menu
- JavaScript-powered interactions

## Deployment Steps

1. Created an Amazon S3 bucket.
2. Configured private bucket access and security settings.
3. Uploaded the website files to S3.
4. Created a CloudFront distribution.
5. Connected the private S3 bucket using CloudFront access.
6. Configured `index.html` as the default root object.
7. Enabled HTTPS delivery through CloudFront.
8. Tested the website on desktop and mobile viewports.

## Testing and Validation

- Verified successful S3 file uploads.
- Verified CloudFront distribution creation.
- Opened the live website using HTTPS.
- Tested website navigation.
- Checked JavaScript execution using browser developer tools.
- Verified responsive layout using Chrome device emulation.
- Tested mobile hamburger navigation.

## Custom Domain

The website currently uses the default CloudFront domain. A separately owned custom domain and DNS configuration were not added because no domain was purchased for this task.

## Screenshots

Deployment screenshots are available in the `screenshorts` folder of this repository.

## Learning Outcomes

- Learned static website hosting using Amazon S3.
- Configured secure private S3 bucket access.
- Learned CloudFront CDN distribution setup.
- Configured HTTPS delivery.
- Understood origin access control.
- Tested responsive website deployment.
- Practised AWS cloud hosting and deployment documentation.




