# 🌐 Deploy Static Website on AWS

This project demonstrates how to deploy a static website to AWS using **Amazon S3**, **CloudFront**, and **IAM**. The website is built with HTML, CSS, Bootstrap, and other static assets and is served securely over the internet via a CDN.

---

## 📁 Project Structure

```
.
├── index.html         # Homepage of the website
├── /img               # Background images used in the site
├── /vendor            # Bootstrap, fonts, and JS libraries
└── /css               # Custom CSS styling
```

---

## 🚀 Deployment Architecture

- **S3** – Hosts the static website content
- **CloudFront** – Distributes content globally with low latency
- **IAM** – Manages user access and permissions
- **S3 Bucket Policy** – Configured for public read access (or CloudFront OAI for restricted access)

---

## 🔧 Deployment Steps

1. **Create S3 Bucket**
   - Enable static website hosting
   - Upload files: `index.html`, `/img`, `/vendor`, `/css`
   - Set `index.html` as the default root object

2. **Set Bucket Policy**
   - Allow public read access for static assets (or use OAI with CloudFront)

3. **Create CloudFront Distribution**
   - Point the origin to your S3 bucket
   - Set default root object as `index.html`
   - Enable HTTPS and configure caching

4. **Access the Website**
   - Once deployed, your website will be available via the CloudFront distribution domain name

---

## 🌍 Example Technologies Used

- **HTML5**
- **CSS3**
- **Bootstrap (via /vendor)**
- **AWS S3**
- **AWS CloudFront**
- **IAM**

---

## 📄 License

This project is licensed under the [LICENSE.txt](LICENSE.txt) file.
