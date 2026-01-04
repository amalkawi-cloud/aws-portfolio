# AWS Project: Serverless Static Website (S3 + CloudFront CDN)

## 🎯 Goal
To deploy a fast, globally-distributed website without managing any servers (serverless infrastructure), minimizing costs and improving performance.

## 🛠️ AWS Services Demonstrated
* **S3 (Simple Storage Service):** Used as the **Origin** (primary storage and web server hosting).
* **CloudFront (CDN):** Used as the **Delivery Network** to cache content globally and enforce HTTPS encryption.

## ⚙️ Key Configuration Details
* **Hosting Type:** Serverless Static Website Hosting.
* **Security:** Viewer Protocol Policy set to **Redirect HTTP to HTTPS** for all public traffic encryption.
* **Performance:** Content is served from the closest **Edge Location** to the user, ensuring low latency (fast loading times).
* **Origin Type:** The CloudFront distribution was configured to point to the **S3 Website Endpoint** as the Origin.

## 🔗 Live Demo
* **Fast CloudFront URL:** [diivtue9whwoc.cloudfront.net]
* **S3 Website Endpoint (Origin):** [http://abdullah-cloudfront-site.s3-website-us-east-1.amazonaws.com]

## 💡 Lessons Learned
This project successfully decoupled storage from delivery, demonstrating a modern, highly scalable, and highly available web hosting architecture. It confirms understanding of basic CDN concepts, caching, and mandatory HTTPS security practices.
