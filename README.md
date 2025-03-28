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

  ---

  # OSINT Techniques & Google Dorking Cheatsheet

## About
This repository provides a collection of OSINT (Open Source Intelligence) techniques, Google dorking queries, and automation tools to gather publicly available information on individuals, organizations, leaked data, and more.

## Contents
- **Google Dorking**: Queries to find emails, passwords, confidential files, and open databases.
- **People OSINT**: Techniques to discover social media profiles, track geolocation, and search leaked data.
- **Dark Web OSINT**: Methods to find leaked credentials, exposed files, and confidential documents.
- **Organizational OSINT**: Finding subdomains, employee details, and company vulnerabilities.
- **OSINT Tools**: Automated tools like SpiderFoot, theHarvester, Amass, and Sherlock for data collection.

---

## 🌐 Google Dorking for OSINT
### 🔍 Finding Emails & Credentials
- **Locate Publicly Available Emails**  
  ```bash
  site:pastebin.com OR site:throwbin.io "@gmail.com" OR "@yahoo.com"
  ```
- **Search for Leaked Passwords**  
  ```bash
  site:github.com OR site:pastebin.com "password" "username"
  ```
- **Find Corporate Email Addresses**  
  ```bash
  site:linkedin.com "@company.com"
  ```

### 📜 Finding Confidential Files
- **Look for Sensitive PDF Documents**  
  ```bash
  filetype:pdf OR filetype:docx "confidential" OR "internal"
  ```
- **Discover Public Google Drive Links**  
  ```bash
  site:drive.google.com "private" OR "restricted"
  ```
- **Identify Open FTP Servers**  
  ```bash
  intitle:"index of" "ftp" site:target.com
  ```

### 📂 Exposed Databases
- **Unprotected MongoDB Instances**  
  ```bash
  inurl:27017 "_id"
  ```
- **Open Elasticsearch Instances**  
  ```bash
  inurl:9200 "_search"
  ```
- **Public Firebase Databases**  
  ```bash
  site:firebasestorage.googleapis.com
  ```

---

## 🕵️‍♂️ OSINT on People
### 🔍 Social Media Investigation
- **Find Profiles Across Social Platforms**  
  ```bash
  site:facebook.com OR site:twitter.com OR site:instagram.com "John Doe"
  ```
- **Search for Usernames on Websites**  
  ```bash
  site:github.com OR site:reddit.com "username123"
  ```
- **Find a Person’s Facebook Profile by Location**  
  ```bash
  site:facebook.com "John Doe" "New York"
  ```

### 📍 Geolocation Tracking
- **Search Tweets from a Specific Area**  
  ```bash
  site:twitter.com "New York" geocode:40.7128,-74.0060,5km
  ```
- **Extract GPS Data from Images**  
  ```bash
  exiftool image.jpg
  ```
- **Perform Reverse Image Search**  
  🔗 [Google Reverse Image Search](https://images.google.com)

---

## 📡 Dark Web & Leaked Data OSINT
### 🔑 Searching for Leaked Credentials
- **Check if an Email is Breached**  
  🔗 [Have I Been Pwned](https://haveibeenpwned.com)
- **Look for Exposed Passwords on Dark Web**  
  ```bash
  site:darksearch.io "email@example.com"
  ```
- **Find Leaked Data on Pastebin**  
  ```bash
  site:pastebin.com "password" OR "login"
  ```

### 📁 Discovering Exposed Files
- **Search Government & Military Docs**  
  ```bash
  site:gov OR site:mil filetype:pdf "confidential"
  ```
- **Find Public AWS Buckets**  
  ```bash
  site:s3.amazonaws.com "target"
  ```
- **Look for API Keys in GitHub Repositories**  
  ```bash
  site:github.com "api_key" "secret"
  ```

---

## 🔍 OSINT on Organizations
### 🌎 Subdomain & Infrastructure Discovery
- **Find Hidden Subdomains**  
  ```bash
  subfinder -d target.com
  ```
- **Locate Public API Endpoints**  
  ```bash
  site:target.com "api/v1/"
  ```

### 🔗 Employee & Corporate Intelligence
- **Look for Employee LinkedIn Profiles**  
  ```bash
  site:linkedin.com "company.com"
  ```
- **Find Open Zoom Meetings**  
  ```bash
  site:zoom.us "join" "meeting"
  ```
- **Discover Public Slack Channels**  
  ```bash
  site:slack.com "company"
  ```

---

## ⚡ OSINT Automation Tools
### 🛠 Recon & Intelligence Gathering
- **SpiderFoot** – Automated OSINT tool  
  ```bash
  spiderfoot -s target.com
  ```
- **theHarvester** – Gather emails & subdomains  
  ```bash
  theHarvester -d target.com -b all
  ```
- **Amass** – Network mapping & reconnaissance  
  ```bash
  amass enum -d target.com
  ```
- **Metagoofil** – Extract metadata from files  
  ```bash
  metagoofil -d target.com -t pdf -o results/
  ```

### 📢 Social Media OSINT
- **Sherlock** – Locate Social Media Accounts  
  ```bash
  sherlock username
  ```
- **Instagram Scraper** – Extract Data from Instagram  
  ```bash
  instaloader --login username target_account
  ```

### 🌍 Geolocation & Image OSINT
- **ExifTool** – Extract Metadata from Images  
  ```bash
  exiftool image.jpg
  ```
- **Reverse Image Search on Google**  
  🔗 [Google Images](https://images.google.com)

