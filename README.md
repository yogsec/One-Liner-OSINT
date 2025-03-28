# One Liner OSINT

A collection of powerful one-liner commands for Open-Source Intelligence (OSINT) gathering. This repository provides quick and efficient command-line solutions to extract valuable information from public sources, including domain reconnaissance, social media analysis, metadata extraction, and more. Perfect for security researchers, bug bounty hunters, and ethical hackers looking to automate OSINT tasks with minimal effort.

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

---


### **🔎 Advanced Google Dorks for People & Organizations**
- **Find Personal Information on a Website**
  ```bash
  site:target.com intext:"phone number" OR "email" OR "address"
  ```
- **Find Login Pages**
  ```bash
  site:target.com inurl:login
  ```
- **Find PDFs & Documents Containing Emails**
  ```bash
  filetype:pdf OR filetype:docx OR filetype:xls intext:"@gmail.com"
  ```
- **Find Public FTP Servers**
  ```bash
  intitle:"index of" "ftp" site:target.com
  ```

### **📍 Find Hidden Data & Cached Info**
- **Search in Google Cache**
  ```bash
  cache:target.com
  ```
- **Find Deleted Pages via Wayback Machine**
  ```bash
  site:web.archive.org target.com
  ```
- **Search for Sensitive PDF Reports**
  ```bash
  site:gov OR site:mil OR site:edu filetype:pdf "confidential"
  ```

---

## **🕵️‍♂️ OSINT on People (Personal Reconnaissance)**
### **🔎 Find Someone's Digital Footprint**
- **People Search Engines**  
  - 🔗 [https://pipl.com](https://pipl.com)  
  - 🔗 [https://thatsthem.com](https://thatsthem.com)  
  - 🔗 [https://www.spokeo.com](https://www.spokeo.com)  

- **Find Phone Numbers & Emails**
  ```bash
  site:target.com "phone number" OR "email"
  ```
- **Reverse Email Lookup**
  ```bash
  site:linkedin.com OR site:facebook.com "email@example.com"
  ```

### **👀 Social Media Intelligence (SOCMINT)**
- **Find All Social Media Accounts for a Username**
  ```bash
  site:twitter.com OR site:instagram.com OR site:facebook.com "username"
  ```
- **Find Facebook Posts About Someone**
  ```bash
  site:facebook.com "John Doe" "lives in New York"
  ```
- **Find Instagram & TikTok Accounts via Google**
  ```bash
  site:instagram.com "john_doe" OR site:tiktok.com "john_doe"
  ```
- **Use Sherlock for Automated Social Media OSINT**
  ```bash
  sherlock username
  ```

---

## **📍 Geolocation OSINT**
### **🔎 Track Location from Photos**
- **Extract GPS from Image Metadata**
  ```bash
  exiftool image.jpg
  ```
- **Search Google for Images from a Location**
  ```bash
  site:instagram.com "New York City" "Times Square"
  ```
- **Find Someone's Location via Twitter**
  ```bash
  site:twitter.com "New York" geocode:40.7128,-74.0060,5km
  ```

### **🔎 Reverse Image Search**
- **Find Someone’s Profile Picture on Other Sites**
  🔗 [https://www.tineye.com](https://www.tineye.com)  
  🔗 [https://images.google.com](https://images.google.com)  

- **Find Images in Cached Archives**
  ```bash
  site:web.archive.org "target image name"
  ```

---

## **💾 Leaked Database & Dark Web OSINT**
### **🔑 Find Leaked Emails & Passwords**
- **Check if an Email is Breached**
  🔗 [https://haveibeenpwned.com](https://haveibeenpwned.com)  
- **Find Leaked Databases on Pastebin**
  ```bash
  site:pastebin.com "password" "target.com"
  ```
- **Search for Leaked Credentials on the Dark Web**
  ```bash
  site:darksearch.io "email@example.com"
  ```

### **📂 Find Exposed Databases**
- **Search for Open MongoDB**
  ```bash
  inurl:27017 "_id"
  ```
- **Search for Open Elasticsearch Instances**
  ```bash
  inurl:9200 "_search"
  ```
- **Find Firebase Databases**
  ```bash
  site:firebasestorage.googleapis.com
  ```

---

## **📡 OSINT on Organizations**
### **🔎 Subdomain & Infrastructure Recon**
- **Find Hidden Subdomains**
  ```bash
  subfinder -d target.com
  ```
- **Find Exposed API Endpoints**
  ```bash
  site:target.com "api/v1/"
  ```

### **🔗 Find Employee Emails**
- **Find Company Email Patterns with Hunter.io**  
  🔗 [https://hunter.io](https://hunter.io)  
- **Search for Leaked Employee Emails**
  ```bash
  site:linkedin.com "@target.com"
  ```

### **🔎 Detect Exposed Cloud Storage**
- **Find Public Google Drive Links**
  ```bash
  site:drive.google.com "confidential"
  ```
- **Find Public AWS S3 Buckets**
  ```bash
  site:s3.amazonaws.com "target"
  ```

---

## **🚀 OSINT Automation Tools**
### **🔎 Comprehensive OSINT Frameworks**
- **SpiderFoot** – Automated OSINT tool  
  ```bash
  spiderfoot -s target.com
  ```
- **theHarvester** – Gather emails & subdomains  
  ```bash
  theHarvester -d target.com -b all
  ```

### **⚡ Fast Recon Tools**
- **Amass** – Network mapping & reconnaissance  
  ```bash
  amass enum -d target.com
  ```
- **Metagoofil** – Extract metadata from public files  
  ```bash
  metagoofil -d target.com -t pdf -o results/
  ```
- **Maltego** – Visualize OSINT data connections  
  🔗 [https://www.maltego.com](https://www.maltego.com)  

---


### **📍 Find Deleted & Cached Information**
- **Wayback Machine (Internet Archive)** – View old versions of websites  
  🔗 [https://web.archive.org](https://web.archive.org)  
  ```bash
  curl "http://web.archive.org/cdx/search/cdx?url=target.com&output=json"
  ```
- **Google Cache** – View cached pages of deleted content  
  ```bash
  cache:target.com
  ```
- **Bing Cache** – Alternative for Google Cache  
  ```bash
  inurl:cache:target.com
  ```

### **🔍 Extract Content from Websites**
- **HTTrack** – Clone websites for offline analysis  
  ```bash
  httrack https://target.com
  ```
- **wget** – Download full websites  
  ```bash
  wget -r -np -k https://target.com
  ```
- **Scrapy** – Python framework for web scraping  
  ```bash
  scrapy startproject target_spider
  ```

---

## **🕵️‍♂️ OSINT on People (Personal Intelligence)**
### **🔎 Find Hidden Personal Information**
- **People Search Engines**  
  - 🔗 [https://www.spokeo.com](https://www.spokeo.com)  
  - 🔗 [https://pipl.com](https://pipl.com)  
  - 🔗 [https://thatsthem.com](https://thatsthem.com)  
  - 🔗 [https://peekyou.com](https://peekyou.com)  

- **Find Phone Numbers & Emails**  
  ```bash
  site:target.com "phone number" OR "contact email"
  ```
- **Search for Social Security Numbers (SSNs)**
  ```bash
  filetype:xls OR filetype:csv "SSN"
  ```
- **Username Lookups (Deep Search)**
  ```bash
  inurl:profile "username"
  ```

### **👤 Find Personal Email Addresses**
- **Hunter.io** – Find email patterns from company domains  
  🔗 [https://hunter.io](https://hunter.io)  
- **Holehe** – Check if an email is linked to online accounts  
  ```bash
  holehe email@example.com
  ```
- **Email Permutator** – Generate possible email variations  
  ```bash
  permute.py first last company.com
  ```

---

## **📌 Find Geolocation & Address Details**
### **📍 Extract GPS from Images**
- **ExifTool** – Extract geolocation from images  
  ```bash
  exiftool image.jpg
  ```
- **Google Earth Historical Imagery** – View past satellite images  
  🔗 [https://earth.google.com](https://earth.google.com)  

### **🗺️ Find Someone’s Address**
- **WhitePages & PeopleFinders**  
  - 🔗 [https://www.whitepages.com](https://www.whitepages.com)  
  - 🔗 [https://www.peoplefinders.com](https://www.peoplefinders.com)  

- **Reverse Address Lookup**
  ```bash
  site:whitepages.com "target address"
  ```

---

## **💾 Leaked Database & Credential Hunting**
### **🔑 Find Leaked Passwords**
- **Have I Been Pwned?** – Check if email is breached  
  🔗 [https://haveibeenpwned.com](https://haveibeenpwned.com)  
- **H8mail** – Search for leaked credentials  
  ```bash
  h8mail -t email@example.com
  ```
- **BreachForums (Mirror)** – Search data leaks  
  🔗 [https://breachforums.st](https://breachforums.st)  

### **📂 Search for Exposed Databases**
- **Find Public MongoDB Databases**
  ```bash
  inurl:27017 "MongoDB"
  ```
- **Search for Open Elasticsearch DBs**
  ```bash
  inurl:9200 "_search"
  ```
- **Check for Firebase Data Leaks**
  ```bash
  site:firebasestorage.googleapis.com
  ```

---

## **🔎 Deep Web & Dark Web OSINT**
### **🛑 Search Hidden Onion Sites**
- **Ahmia** – Search the dark web  
  🔗 [https://ahmia.fi](https://ahmia.fi)  
- **TorBot** – Automate OSINT on onion sites  
  ```bash
  git clone https://github.com/DedSecInside/TorBot.git
  ```
- **OnionSearch** – Find stolen credentials  
  ```bash
  python3 onionsearch.py target
  ```

### **📡 Scan Deep Web Data Leaks**
- **DarkSearch.io** – Search dark web leaks  
  🔗 [https://darksearch.io](https://darksearch.io)  
- **IntelX** – Search breached data  
  🔗 [https://intelx.io](https://intelx.io)  

---

## **🛠️ Subdomain & Website OSINT**
### **🔎 Find Hidden Subdomains**
- **Subfinder** – Collect subdomains  
  ```bash
  subfinder -d target.com
  ```
- **Amass** – Map an organization's infrastructure  
  ```bash
  amass enum -d target.com
  ```

### **🔗 Discover Public API Endpoints**
- **Find API Keys in GitHub**
  ```bash
  site:github.com "api_key" "target.com"
  ```
- **Search for Publicly Accessible APIs**
  ```bash
  site:target.com "api/v1/"
  ```

---

## **🚀 Automated OSINT Tools**
### **🔎 OSINT Frameworks**
- **SpiderFoot** – Full OSINT automation  
  ```bash
  spiderfoot -s target.com
  ```
- **Metagoofil** – Extract metadata from public files  
  ```bash
  metagoofil -d target.com -t pdf -o results/
  ```

### **⚡ Fast Data Gathering**
- **theHarvester** – Find emails, subdomains, and metadata  
  ```bash
  theHarvester -d target.com -b all
  ```
- **Maltego** – Visualize OSINT data connections  
  🔗 [https://www.maltego.com](https://www.maltego.com)  

---


### **📍 Find Hidden Data & Leaks**
- **Shodan** – Search for exposed servers, IoT devices  
  🔗 [https://www.shodan.io](https://www.shodan.io)  
  ```bash
  shodan search "Default password"
  ```
- **Censys** – Find exposed devices, certificates, open ports  
  🔗 [https://censys.io](https://censys.io)  
  ```bash
  censys search target.com
  ```
- **ZoomEye** – Chinese version of Shodan with more results  
  🔗 [https://www.zoomeye.org](https://www.zoomeye.org)  
- **BinaryEdge** – Advanced IP and port scanning  
  🔗 [https://www.binaryedge.io](https://www.binaryedge.io)  

### **📂 Data Breach & Credential Lookups**
- **WeLeakInfo (Mirror)** – Search for exposed credentials  
  🔗 [https://weleakinfo.to](https://weleakinfo.to)  
- **LeaksDB** – Find leaked usernames and passwords  
  🔗 [https://leaksdb.com](https://leaksdb.com)  
- **Snusbase** – Advanced breach database  
  🔗 [https://snusbase.com](https://snusbase.com)  
- **Scylla.sh** – Search credentials from past dumps  
  🔗 [https://scylla.sh](https://scylla.sh)  

---

## **🕵️ Social Media Intelligence (SOCMINT)**
### **🔍 Find Hidden Social Media Accounts**
- **WhatsMyName** – Search username across multiple platforms  
  🔗 [https://whatsmyname.app](https://whatsmyname.app)  
- **Sherlock** – Find accounts linked to a username  
  ```bash
  python3 sherlock.py username
  ```
- **Maigret** – More powerful than Sherlock for finding social accounts  
  ```bash
  python3 maigret.py username
  ```

### **📸 Reverse Image Search on Social Media**
- **Yandex** – Best for finding hidden social media profiles  
  🔗 [https://yandex.com/images](https://yandex.com/images)  
- **Google Lens** – Identifies faces, places, and objects  
  🔗 [https://lens.google](https://lens.google)  
- **PimEyes** – AI-powered face recognition  
  🔗 [https://pimeyes.com](https://pimeyes.com)  

### **📍 Track Geolocation Data**
- **GeoCreepy** – Extracts geolocation from social media posts  
  ```bash
  git clone https://github.com/ilektrojohn/creepy.git
  ```
- **ExifTool** – Extracts GPS coordinates from photos  
  ```bash
  exiftool image.jpg
  ```
- **Google Earth Historical Imagery** – View past satellite images  
  🔗 [https://earth.google.com](https://earth.google.com)  

---

## **🔑 Extract Metadata & Documents**
### **📂 Hidden Metadata in Files**
- **FOCA** – Extracts metadata from documents, PDFs  
  🔗 [https://elevenpaths.com/foca](https://elevenpaths.com/foca)  
- **ExifTool** – Extract hidden details from images and documents  
  ```bash
  exiftool document.docx
  ```
- **Strings** – Find hidden text in binary files  
  ```bash
  strings target.pdf
  ```
- **Metadata2Go** – Online metadata extraction  
  🔗 [https://www.metadata2go.com](https://www.metadata2go.com)  

---

## **📡 Subdomain & Website Enumeration**
### **🔍 Find Hidden Subdomains**
- **Subfinder** – Finds subdomains via multiple sources  
  ```bash
  subfinder -d target.com
  ```
- **Findomain** – Fast subdomain enumeration  
  ```bash
  findomain -t target.com
  ```
- **CRT.sh** – Find SSL certificates linked to subdomains  
  🔗 [https://crt.sh](https://crt.sh)  

### **🛠️ Find Exposed Directories**
- **GoBuster** – Find hidden directories and files  
  ```bash
  gobuster dir -u target.com -w wordlist.txt
  ```
- **Dirsearch** – More advanced directory brute-forcing  
  ```bash
  python3 dirsearch.py -u target.com -e php,html,js
  ```

---

## **🔎 Google Dorks (More Advanced)**
### **🗂️ Find Exposed Databases**
- **Search for SQL dumps**  
  ```bash
  inurl:.sql filetype:sql
  ```
- **Find public Firebase databases**  
  ```bash
  site:firebasestorage.googleapis.com
  ```
- **Locate public MongoDB instances**  
  ```bash
  inurl:27017 filetype:log
  ```

### **📄 Find Sensitive Documents**
- **Find internal reports**  
  ```bash
  site:target.com filetype:pdf "confidential"
  ```
- **Search for exposed .env files (credentials)**  
  ```bash
  inurl:.env "DB_PASSWORD"
  ```
- **Look for exposed config files**  
  ```bash
  intitle:"index of" "wp-config.php"
  ```

---

## **💾 Data Breach & Credential Automation**
### **📂 Check If an Email Is in a Breach**
- **Holehe** – Check if an email is linked to social accounts  
  ```bash
  holehe email@example.com
  ```
- **H8mail** – Find leaked passwords  
  ```bash
  h8mail -t email@example.com
  ```
- **GHunt** – Extract data from Google accounts  
  ```bash
  python3 ghunt.py email@example.com
  ```

### **🚀 Dark Web Data Mining**
- **TorBot** – Automates OSINT on dark web sites  
  ```bash
  git clone https://github.com/DedSecInside/TorBot.git
  ```
- **OnionSearch** – Searches dark web for stolen data  
  ```bash
  python3 onionsearch.py target
  ```

---


### **🔎 People & Organization Searches**
- **Intelius** – Background checks, addresses, phone numbers  
  🔗 [https://www.intelius.com](https://www.intelius.com)  
- **PeekYou** – Finds social media profiles and online presence  
  🔗 [https://www.peekyou.com](https://www.peekyou.com)  
- **Pipl** – Deep web search for emails, numbers, social links  
  🔗 [https://pipl.com](https://pipl.com)  
- **Spokeo** – Search for personal details, addresses, relatives  
  🔗 [https://www.spokeo.com](https://www.spokeo.com)  

### **📝 Leaked Data & Breach Searches**
- **Have I Been Pwned** – Check if an email is in a data breach  
  🔗 [https://haveibeenpwned.com](https://haveibeenpwned.com)  
- **DeHashed** – Advanced search for breached credentials  
  🔗 [https://www.dehashed.com](https://www.dehashed.com)  
- **LeakCheck** – Finds leaked passwords, usernames, emails  
  🔗 [https://leakcheck.io](https://leakcheck.io)  
- **IntelX** – Search dark web leaks, emails, pastes  
  🔗 [https://intelx.io](https://intelx.io)  

### **🧕️ Dark Web & Underground Searches**
- **Ahmia** – Search the Tor network  
  🔗 [https://ahmia.fi](https://ahmia.fi)  
- **OnionLand Search** – Index of hidden .onion sites  
  🔗 [https://onionlandsearchengine.com](https://onionlandsearchengine.com)  
- **DarkSearch** – Crawls dark web marketplaces, forums  
  🔗 [https://darksearch.io](https://darksearch.io)  
- **TorBot** – Open-source dark web search tool  
  ```bash
  git clone https://github.com/DedSecInside/TorBot.git
  ```

---

## **📎 Advanced Metadata & Document Analysis**
### **🔑 Extract Metadata from Images & Documents**
- **ExifTool** – Extract metadata from photos, PDFs, docs  
  ```bash
  exiftool target.jpg
  ```
- **strings** – Find hidden text in binary files  
  ```bash
  strings target.docx
  ```
- **pdf-parser** – Search for hidden data in PDFs  
  ```bash
  pdf-parser target.pdf
  ```
- **OpenMetadata** – Online metadata extractor  
  🔗 [https://metapicz.com](https://metapicz.com)  

### **🔍 Reverse Image & Facial Recognition**
- **Google Lens** – Reverse image search  
  🔗 [https://lens.google](https://lens.google)  
- **Yandex Images** – More accurate than Google for faces  
  🔗 [https://yandex.com/images](https://yandex.com/images)  
- **PimEyes** – AI-powered face recognition  
  🔗 [https://pimeyes.com](https://pimeyes.com)  
- **TinEye** – Reverse image lookup  
  🔗 [https://tineye.com](https://tineye.com)  

---

## **🚀 Automated OSINT Tools**
### **🐾 Subdomain & Website Enumeration**
- **Sublist3r** – Find subdomains of a target  
  ```bash
  python sublist3r.py -d target.com
  ```
- **Amass** – Powerful OSINT reconnaissance tool  
  ```bash
  amass enum -d target.com
  ```
- **CRT.sh** – Find SSL certificates revealing hidden subdomains  
  🔗 [https://crt.sh](https://crt.sh)  

### **📞 Phone Number Intelligence**
- **NumVerify** – Check phone number validity  
  🔗 [https://numverify.com](https://numverify.com)  
- **Truecaller** – Find registered names of phone numbers  
  🔗 [https://www.truecaller.com](https://www.truecaller.com)  
- **OSINTFramework** – Collection of phone lookup resources  
  🔗 [https://osintframework.com](https://osintframework.com)  

---

## **🔍 Google Dorks (More Advanced)**
- **Find plaintext passwords**  
  ```bash
  intext:"password" filetype:log
  ```
- **Search for exposed email lists**  
  ```bash
  site:pastebin.com "email" | "password"
  ```
- **Locate hidden admin panels**  
  ```bash
  site:target.com inurl:admin
  ```

---

