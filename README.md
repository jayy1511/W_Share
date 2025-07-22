# 🔐 W_Share - Secure File Sharing Platform

**W_Share** is a secure file-sharing web application that enables users to encrypt files in the browser, share them via one-time links, and ensure end-to-end security with advanced access controls and admin analytics.

---

## 🧩 Features

### ✅ Authentication
- User registration & login
- OTP verification for added security
- Secure password hashing and protection against brute-force attacks

### 🔐 File Upload Flow
- Client-side file encryption (AES)
- AES key encryption with RSA
- File + metadata securely uploaded to backend
- Encrypted files stored in S3 or equivalent object storage
- Metadata stored in a secure database

### 📥 Download Flow
- One-time access links
- Backend token validation
- Expiry and download limit check
- Decryption in-browser after secure download
- Auto-invalidation of used links
- Logs timestamp and IP of download

### 🧾 Admin Analytics
- Admin dashboard
- Abuse logs
- Map of downloads
- Upload/download stats

### 🔗 Link Generation
- Generates one-time access tokens
- Stores encrypted tokens securely
- Displays shareable link to user

### 🛡️ Security Layers
- Optional CAPTCHA
- Rate limiting
- CSP, XSS, CORS hardening
- HTTPS enforced
- Alert on suspicious behavior

---

## 🛠 Tech Stack

- Frontend: HTML/CSS/JS with in-browser crypto libraries
- Backend: Node.js / Python (Flask or FastAPI)
- Database: MongoDB / PostgreSQL
- Storage: Amazon S3 or MinIO
- Security: AES, RSA, JWT, HTTPS, OTP

---

## 🚀 How It Works

1. **User signs up/logs in**
2. **Uploads a file → Encrypted in browser**
3. **AES key encrypted with RSA and sent to backend**
4. **System generates a one-time link with expiry/download limits**
5. **Recipient clicks the link → Token verified → File decrypted in browser**
6. **Link is invalidated and access is logged**

---

## 📸 Architecture

Check out the full system architecture in the diagram below:

![Architecture Diagram](./path/to/your/image.png)

---

## 🧪 Setup & Run Locally

```bash
# Clone the repository
git clone https://github.com/jayy1511/W_Share.git
cd W_Share

# Install dependencies
npm install  # or pip install -r requirements.txt for Python backend

# Start the app
npm start     # or uvicorn main:app --reload for FastAPI backend
