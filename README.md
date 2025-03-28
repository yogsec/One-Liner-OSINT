# One Liner OSINT

A collection of powerful one-liner commands for Open-Source Intelligence (OSINT) gathering. This repository provides quick and efficient command-line solutions to extract valuable information from public sources, including domain reconnaissance, social media analysis, metadata extraction, and more. Perfect for security researchers, bug bounty hunters, and ethical hackers looking to automate OSINT tasks with minimal effort. 🚀

---

## **🔍 OSINT Dorks for Finding Personal Information**
### **📧 Email & Contact Information**
- **Find a person's email address**:  
  ```bash
  "John Doe" "@gmail.com" | "@yahoo.com" | "@outlook.com" -www
  ```
- **Find leaked email addresses in data breaches**:  
  ```bash
  "John Doe" site:pastebin.com | site:throwbin.io | site:breachforums.st
  ```
- **Look for email addresses from a specific domain**:  
  ```bash
  site:targetcompany.com "@targetcompany.com"
  ```
- **Search for phone numbers**:  
  ```bash
  "John Doe" "phone" | "contact" | "mobile" | "WhatsApp"
  ```
- **Find a person’s email in GitHub repositories**:  
  ```bash
  site:github.com "John Doe" "@gmail.com"
  ```
- **Find all social media accounts of a person**:  
  ```bash
  "John Doe" site:linkedin.com | site:facebook.com | site:twitter.com | site:instagram.com
  ```
- **Find someone’s Facebook profile even if hidden**:  
  ```bash
  "John Doe" site:facebook.com/public/
  ```
- **Search for Instagram profiles**:  
  ```bash
  site:instagram.com "John Doe"
  ```
- **Look for their posts on forums (Quora, Reddit, etc.)**:  
  ```bash
  "John Doe" site:reddit.com | site:quora.com | site:stackoverflow.com
  ```
- **Search for personal blogs and old web profiles**:  
  ```bash
  "John Doe" site:medium.com | site:tumblr.com | site:blogspot.com
  ```
- **Find their Amazon wishlist**:  
  ```bash
  "John Doe" site:amazon.com "wishlist"
  ```
- **Look for mentions in news articles**:  
  ```bash
  "John Doe" site:nytimes.com | site:bbc.com | site:cnn.com
  ```
- **Find someone’s pictures across the web**:  
  ```bash
  "John Doe" site:flickr.com | site:500px.com | site:pinterest.com
  ```

### **📜 Resumes, CVs, & Work History**
- **Find someone's resume or CV**:  
  ```bash
  "John Doe" filetype:pdf | filetype:doc "resume" | "curriculum vitae"
  ```
- **Look for employment history on LinkedIn**:  
  ```bash
  site:linkedin.com/in "John Doe"
  ```
- **Find past job applications**:  
  ```bash
  "John Doe" site:indeed.com | site:glassdoor.com
  ```

---

## **🔍 OSINT Dorks for Finding Organizational Information**
### **🏢 Subdomains & Infrastructure**
- **Find all subdomains of a company**:  
  ```bash
  site:*.targetcompany.com -www
  ```
- **Search for sensitive open directories**:  
  ```bash
  intitle:"index of" site:targetcompany.com
  ```
- **Check for publicly accessible FTP servers**:  
  ```bash
  inurl:ftp:// targetcompany.com
  ```
- **Find internal company documents**:  
  ```bash
  site:targetcompany.com ext:pdf | ext:doc | ext:ppt "confidential"
  ```
- **Look for job postings to understand their tech stack**:  
  ```bash
  site:targetcompany.com "hiring" | "we are looking for"
  ```
- **Check for network devices and login portals**:  
  ```bash
  site:targetcompany.com inurl:admin | inurl:dashboard | inurl:login
  ```

### **🔎 Leaks & Security Issues**
- **Search for past security incidents**:  
  ```bash
  "targetcompany.com" "data breach" | "leaked database"
  ```
- **Look for exposed database files**:  
  ```bash
  site:targetcompany.com ext:sql | ext:db | ext:json
  ```
- **Find security vulnerabilities related to the organization**:  
  ```bash
  site:targetcompany.com inurl:CVE- | intext:"vulnerability"
  ```
