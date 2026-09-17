# One Liner OSINT

![image](https://github.com/yogsec/One-Liner-OSINT/blob/main/power-rangers.gif?raw=true)

A collection of powerful one-liner commands for Open-Source Intelligence (OSINT) gathering. This repository provides quick and efficient command-line solutions to extract valuable information from public sources, including domain reconnaissance, social media analysis, metadata extraction, and more. Perfect for security researchers, bug bounty hunters, and ethical hackers looking to automate OSINT tasks with minimal effort.

---

## **OSINT Dorks for Finding Personal Information**
### **Email & Contact Information**
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

### **Resumes, CVs, & Work History**
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

## **OSINT Dorks for Finding Organizational Information**
### **Subdomains & Infrastructure**
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

### **Leaks & Security Issues**
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

### Finding Emails & Credentials
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

### Finding Confidential Files
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

### Exposed Databases
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

## OSINT on People
### Social Media Investigation
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

### Geolocation Tracking
- **Search Tweets from a Specific Area**  
  ```bash
  site:twitter.com "New York" geocode:40.7128,-74.0060,5km
  ```
- **Extract GPS Data from Images**  
  ```bash
  exiftool image.jpg
  ```
- **Perform Reverse Image Search**  
  [Google Reverse Image Search](https://images.google.com)

---

## Dark Web & Leaked Data OSINT
### Searching for Leaked Credentials
- **Check if an Email is Breached**  
  [Have I Been Pwned](https://haveibeenpwned.com)
- **Look for Exposed Passwords on Dark Web**  
  ```bash
  site:darksearch.io "email@example.com"
  ```
- **Find Leaked Data on Pastebin**  
  ```bash
  site:pastebin.com "password" OR "login"
  ```

### Discovering Exposed Files
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

## OSINT on Organizations
### Subdomain & Infrastructure Discovery
- **Find Hidden Subdomains**  
  ```bash
  subfinder -d target.com
  ```
- **Locate Public API Endpoints**  
  ```bash
  site:target.com "api/v1/"
  ```

### Employee & Corporate Intelligence
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

## OSINT Automation Tools
### Recon & Intelligence Gathering
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

### Social Media OSINT
- **Sherlock** – Locate Social Media Accounts  
  ```bash
  sherlock username
  ```
- **Instagram Scraper** – Extract Data from Instagram  
  ```bash
  instaloader --login username target_account
  ```

### Geolocation & Image OSINT
- **ExifTool** – Extract Metadata from Images  
  ```bash
  exiftool image.jpg
  ```
- **Reverse Image Search on Google**  
  [Google Images](https://images.google.com)

---


### **Advanced Google Dorks for People & Organizations**
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

### **Find Hidden Data & Cached Info**
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

## **OSINT on People (Personal Reconnaissance)**
### **Find Someone's Digital Footprint**
- **People Search Engines**  
  - [https://pipl.com](https://pipl.com)  
  - [https://thatsthem.com](https://thatsthem.com)  
  - [https://www.spokeo.com](https://www.spokeo.com)  

- **Find Phone Numbers & Emails**
  ```bash
  site:target.com "phone number" OR "email"
  ```
- **Reverse Email Lookup**
  ```bash
  site:linkedin.com OR site:facebook.com "email@example.com"
  ```

### **Social Media Intelligence (SOCMINT)**
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

## **Geolocation OSINT**
### **Track Location from Photos**
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

### **Reverse Image Search**
- **Find Someone’s Profile Picture on Other Sites**
  [https://www.tineye.com](https://www.tineye.com)  
  [https://images.google.com](https://images.google.com)  

- **Find Images in Cached Archives**
  ```bash
  site:web.archive.org "target image name"
  ```

---

## **Leaked Database & Dark Web OSINT**
### **Find Leaked Emails & Passwords**
- **Check if an Email is Breached**
  [https://haveibeenpwned.com](https://haveibeenpwned.com)  
- **Find Leaked Databases on Pastebin**
  ```bash
  site:pastebin.com "password" "target.com"
  ```
- **Search for Leaked Credentials on the Dark Web**
  ```bash
  site:darksearch.io "email@example.com"
  ```

### **Find Exposed Databases**
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

## **OSINT on Organizations**
### **Subdomain & Infrastructure Recon**
- **Find Hidden Subdomains**
  ```bash
  subfinder -d target.com
  ```
- **Find Exposed API Endpoints**
  ```bash
  site:target.com "api/v1/"
  ```

### **Find Employee Emails**
- **Find Company Email Patterns with Hunter.io**  
  [https://hunter.io](https://hunter.io)  
- **Search for Leaked Employee Emails**
  ```bash
  site:linkedin.com "@target.com"
  ```

### **Detect Exposed Cloud Storage**
- **Find Public Google Drive Links**
  ```bash
  site:drive.google.com "confidential"
  ```
- **Find Public AWS S3 Buckets**
  ```bash
  site:s3.amazonaws.com "target"
  ```

---

## **OSINT Automation Tools**
### **Comprehensive OSINT Frameworks**
- **SpiderFoot** – Automated OSINT tool  
  ```bash
  spiderfoot -s target.com
  ```
- **theHarvester** – Gather emails & subdomains  
  ```bash
  theHarvester -d target.com -b all
  ```

### **Fast Recon Tools**
- **Amass** – Network mapping & reconnaissance  
  ```bash
  amass enum -d target.com
  ```
- **Metagoofil** – Extract metadata from public files  
  ```bash
  metagoofil -d target.com -t pdf -o results/
  ```
- **Maltego** – Visualize OSINT data connections  
  [https://www.maltego.com](https://www.maltego.com)  

---


### **Find Deleted & Cached Information**
- **Wayback Machine (Internet Archive)** – View old versions of websites  
  [https://web.archive.org](https://web.archive.org)  
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

### **Extract Content from Websites**
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

## **OSINT on People (Personal Intelligence)**
### **Find Hidden Personal Information**
- **People Search Engines**  
  - [https://www.spokeo.com](https://www.spokeo.com)  
  - [https://pipl.com](https://pipl.com)  
  - [https://thatsthem.com](https://thatsthem.com)  
  - [https://peekyou.com](https://peekyou.com)  

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

### **Find Personal Email Addresses**
- **Hunter.io** – Find email patterns from company domains  
  [https://hunter.io](https://hunter.io)  
- **Holehe** – Check if an email is linked to online accounts  
  ```bash
  holehe email@example.com
  ```
- **Email Permutator** – Generate possible email variations  
  ```bash
  permute.py first last company.com
  ```

---

## **Find Geolocation & Address Details**
### **Extract GPS from Images**
- **ExifTool** – Extract geolocation from images  
  ```bash
  exiftool image.jpg
  ```
- **Google Earth Historical Imagery** – View past satellite images  
  [https://earth.google.com](https://earth.google.com)  

### **Find Someone’s Address**
- **WhitePages & PeopleFinders**  
  - [https://www.whitepages.com](https://www.whitepages.com)  
  - [https://www.peoplefinders.com](https://www.peoplefinders.com)  

- **Reverse Address Lookup**
  ```bash
  site:whitepages.com "target address"
  ```

---

## **Leaked Database & Credential Hunting**
### **Find Leaked Passwords**
- **Have I Been Pwned?** – Check if email is breached  
  [https://haveibeenpwned.com](https://haveibeenpwned.com)  
- **H8mail** – Search for leaked credentials  
  ```bash
  h8mail -t email@example.com
  ```
- **BreachForums (Mirror)** – Search data leaks  
  [https://breachforums.st](https://breachforums.st)  

### **Search for Exposed Databases**
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

## **Deep Web & Dark Web OSINT**
### **Search Hidden Onion Sites**
- **Ahmia** – Search the dark web  
  [https://ahmia.fi](https://ahmia.fi)  
- **TorBot** – Automate OSINT on onion sites  
  ```bash
  git clone https://github.com/DedSecInside/TorBot.git
  ```
- **OnionSearch** – Find stolen credentials  
  ```bash
  python3 onionsearch.py target
  ```

### **Scan Deep Web Data Leaks**
- **DarkSearch.io** – Search dark web leaks  
  [https://darksearch.io](https://darksearch.io)  
- **IntelX** – Search breached data  
  [https://intelx.io](https://intelx.io)  

---

## **Subdomain & Website OSINT**
### **Find Hidden Subdomains**
- **Subfinder** – Collect subdomains  
  ```bash
  subfinder -d target.com
  ```
- **Amass** – Map an organization's infrastructure  
  ```bash
  amass enum -d target.com
  ```

### **Discover Public API Endpoints**
- **Find API Keys in GitHub**
  ```bash
  site:github.com "api_key" "target.com"
  ```
- **Search for Publicly Accessible APIs**
  ```bash
  site:target.com "api/v1/"
  ```

---

## **Automated OSINT Tools**
### **OSINT Frameworks**
- **SpiderFoot** – Full OSINT automation  
  ```bash
  spiderfoot -s target.com
  ```
- **Metagoofil** – Extract metadata from public files  
  ```bash
  metagoofil -d target.com -t pdf -o results/
  ```

### **Fast Data Gathering**
- **theHarvester** – Find emails, subdomains, and metadata  
  ```bash
  theHarvester -d target.com -b all
  ```
- **Maltego** – Visualize OSINT data connections  
  [https://www.maltego.com](https://www.maltego.com)  

---


### **Find Hidden Data & Leaks**
- **Shodan** – Search for exposed servers, IoT devices  
  [https://www.shodan.io](https://www.shodan.io)  
  ```bash
  shodan search "Default password"
  ```
- **Censys** – Find exposed devices, certificates, open ports  
  [https://censys.io](https://censys.io)  
  ```bash
  censys search target.com
  ```
- **ZoomEye** – Chinese version of Shodan with more results  
  [https://www.zoomeye.org](https://www.zoomeye.org)  
- **BinaryEdge** – Advanced IP and port scanning  
  [https://www.binaryedge.io](https://www.binaryedge.io)  

### **Data Breach & Credential Lookups**
- **WeLeakInfo (Mirror)** – Search for exposed credentials  
  [https://weleakinfo.to](https://weleakinfo.to)  
- **LeaksDB** – Find leaked usernames and passwords  
  [https://leaksdb.com](https://leaksdb.com)  
- **Snusbase** – Advanced breach database  
  [https://snusbase.com](https://snusbase.com)  
- **Scylla.sh** – Search credentials from past dumps  
  [https://scylla.sh](https://scylla.sh)  

---

## **Social Media Intelligence (SOCMINT)**
### **Find Hidden Social Media Accounts**
- **WhatsMyName** – Search username across multiple platforms  
  [https://whatsmyname.app](https://whatsmyname.app)  
- **Sherlock** – Find accounts linked to a username  
  ```bash
  python3 sherlock.py username
  ```
- **Maigret** – More powerful than Sherlock for finding social accounts  
  ```bash
  python3 maigret.py username
  ```

### **Reverse Image Search on Social Media**
- **Yandex** – Best for finding hidden social media profiles  
  [https://yandex.com/images](https://yandex.com/images)  
- **Google Lens** – Identifies faces, places, and objects  
  [https://lens.google](https://lens.google)  
- **PimEyes** – AI-powered face recognition  
  [https://pimeyes.com](https://pimeyes.com)  

### **Track Geolocation Data**
- **GeoCreepy** – Extracts geolocation from social media posts  
  ```bash
  git clone https://github.com/ilektrojohn/creepy.git
  ```
- **ExifTool** – Extracts GPS coordinates from photos  
  ```bash
  exiftool image.jpg
  ```
- **Google Earth Historical Imagery** – View past satellite images  
  [https://earth.google.com](https://earth.google.com)  

---

## **Extract Metadata & Documents**
### **Hidden Metadata in Files**
- **FOCA** – Extracts metadata from documents, PDFs  
  [https://elevenpaths.com/foca](https://elevenpaths.com/foca)  
- **ExifTool** – Extract hidden details from images and documents  
  ```bash
  exiftool document.docx
  ```
- **Strings** – Find hidden text in binary files  
  ```bash
  strings target.pdf
  ```
- **Metadata2Go** – Online metadata extraction  
  [https://www.metadata2go.com](https://www.metadata2go.com)  

---

## **Subdomain & Website Enumeration**
### **Find Hidden Subdomains**
- **Subfinder** – Finds subdomains via multiple sources  
  ```bash
  subfinder -d target.com
  ```
- **Findomain** – Fast subdomain enumeration  
  ```bash
  findomain -t target.com
  ```
- **CRT.sh** – Find SSL certificates linked to subdomains  
  [https://crt.sh](https://crt.sh)  

### **Find Exposed Directories**
- **GoBuster** – Find hidden directories and files  
  ```bash
  gobuster dir -u target.com -w wordlist.txt
  ```
- **Dirsearch** – More advanced directory brute-forcing  
  ```bash
  python3 dirsearch.py -u target.com -e php,html,js
  ```

---

## **Google Dorks (More Advanced)**
### **Find Exposed Databases**
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

### **Find Sensitive Documents**
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

## **Data Breach & Credential Automation**
### **Check If an Email Is in a Breach**
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

### **Dark Web Data Mining**
- **TorBot** – Automates OSINT on dark web sites  
  ```bash
  git clone https://github.com/DedSecInside/TorBot.git
  ```
- **OnionSearch** – Searches dark web for stolen data  
  ```bash
  python3 onionsearch.py target
  ```

---


### **People & Organization Searches**
- **Intelius** – Background checks, addresses, phone numbers  
  [https://www.intelius.com](https://www.intelius.com)  
- **PeekYou** – Finds social media profiles and online presence  
  [https://www.peekyou.com](https://www.peekyou.com)  
- **Pipl** – Deep web search for emails, numbers, social links  
  [https://pipl.com](https://pipl.com)  
- **Spokeo** – Search for personal details, addresses, relatives  
  [https://www.spokeo.com](https://www.spokeo.com)  

### **Leaked Data & Breach Searches**
- **Have I Been Pwned** – Check if an email is in a data breach  
  [https://haveibeenpwned.com](https://haveibeenpwned.com)  
- **DeHashed** – Advanced search for breached credentials  
  [https://www.dehashed.com](https://www.dehashed.com)  
- **LeakCheck** – Finds leaked passwords, usernames, emails  
  [https://leakcheck.io](https://leakcheck.io)  
- **IntelX** – Search dark web leaks, emails, pastes  
  [https://intelx.io](https://intelx.io)  

### **Dark Web & Underground Searches**
- **Ahmia** – Search the Tor network  
  [https://ahmia.fi](https://ahmia.fi)  
- **OnionLand Search** – Index of hidden .onion sites  
  [https://onionlandsearchengine.com](https://onionlandsearchengine.com)  
- **DarkSearch** – Crawls dark web marketplaces, forums  
  [https://darksearch.io](https://darksearch.io)  
- **TorBot** – Open-source dark web search tool  
  ```bash
  git clone https://github.com/DedSecInside/TorBot.git
  ```

---

## **Advanced Metadata & Document Analysis**
### **Extract Metadata from Images & Documents**
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
  [https://metapicz.com](https://metapicz.com)  

### **Reverse Image & Facial Recognition**
- **Google Lens** – Reverse image search  
  [https://lens.google](https://lens.google)  
- **Yandex Images** – More accurate than Google for faces  
  [https://yandex.com/images](https://yandex.com/images)  
- **PimEyes** – AI-powered face recognition  
  [https://pimeyes.com](https://pimeyes.com)  
- **TinEye** – Reverse image lookup  
  [https://tineye.com](https://tineye.com)  

---

## **Automated OSINT Tools**
### **Subdomain & Website Enumeration**
- **Sublist3r** – Find subdomains of a target  
  ```bash
  python sublist3r.py -d target.com
  ```
- **Amass** – Powerful OSINT reconnaissance tool  
  ```bash
  amass enum -d target.com
  ```
- **CRT.sh** – Find SSL certificates revealing hidden subdomains  
  [https://crt.sh](https://crt.sh)  

### **Phone Number Intelligence**
- **NumVerify** – Check phone number validity  
  [https://numverify.com](https://numverify.com)  
- **Truecaller** – Find registered names of phone numbers  
  [https://www.truecaller.com](https://www.truecaller.com)  
- **OSINTFramework** – Collection of phone lookup resources  
  [https://osintframework.com](https://osintframework.com)  

---

## **Google Dorks (More Advanced)**
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


### Email & Contact Information
Find all email formats used by a company:
```bash
site:targetcompany.com "@targetcompany.com"
```

Search for leaked emails:
```bash
"john.doe@email.com" site:pastebin.com | site:breachforums.st
```

### Phone Numbers & Messaging Apps
Look for leaked phone numbers:
```bash
"+123456789" site:pastebin.com | site:throwbin.io
```

Find if a number is linked to Telegram:
```bash
site:t.me "+123456789"
```

### Social Media & Online Presence
Find hidden social media profiles:
```bash
"John Doe" site:linkedin.com | site:facebook.com | site:instagram.com
```

Locate images of a person:
```bash
site:instagram.com "John Doe" | site:flickr.com "John Doe"
```

### Company Subdomains & Infrastructure
Find all subdomains of a company:
```bash
site:*.targetcompany.com -www
```

Check for open directories:
```bash
intitle:"index of" site:targetcompany.com
```

### API Keys & Credentials
Find API keys leaked in GitHub repositories:
```bash
site:github.com "api_key" | "AWS_SECRET" | "password" targetcompany.com
```

Search for environment files:
```bash
site:targetcompany.com ext:env "DB_PASSWORD" | "SECRET_KEY"
```

### Leaks & Security Issues
Find leaked internal documents:
```bash
site:targetcompany.com ext:pdf | ext:doc "confidential"
```

Look for mentions of a company in hacking forums:
```bash
"targetcompany.com" site:breachforums.st | site:raidforums.com
```

---


## **Google Dorks for Personal OSINT**
- **Find social media profiles**:  
  ```bash
  "John Doe" site:facebook.com | site:twitter.com | site:linkedin.com | site:instagram.com
  ```
- **Find email addresses linked to a person**:  
  ```bash
  "John Doe" "@gmail.com" | "@yahoo.com" | "@outlook.com"
  ```
- **Search for phone numbers**:  
  ```bash
  "John Doe" "contact" | "phone" | "mobile" | "WhatsApp" site:pastebin.com | site:github.com
  ```
- **Find resume or CV**:  
  ```bash
  "John Doe" filetype:pdf | filetype:doc "resume" | "curriculum vitae"
  ```
- **Look for mentions in data leaks**:  
  ```bash
  "John Doe" site:pastebin.com | site:github.com | site:throwbin.io
  ```
- **Check for forum posts**:  
  ```bash
  "John Doe" site:reddit.com | site:quora.com | site:stackoverflow.com
  ```
- **Search for person’s photos**:  
  ```bash
  "John Doe" site:instagram.com | site:pinterest.com | site:flickr.com
  ```
- **Find Amazon wishlists**:  
  ```bash
  "John Doe" site:amazon.com "wishlist"
  ```

---

## **Google Dorks for Organizations**
- **Find subdomains of a company**:  
  ```bash
  site:*.targetcompany.com -www
  ```
- **Look for internal documents**:  
  ```bash
  site:targetcompany.com ext:pdf | ext:doc | ext:ppt "confidential"
  ```
- **Search for employee emails**:  
  ```bash
  "@targetcompany.com" -www
  ```
- **Find job postings to understand technology stack**:  
  ```bash
  "hiring" | "we are looking for" site:targetcompany.com
  ```
- **Check for API keys and credentials on GitHub**:  
  ```bash
  site:github.com "targetcompany.com" "api_key" | "password"
  ```
- **Find exposed databases**:  
  ```bash
  site:targetcompany.com ext:sql | ext:db | ext:json
  ```
- **Search for network devices and login portals**:  
  ```bash
  site:targetcompany.com inurl:login | inurl:admin
  ```
- **Look for configuration files**:  
  ```bash
  site:targetcompany.com ext:conf | ext:ini | ext:log
  ```
- **Check for past security incidents**:  
  ```bash
  "targetcompany.com" "data breach" | "leaked database"
  ```

---

## **Bing & Yandex Dorks for Personal & Organization OSINT**
- **Find person’s profiles on lesser-known sites**:  
  ```bash
  "John Doe" site:myspace.com | site:medium.com | site:tumblr.com
  ```
- **Check for old cached pages**:  
  ```bash
  site:targetcompany.com cache:
  ```
- **Find hidden directories**:  
  ```bash
  intitle:"index of" site:targetcompany.com
  ```

---
---

# **OSINT for Social Media**

## **Automating OSINT with APIs & Scrapers**  
### **Twitter (X) Advanced OSINT**
```bash
# Extract tweets, likes, and followers via API
twint -u username --followers --following --tweets
```
```bash
# Search for leaked credentials in tweets  
twint -s "password OR API_KEY OR AWS_SECRET_ACCESS_KEY"
```
```bash
# Extract Twitter followers without rate limits
twint -u username --followers --csv -o followers.csv
```
```bash
# Find accounts linked to a phone number  
twint -s "+1234567890"
```
```bash
# Monitor target’s tweets in real-time
twint -u username --rt
```
```bash
# Find tweets with geotagged locations  
twint -s "keyword" --near "New York"
```

---

### **Facebook Advanced OSINT**
```bash
# Find all Facebook groups a user is in  
google "site:facebook.com/groups username"
```
```bash
# Extract hidden friends list from a Facebook profile  
curl -s "https://graph.facebook.com/v14.0/username/friends?access_token=YOUR_ACCESS_TOKEN"
```
```bash
# Scrape Facebook public posts by a user  
facebook-scraper username --posts
```
```bash
# Search for leaked Facebook IDs in breaches  
google "site:pastebin.com facebook.com/profile.php?id="
```
```bash
# Find Facebook posts from a specific location  
google "site:facebook.com intext:'📍 New York'"
```

---

### **Instagram Advanced OSINT**
```bash
# Download all Instagram stories from a target  
instaloader --stories username
```
```bash
# Extract Instagram metadata (location, device info, etc.)  
instaloader --metadata-json username
```
```bash
# Find all Instagram profiles linked to an email  
google "site:instagram.com intext:email@example.com"
```
```bash
# Extract geotagged Instagram posts  
google "site:instagram.com intext:'📍 London'"
```
```bash
# Find Instagram users with similar interests  
google "site:instagram.com intext:'#hacking #cybersecurity'"
```

---

### **LinkedIn Advanced OSINT**
```bash
# Scrape all employees from a company  
linkedin-scraper -c "Google"
```
```bash
# Extract job postings and hidden email contacts  
google "site:linkedin.com/jobs 'Cybersecurity Analyst' 'Remote'"
```
```bash
# Find LinkedIn profiles with leaked credentials  
google "site:linkedin.com/in 'password' OR 'email@example.com'"
```
```bash
# Identify LinkedIn users who worked for a company in the past  
google "site:linkedin.com/in 'Worked at Google'"
```
```bash
# Find LinkedIn profiles linked to an IP address  
shodan search "org:'LinkedIn Corp'"
```

---

### **YouTube Advanced OSINT**
```bash
# Download metadata from a YouTube channel  
yt-dlp -J "https://www.youtube.com/c/username"
```
```bash
# Extract subtitles and hidden keywords from videos  
yt-dlp --write-auto-sub --skip-download "https://www.youtube.com/watch?v=VIDEO_ID"
```
```bash
# Find YouTube videos from a specific geolocation  
google "site:youtube.com intext:'📍 New York'"
```
```bash
# Extract YouTube video analytics & insights  
google "site:socialblade.com youtube username"
```
```bash
# Find deleted YouTube videos  
google "site:archive.org youtube.com/watch?v="
```

---

### **TikTok Advanced OSINT**
```bash
# Scrape TikTok videos from a user  
tiktok-scraper user username -n 50 -d
```
```bash
# Extract TikTok comments and engagement analytics  
tiktok-scraper user username -t comments
```
```bash
# Find TikTok accounts linked to an email  
google "site:tiktok.com intext:email@example.com"
```
```bash
# Download TikTok videos and metadata  
tiktok-scraper video VIDEO_ID
```
```bash
# Extract hashtags and trends from TikTok  
google "site:tiktok.com intext:'#OSINT #Cybersecurity'"
```

---

### **Extra OSINT Techniques**
```bash
# Reverse search social media profile pictures  
google "site:tineye.com inurl:result image.jpg"
```
```bash
# Find deep-web social media leaks  
google "site:pastebin.com OR site:ghostbin.com 'email@example.com'"
```
```bash
# Extract hidden metadata from social media images  
exiftool image.jpg
```
```bash
# Search for hidden social media accounts using an IP  
shodan search "ip:xxx.xxx.xxx.xxx"
```

---

## **General Social Media OSINT**
```bash
# Find accounts linked to an email or phone
whatsmyname -u email@example.com
```
```bash
# Check username presence across 500+ platforms
python3 sherlock username
```
```bash
# Scrape all social media links from a website
python3 photon.py -u example.com
```
```bash
# Identify hidden social media accounts of a target
theHarvester -d target.com -b all
```
```bash
# Check for social media accounts linked to an IP
shodan search "org:'Target ISP' http.title:'Login'"
```

---

## **Twitter (X) OSINT**  
```bash
# Get all tweets from a specific time range
twint -u username --since 2024-01-01 --until 2024-03-01
```
```bash
# Extract user email from tweets (if leaked)
twint -u username --email
```
```bash
# Find accounts created in a specific year
twint --year 2010
```
```bash
# Get tweets containing geolocation data
twint -u username --geocode
```
```bash
# Identify all hashtags used by a user
twint -u username --hashtags
```
```bash
# Extract all retweets of a specific user
twint -u username --retweets
```

---

## **Facebook OSINT**  
```bash
# Find a user’s Facebook ID
curl -s "https://graph.facebook.com/username?access_token=YOUR_ACCESS_TOKEN"
```
```bash
# Find Facebook pages associated with an email
google "site:facebook.com intext:'email@example.com'"
```
```bash
# Extract all friends of a target (if public)
google "site:facebook.com intext:'Friends' username"
```
```bash
# Get public posts mentioning a keyword
google "site:facebook.com/public keyword"
```
```bash
# Search for Facebook profiles linked to a phone number
google "site:facebook.com intext:'+1234567890'"
```

---

## **Instagram OSINT**  
```bash
# Find Instagram accounts linked to an email
google "site:instagram.com intext:email@example.com"
```
```bash
# Search for Instagram users by location
google "site:instagram.com intext:'📍 Location'"
```
```bash
# Extract all captions from an Instagram profile
instaloader --comments --metadata-json profile_username
```
```bash
# Get all Instagram stories from a public account
instaloader --stories username
```
```bash
# Extract all tagged photos of a user
google "site:instagram.com inurl:tags username"
```

---

## **LinkedIn OSINT**  
```bash
# Find all employees of a company
theHarvester -d company.com -b linkedin
```
```bash
# Extract LinkedIn profile email from commits
git log --pretty=format:"%ae" | sort -u
```
```bash
# Search for LinkedIn users by job title
google "site:linkedin.com/in 'Cybersecurity Researcher' 'India'"
```
```bash
# Extract all skills listed on a LinkedIn profile
google "site:linkedin.com/in username 'Skills'"
```
```bash
# Search for LinkedIn profiles linked to a phone number
google "site:linkedin.com/in intext:'+1234567890'"
```

---

## **YouTube OSINT**  
```bash
# Find all videos uploaded by a user
google "site:youtube.com/c/username"
```
```bash
# Extract metadata from a YouTube video
yt-dlp -J "https://www.youtube.com/watch?v=VIDEO_ID"
```
```bash
# Search for YouTube comments mentioning a keyword
google "site:youtube.com 'keyword' 'comments'"
```
```bash
# Download all subtitles from a YouTube channel
yt-dlp --write-auto-sub --sub-lang en --skip-download "https://www.youtube.com/c/username"
```

---

## **TikTok OSINT**  
```bash
# Scrape TikTok videos from a user
tiktok-scraper user username -n 50 -d
```
```bash
# Find TikTok videos based on geolocation
google "site:tiktok.com intext:'📍 New York'"
```
```bash
# Extract TikTok user bio information
tiktok-scraper user username -d --store
```

---

## **Reddit OSINT**  
```bash
# Search for deleted Reddit posts
google "site:removeddit.com user username"
```
```bash
# Find Reddit users discussing a keyword
google "site:reddit.com 'keyword' 'thread'"
```
```bash
# Extract all posts made by a Reddit user
reddit-scraper -s "username"
```
```bash
# Find Reddit users who commented on a specific post
google "site:reddit.com inurl:comments 'keyword'"
```

---

## **GitHub OSINT**  
```bash
# Search for exposed API keys in GitHub
google "site:github.com intext:'AWS_SECRET_ACCESS_KEY'"
```
```bash
# Find GitHub repositories linked to an email
google "site:github.com intext:'email@example.com'"
```
```bash
# Extract GitHub commits mentioning a keyword
github-search "keyword"
```
```bash
# Search for leaked credentials in GitHub
google "site:github.com intext:'password='"
```

---

## **Telegram OSINT**  
```bash
# Search for Telegram groups related to a topic
google "site:t.me keyword"
```
```bash
# Extract messages from a public Telegram group
telegram-history-dump -c "https://t.me/group_name"
```

---

## **WhatsApp OSINT**  
```bash
# Find public WhatsApp groups
google "site:chat.whatsapp.com keyword"
```
```bash
# Check if a phone number is linked to WhatsApp
curl -s "https://api.whatsapp.com/send?phone=+1234567890"
```

---

## **Advanced OSINT Tricks**
```bash
# Reverse search social media profile pictures
google "site:tineye.com inurl:result image.jpg"
```
```bash
# Find data leaks related to an email
dehashed -q email@example.com
```
```bash
# Extract EXIF metadata from social media images
exiftool image.jpg
```

---


## **General Social Media Search:**  
```bash
# Search for a username across multiple social media platforms
curl -s "https://usersearch.org/?q=username" | grep -Eo 'https://[a-zA-Z0-9./?=_-]+'
```
```bash
# Check if a username exists on multiple sites using Sherlock
python3 sherlock username
```

## **Twitter (X) OSINT:**  
```bash
# Search for tweets from a specific user containing a keyword
curl -s "https://nitter.net/username/search?q=keyword"
```
```bash
# Find all images posted by a Twitter user
twint -u username --media
```
```bash
# Search for email addresses in tweets
twint -s "@gmail.com OR @yahoo.com OR @protonmail.com" --output emails.txt --csv
```

## **Facebook OSINT:**  
```bash
# Search for a Facebook profile by name
google "site:facebook.com inurl:profile Name"
```
```bash
# Find Facebook posts mentioning a keyword
google "site:facebook.com/posts keyword"
```

## **Instagram OSINT:**  
```bash
# Extract Instagram user information
instaloader --login your_username profile_username
```
```bash
# Find all tagged photos of a user
google "site:instagram.com/tagged/ username"
```

## **LinkedIn OSINT:**  
```bash
# Search for employees of a company
google "site:linkedin.com/in company name"
```
```bash
# Extract LinkedIn profile data
python3 linkedin2username.py -u "Company Name"
```

## **Reddit OSINT:**  
```bash
# Search for a Reddit user’s posts
google "site:reddit.com/user/username"
```
```bash
# Find comments from a user
curl -s "https://www.reddit.com/user/username/comments.json"
```

## **YouTube OSINT:**  
```bash
# Find all videos uploaded by a user
google "site:youtube.com/user OR site:youtube.com/channel username"
```
```bash
# Extract YouTube video metadata
yt-dlp --get-title --get-id --get-description --get-duration --get-upload-date "https://www.youtube.com/watch?v=VIDEO_ID"
```

## **TikTok OSINT:**  
```bash
# Search for a TikTok user's profile
google "site:tiktok.com/@username"
```
```bash
# Extract TikTok videos and metadata
tiktok-scraper user username -n 50 -d
```

## **Snapchat OSINT:**  
```bash
# Find public Snapchat stories
google "site:map.snapchat.com username"
```
```bash
# Search for Snapchat users by name
google "site:snapchat.com add username"
```

## **Pinterest OSINT:**  
```bash
# Find all Pinterest boards of a user
google "site:pinterest.com/username"
```
```bash
# Search for pins related to a keyword
google "site:pinterest.com/pin/ keyword"
```

## **GitHub OSINT:**  
```bash
# Search for sensitive data in a user's GitHub repo
google "site:github.com username password OR api_key OR token"
```
```bash
# Find email addresses in GitHub commits
git log --pretty=format:"%ae" | sort -u
```

## **Telegram OSINT:**  
```bash
# Find Telegram groups related to a keyword
google "site:t.me keyword"
```
```bash
# Check if a Telegram username exists
curl -s "https://t.me/username"
```

## **Discord OSINT:**  
```bash
# Find Discord servers related to a keyword
google "site:discord.gg keyword"
```
```bash
# Search for Discord user profiles
google "site:discord.com users username"
```

## **WhatsApp OSINT:**  
```bash
# Search for public WhatsApp groups
google "site:chat.whatsapp.com keyword"
```
```bash
# Check if a phone number has a WhatsApp account
curl -s "https://api.whatsapp.com/send?phone=+1234567890"
```

## **General OSINT Tools for Social Media:**  
```bash
# Find all social media profiles of a user
holehe username@example.com
```
```bash
# Check username availability on multiple sites
python3 maigret username
```
```bash
# Extract metadata from an image (EXIF data)
exiftool image.jpg
```

---

# OSINT One-Liners for People Search & Email Investigation

## People Search

- **Find social media profiles using name & location:**  
  ```bash
  site:facebook.com "John Doe" "New York"
  ```
- **Search for a username across multiple sites:**  
  ```bash
  curl -s https://usersearch.org/?q=username | grep -oP 'https?://\S+'
  ```
- **Check if a username exists on social networks (Sherlock):**  
  ```bash
  python3 sherlock username
  ```
- **Google dork for public records:**  
  ```bash
  "John Doe" site:whitepages.com OR site:spokeo.com OR site:intelius.com
  ```
- **Find someone’s name linked to a phone number:**  
  ```bash
  site:truepeoplesearch.com "123-456-7890"
  ```

## Email Investigation

- **Check if an email is in a data breach (Have I Been Pwned API):**  
  ```bash
  curl -s "https://haveibeenpwned.com/api/v3/breachedaccount/test@example.com" -H "hibp-api-key: YOUR_API_KEY"
  ```
- **Find email format for a company:**  
  ```bash
  hunter.io "example.com"
  ```
- **Reverse lookup email to find associated accounts:**  
  ```bash
  site:linkedin.com intext:"test@example.com"
  ```
- **Search for email leaks using Google dorks:**  
  ```bash
  "test@example.com" filetype:txt OR filetype:csv OR filetype:log
  ```
- **Check email reputation (MXToolbox):**  
  ```bash
  curl -s "https://mxtoolbox.com/SuperTool.aspx?action=blacklist:test@example.com"
  ```



- **Find someone's old accounts via Wayback Machine:**  
  ```bash
  curl -s "http://web.archive.org/cdx/search/cdx?url=facebook.com/johndoe*&output=text&fl=original"
  ```  
- **Get full details of a phone number (Numverify API):**  
  ```bash
  curl -s "http://apilayer.net/api/validate?access_key=YOUR_API_KEY&number=+11234567890"
  ```  
- **Find all images of a person using face recognition (PimEyes):**  
  ```bash
  site:pimeyes.com "John Doe"
  ```  
- **Locate someone's forum activity using email hash (Gravatar):**  
  ```bash
  curl -s "https://en.gravatar.com/avatar/$(echo -n 'test@example.com' | md5sum | awk '{print $1}')"
  ```  
- **Find a person's connections & mentions on the web:**  
  ```bash
  site:about.me OR site:angel.co OR site:medium.com "John Doe"
  ```  
- **Reverse image search a profile picture (Google Images):**  
  ```bash
  curl -F "encoded_image=@profile.jpg" https://www.google.com/searchbyimage/upload
  ```

---

## Email Investigation

- **Find email aliases used by a person:**  
  ```bash
  site:pastebin.com OR site:throwawaymail.com "JohnDoe@example.com"
  ```  
- **Find an email in GitHub repositories:**  
  ```bash
  site:github.com "JohnDoe@example.com"
  ```  
- **Search for breached email data (Dehashed API):**  
  ```bash
  curl -u "user:password" -X GET "https://api.dehashed.com/search?query=test@example.com"
  ```  
- **Check SPF, DKIM, and DMARC records for an email domain:**  
  ```bash
  dig TXT example.com | grep "spf"
  ```
  ```bash
  dig TXT _dmarc.example.com | grep "v=DMARC1"
  ```
- **Find subdomains linked to an email provider (for company investigation):**  
  ```bash
  amass enum -d example.com
  ```
- **Extract emails from a webpage using regex (wget & grep):**  
  ```bash
  wget -qO- "https://example.com" | grep -E -o "[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}"
  ```  
- **Generate possible email variations for a person:**  
  ```bash
  echo "John Doe" | awk '{print tolower($1$2"@example.com"), tolower($1"."$2"@example.com"), tolower(substr($1,1,1)$2"@example.com")}'
  ```

---


## Advanced People Search  
- **Find hidden social media profiles using Google dorks:**  
  ```bash
  site:instagram.com | site:tiktok.com | site:twitter.com "John Doe" "New York"
  ```
- **Find someone's aliases, old usernames, and accounts:**  
  ```bash
  site:usernamecheck.com OR site:checkusernames.com "JohnDoe"
  ```
- **Check if a phone number is linked to an online account (PhoneInfoga):**  
  ```bash
  phoneinfoga scan -n "+11234567890"
  ```
- **Check for leaked personal details on public databases:**  
  ```bash
  site:publicrecords.directory "John Doe" "Los Angeles"
  ```
- **Find associated domains with a name or business:**  
  ```bash
  curl -s "https://crt.sh/?q=%25example.com&output=json" | jq .
  ```
- **Reverse lookup a street address to find past owners:**  
  ```bash
  site:rehold.com OR site:spokeo.com OR site:truthfinder.com "123 Main St, NY"
  ```
- **Find images linked to a name (Google Reverse Image):**  
  ```bash
  site:images.google.com "John Doe"
  ```

---

## Advanced Email Investigation  
- **Extract emails from a website recursively:**  
  ```bash
  theharvester -d example.com -l 100 -b google
  ```
- **Find all mentions of an email in forum posts:**  
  ```bash
  site:reddit.com OR site:quora.com "test@example.com"
  ```
- **Search for email leaks in plaintext files:**  
  ```bash
  "test@example.com" ext:txt OR ext:csv OR ext:log OR ext:sql
  ```
- **Find old email addresses linked to a domain:**  
  ```bash
  curl -s "http://web.archive.org/cdx/search/cdx?url=example.com&fl=original"
  ```
- **Find the social media accounts linked to an email:**  
  ```bash
  holehe test@example.com
  ```
- **Check if an email is linked to a PayPal account:**  
  ```bash
  curl -s -X POST -d "cmd=_notify-validate&receiver_email=test@example.com" https://www.paypal.com/cgi-bin/webscr
  ```
- **Generate potential email variations for a target:**  
  ```bash
  echo "John Doe" | awk '{print tolower($1$2"@example.com"), tolower($1"."$2"@example.com"), tolower(substr($1,1,1)$2"@example.com")}'
  ```
- **Check SPF, DKIM, and DMARC for an email domain:**  
  ```bash
  nslookup -q=TXT example.com
  ```
- **Check if an email is being used in spam campaigns (Spamhaus API):**  
  ```bash
  curl -s "https://check.spamhaus.org/test@example.com"
  ```


- **Find an old username linked to a person via Pastebin dumps:**  
  ```bash
  site:pastebin.com "John Doe" OR "johndoe123"
  ```
- **Find hidden profiles & associated links using WHOIS history:**  
  ```bash
  curl -s "https://whois-history.whoisxmlapi.com/api/v1?apiKey=YOUR_API_KEY&domainName=example.com"
  ```
- **Discover someone’s political donations (USA only):**  
  ```bash
  site:fec.gov "John Doe" "New York"
  ```
- **Check court records, arrest logs & criminal history:**  
  ```bash
  site:unicourt.com OR site:pacer.gov OR site:arrestfacts.com "John Doe"
  ```
- **Find if a person has been involved in a lawsuit:**  
  ```bash
  site:justia.com "John Doe" lawsuit OR defendant OR plaintiff
  ```
- **Reverse search job applications & résumés online:**  
  ```bash
  site:linkedin.com/in OR site:indeed.com "John Doe" "resume"
  ```
- **Find possible relatives or family members linked to a person:**  
  ```bash
  site:familytreenow.com "John Doe" "New York"
  ```
- **Get personal details leaked in public government databases:**  
  ```bash
  site:data.gov "John Doe" OR "123-45-6789"
  ```

## Email Investigation - Advanced Tactics  
- **Find websites & domains registered with an email:**  
  ```bash
  curl -s "https://www.whoxy.com/?whois=test@example.com"
  ```
- **Find hidden email leaks in public FTP servers:**  
  ```bash
  intitle:"index of" "test@example.com" ext:txt | ext:csv | ext:sql
  ```
- **Check if an email is linked to an Apple ID:**  
  ```bash
  curl -X POST "https://iforgot.apple.com/password/verify/appleid" -d "id=test@example.com"
  ```
- **Find metadata in email headers (SPF, DKIM, DMARC validation):**  
  ```bash
  exiftool email.eml
  ```
- **Check for compromised accounts in combo lists:**  
  ```bash
  grep -i "test@example.com" breached-database.txt
  ```
- **Extract all emails from a PDF file:**  
  ```bash
  pdfgrep -o "[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}" file.pdf
  ```
- **Find email-associated subdomains via DNS:**  
  ```bash
  subfinder -d example.com
  ```
- **Check if an email is linked to cryptocurrency wallets:**  
  ```bash
  site:blockchain.com OR site:etherscan.io "test@example.com"
  ```
- **Find disposable or temporary emails linked to a person:**  
  ```bash
  site:temp-mail.org OR site:10minutemail.com OR site:mailfo.pages.dev "test@example.com"
  ```
- **Check for SMTP open relay on an email server:**  
  ```bash
  swaks --to test@example.com --server mail.example.com --data "Subject: Test"
  ```


- **Check if a person’s phone number is in a spam database:**  
  ```bash
  curl -s "https://api.callinsider.com/v1/search?number=+11234567890&apikey=YOUR_API_KEY"
  ```
- **Find deleted social media posts (cached Google & Bing results):**  
  ```bash
  cache:twitter.com/johndoe OR cache:facebook.com/johndoe
  ```
- **Search for user profiles in data breaches:**  
  ```bash
  site:haveibeenpwned.com "John Doe" OR "test@example.com"
  ```
- **Find out if someone has a Medium or Substack account:**  
  ```bash
  site:medium.com OR site:substack.com "John Doe"
  ```
- **Check for public Amazon wishlists linked to a name:**  
  ```bash
  site:amazon.com "John Doe" wishlist
  ```
- **Search property ownership records (USA only):**  
  ```bash
  site:realtor.com OR site:zillow.com "123 Main St, NY"
  ```
- **Check past travel history via flight logs (Private Jet owners):**  
  ```bash
  site:flightaware.com OR site:flightradar24.com "John Doe"
  ```
- **Look for someone's online dating profiles (Tinder, Bumble, etc.):**  
  ```bash
  site:tinder.com OR site:bumble.com "John Doe"
  ```
- **Find a person's reviews on websites (Amazon, Yelp, TrustPilot):**  
  ```bash
  site:amazon.com OR site:yelp.com OR site:trustpilot.com "John Doe"
  ```
- **Check if a person has been mentioned in news articles:**  
  ```bash
  site:bbc.com OR site:cnn.com OR site:forbes.com "John Doe"
  ```

## Email Investigation - Pro Level

- **Find alternate emails linked to a domain using Hunter.io:**  
  ```bash
  curl -s "https://api.hunter.io/v2/domain-search?domain=example.com&api_key=YOUR_API_KEY"
  ```
- **Extract email addresses from a CSV file:**  
  ```bash
  awk -F, '{print $2}' emails.csv | grep -E -o "[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}"
  ```
- **Check if an email is linked to a Steam account:**  
  ```bash
  curl -s "https://steamcommunity.com/actions/WhoIsOnline/test@example.com"
  ```
- **Search old forum posts linked to an email (4chan, Reddit, etc.):**  
  ```bash
  site:4chan.org OR site:reddit.com "test@example.com"
  ```
- **Find if an email is listed in PGP key databases:**  
  ```bash
  gpg --search-keys test@example.com
  ```
- **Extract emails from a Word document (.docx):**  
  ```bash
  strings file.docx | grep -E -o "[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}"
  ```
- **Find subdomains linked to an email provider:**  
  ```bash
  amass enum -d example.com
  ```
- **Check if an email is used in crypto forums (BitcoinTalk, etc.):**  
  ```bash
  site:bitcointalk.org "test@example.com"
  ```
- **Check if an email is linked to a Patreon account:**  
  ```bash
  site:patreon.com "test@example.com"
  ```
- **Verify if an email has been involved in fraud cases:**  
  ```bash
  site:ripoffreport.com OR site:scamwarners.com "test@example.com"
  ```

- **Find a person’s past usernames across multiple platforms:**  
  ```bash
  site:namemc.com OR site:usersearch.org OR site:instantusername.com "JohnDoe"
  ```
- **Check if a person is registered on genealogy websites:**  
  ```bash
  site:ancestry.com OR site:familysearch.org OR site:genealogy.com "John Doe"
  ```
- **Look up past marriages & divorces (US only):**  
  ```bash
  site:divorcerecords.org OR site:marriagerecords.com "John Doe"
  ```
- **Check public campaign donations (US politicians & donors):**  
  ```bash
  site:opensecrets.org OR site:fec.gov "John Doe"
  ```
- **Find someone’s car registration details (some countries):**  
  ```bash
  site:vehiclehistory.com OR site:carfax.com "John Doe"
  ```
- **Search for hidden YouTube channels linked to a person:**  
  ```bash
  site:youtube.com "John Doe"
  ```
- **Find someone’s frequently used locations via check-ins:**  
  ```bash
  site:foursquare.com OR site:swarmapp.com "John Doe"
  ```
- **Look up private business records or LLC registrations:**  
  ```bash
  site:opencorporates.com "John Doe" OR "Doe Enterprises"
  ```
- **Check if a person has published academic papers or research:**  
  ```bash
  site:researchgate.net OR site:academia.edu "John Doe"
  ```
- **Find an author’s books, blog posts, or past writings:**  
  ```bash
  site:goodreads.com OR site:medium.com OR site:substack.com "John Doe"
  ```

## 📧 Email Investigation - Next Level Tactics

- **Check if an email is linked to a Facebook account:**  
  ```bash
  curl -X POST -d "email=test@example.com" https://www.facebook.com/login/identify
  ```
- **Find if an email is mentioned in Telegram groups:**  
  ```bash
  site:t.me OR site:telegram.me "test@example.com"
  ```
- **Look up emails linked to an IP address using AbuseIPDB:**  
  ```bash
  curl -s "https://api.abuseipdb.com/api/v2/check?ipAddress=1.2.3.4&apiKey=YOUR_API_KEY"
  ```
- **Extract email addresses from HTML source code of a website:**  
  ```bash
  curl -s "http://example.com" | grep -oP '[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}'
  ```
- **Find all emails ever used on a specific website:**  
  ```bash
  site:example.com "email"
  ```
- **Search for past email leaks using HIBP API:**  
  ```bash
  curl -s "https://haveibeenpwned.com/api/v2/breachedaccount/test@example.com"
  ```
- **Generate common email permutations for OSINT scanning:**  
  ```bash
  python3 EmailPermutator.py -n "John Doe" -d example.com
  ```
- **Check if an email is linked to a Zoom account:**  
  ```bash
  curl -X POST "https://zoom.us/signup" -d "email=test@example.com"
  ```
- **Find if an email is associated with a LinkedIn account:**  
  ```bash
  curl -X POST "https://www.linkedin.com/checkpoint/lg/login-submit" -d "session_key=test@example.com"
  ```
- **Discover if an email is linked to an Instagram account:**  
  ```bash
  curl -X POST "https://www.instagram.com/accounts/account_recovery_send_ajax/" -d "email_or_username=test@example.com"
  ```


### **Twitter (X) Advanced OSINT**
```bash
# Extract tweets, likes, and followers via API
twint -u username --followers --following --tweets
```
```bash
# Search for leaked credentials in tweets  
twint -s "password OR API_KEY OR AWS_SECRET_ACCESS_KEY"
```
```bash
# Extract Twitter followers without rate limits
twint -u username --followers --csv -o followers.csv
```
```bash
# Find accounts linked to a phone number  
twint -s "+1234567890"
```
```bash
# Monitor target’s tweets in real-time
twint -u username --rt
```
```bash
# Find tweets with geotagged locations  
twint -s "keyword" --near "New York"
```

---

### **Facebook Advanced OSINT**
```bash
# Find all Facebook groups a user is in  
google "site:facebook.com/groups username"
```
```bash
# Extract hidden friends list from a Facebook profile  
curl -s "https://graph.facebook.com/v14.0/username/friends?access_token=YOUR_ACCESS_TOKEN"
```
```bash
# Scrape Facebook public posts by a user  
facebook-scraper username --posts
```
```bash
# Search for leaked Facebook IDs in breaches  
google "site:pastebin.com facebook.com/profile.php?id="
```
```bash
# Find Facebook posts from a specific location  
google "site:facebook.com intext:'📍 New York'"
```

---

### **Instagram Advanced OSINT**
```bash
# Download all Instagram stories from a target  
instaloader --stories username
```
```bash
# Extract Instagram metadata (location, device info, etc.)  
instaloader --metadata-json username
```
```bash
# Find all Instagram profiles linked to an email  
google "site:instagram.com intext:email@example.com"
```
```bash
# Extract geotagged Instagram posts  
google "site:instagram.com intext:'📍 London'"
```
```bash
# Find Instagram users with similar interests  
google "site:instagram.com intext:'#hacking #cybersecurity'"
```

---

### **LinkedIn Advanced OSINT**
```bash
# Scrape all employees from a company  
linkedin-scraper -c "Google"
```
```bash
# Extract job postings and hidden email contacts  
google "site:linkedin.com/jobs 'Cybersecurity Analyst' 'Remote'"
```
```bash
# Find LinkedIn profiles with leaked credentials  
google "site:linkedin.com/in 'password' OR 'email@example.com'"
```
```bash
# Identify LinkedIn users who worked for a company in the past  
google "site:linkedin.com/in 'Worked at Google'"
```
```bash
# Find LinkedIn profiles linked to an IP address  
shodan search "org:'LinkedIn Corp'"
```

---

### **YouTube Advanced OSINT**
```bash
# Download metadata from a YouTube channel  
yt-dlp -J "https://www.youtube.com/c/username"
```
```bash
# Extract subtitles and hidden keywords from videos  
yt-dlp --write-auto-sub --skip-download "https://www.youtube.com/watch?v=VIDEO_ID"
```
```bash
# Find YouTube videos from a specific geolocation  
google "site:youtube.com intext:'📍 New York'"
```
```bash
# Extract YouTube video analytics & insights  
google "site:socialblade.com youtube username"
```
```bash
# Find deleted YouTube videos  
google "site:archive.org youtube.com/watch?v="
```

---

## **Extra OSINT Techniques**
```bash
# Reverse search social media profile pictures  
google "site:tineye.com inurl:result image.jpg"
```
```bash
# Find deep-web social media leaks  
google "site:pastebin.com OR site:ghostbin.com 'email@example.com'"
```
```bash
# Extract hidden metadata from social media images  
exiftool image.jpg
```
```bash
# Search for hidden social media accounts using an IP  
shodan search "ip:xxx.xxx.xxx.xxx"
```


## **General Social Media OSINT**
```bash
# Find accounts linked to an email or phone
whatsmyname -u email@example.com
```
```bash
# Check username presence across 500+ platforms
python3 sherlock username
```
```bash
# Scrape all social media links from a website
python3 photon.py -u example.com
```
```bash
# Identify hidden social media accounts of a target
theHarvester -d target.com -b all
```
```bash
# Check for social media accounts linked to an IP
shodan search "org:'Target ISP' http.title:'Login'"
```

---

## **Twitter (X) OSINT**  
```bash
# Get all tweets from a specific time range
twint -u username --since 2024-01-01 --until 2024-03-01
```
```bash
# Extract user email from tweets (if leaked)
twint -u username --email
```
```bash
# Find accounts created in a specific year
twint --year 2010
```
```bash
# Get tweets containing geolocation data
twint -u username --geocode
```
```bash
# Identify all hashtags used by a user
twint -u username --hashtags
```
```bash
# Extract all retweets of a specific user
twint -u username --retweets
```

---

## **Facebook OSINT**  
```bash
# Find a user’s Facebook ID
curl -s "https://graph.facebook.com/username?access_token=YOUR_ACCESS_TOKEN"
```
```bash
# Find Facebook pages associated with an email
google "site:facebook.com intext:'email@example.com'"
```
```bash
# Extract all friends of a target (if public)
google "site:facebook.com intext:'Friends' username"
```
```bash
# Get public posts mentioning a keyword
google "site:facebook.com/public keyword"
```
```bash
# Search for Facebook profiles linked to a phone number
google "site:facebook.com intext:'+1234567890'"
```

---

## **Instagram OSINT**  
```bash
# Find Instagram accounts linked to an email
google "site:instagram.com intext:email@example.com"
```
```bash
# Search for Instagram users by location
google "site:instagram.com intext:'📍 Location'"
```
```bash
# Extract all captions from an Instagram profile
instaloader --comments --metadata-json profile_username
```
```bash
# Get all Instagram stories from a public account
instaloader --stories username
```
```bash
# Extract all tagged photos of a user
google "site:instagram.com inurl:tags username"
```

---

## **LinkedIn OSINT**  
```bash
# Find all employees of a company
theHarvester -d company.com -b linkedin
```
```bash
# Extract LinkedIn profile email from commits
git log --pretty=format:"%ae" | sort -u
```
```bash
# Search for LinkedIn users by job title
google "site:linkedin.com/in 'Cybersecurity Researcher' 'India'"
```
```bash
# Extract all skills listed on a LinkedIn profile
google "site:linkedin.com/in username 'Skills'"
```
```bash
# Search for LinkedIn profiles linked to a phone number
google "site:linkedin.com/in intext:'+1234567890'"
```

---

## **YouTube OSINT**  
```bash
# Find all videos uploaded by a user
google "site:youtube.com/c/username"
```
```bash
# Extract metadata from a YouTube video
yt-dlp -J "https://www.youtube.com/watch?v=VIDEO_ID"
```
```bash
# Search for YouTube comments mentioning a keyword
google "site:youtube.com 'keyword' 'comments'"
```
```bash
# Download all subtitles from a YouTube channel
yt-dlp --write-auto-sub --sub-lang en --skip-download "https://www.youtube.com/c/username"
```

---

## **TikTok OSINT**  
```bash
# Scrape TikTok videos from a user
tiktok-scraper user username -n 50 -d
```
```bash
# Find TikTok videos based on geolocation
google "site:tiktok.com intext:'📍 New York'"
```
```bash
# Extract TikTok user bio information
tiktok-scraper user username -d --store
```

---

## **WhatsApp OSINT**  
```bash
# Find public WhatsApp groups
google "site:chat.whatsapp.com keyword"
```
```bash
# Check if a phone number is linked to WhatsApp
curl -s "https://api.whatsapp.com/send?phone=+1234567890"
```

---

## **Advanced OSINT Tricks**  
```bash
# Reverse search social media profile pictures
google "site:tineye.com inurl:result image.jpg"
```
```bash
# Find data leaks related to an email
dehashed -q email@example.com
```
```bash
# Extract EXIF metadata from social media images
exiftool image.jpg
```
```bash
# Search for hidden social media accounts using an IP
shodan search "ip:xxx.xxx.xxx.xxx"
```

## **Extract Geolocation from Metadata**  

🔹 **Check image metadata for GPS coordinates**  
```bash
exiftool image.jpg | grep -i "GPS"
```

🔹 **Extract metadata from videos (if available)**  
```bash
ffmpeg -i video.mp4 -f ffmetadata metadata.txt
```

🔹 **Check metadata of PDFs for location info**  
```bash
pdfinfo file.pdf
```

---

## **IP Geolocation**  

🔹 **Find location from an IP address**  
```bash
curl -s "http://ip-api.com/json/8.8.8.8"
```

🔹 **More detailed IP location data (including ISP & ASN)**  
```bash
curl -s "https://ipinfo.io/8.8.8.8/json"
```

🔹 **Check IP geolocation with MaxMind**  
```bash
geoiplookup 8.8.8.8
```

🔹 **Get approximate IP location from Shodan**  
```bash
shodan host 8.8.8.8
```

---

## **Reverse Geocoding & Mapping**  

🔹 **Find address from GPS coordinates**  
```bash
curl -s "https://nominatim.openstreetmap.org/reverse?format=json&lat=40.748817&lon=-73.985428"
```

🔹 **Find nearby locations using OpenStreetMap**  
```bash
curl -s "https://nominatim.openstreetmap.org/search?q=Eiffel+Tower&format=json"
```

🔹 **Search places via Google Maps API**  
```bash
curl -s "https://maps.googleapis.com/maps/api/geocode/json?address=Eiffel+Tower&key=YOUR_API_KEY"
```

🔹 **Find historical satellite images**  
```bash
https://livingatlas.arcgis.com/wayback/
```

---

## **Wi-Fi, Bluetooth, & Mobile Data OSINT**  

🔹 **Find location from Wi-Fi BSSID (if known)**  
```bash
curl "https://wigle.net/api/v2/network/search?netid=XX:XX:XX:XX:XX:XX"
```

🔹 **Check if a Wi-Fi SSID has been mapped**  
```bash
curl -s "https://api.mylnikov.org/geolocation/wifi?v=1.1&bssid=XX:XX:XX:XX:XX:XX"
```

🔹 **Check Bluetooth device locations (if tracked)**  
```bash
https://www.bluetooth.com/specifications/assigned-numbers/company-identifiers/
```

🔹 **Check cell tower geolocation (for mobile tracking)**  
```bash
curl -s "https://opencellid.org/cell/get?mcc=310&mnc=410&lac=7033&cellid=17811&key=YOUR_API_KEY"
```

---

## **Social Media Geolocation OSINT**  

🔹 **Find location from Instagram post (if geotagged)**  
```bash
https://www.instagram.com/p/POST_ID/
```

🔹 **Find location from Twitter post (if enabled)**  
```bash
https://twitter.com/username/status/POST_ID
```

🔹 **Extract location from Facebook check-ins**  
```bash
https://www.facebook.com/search/places/?q=locationname
```

🔹 **Reverse search a Snapchat map story**  
```bash
https://map.snapchat.com/
```

---

## **Vehicle & Transport Tracking**  

🔹 **Track Uber/Lyft rides (if shared link available)**  
```bash
https://www.uber.com/track/TRACKING_CODE
```

🔹 **Look up a car’s geotagged photos (if available)**  
```bash
https://www.instagram.com/explore/tags/carnumberplate/
```

🔹 **Find ship locations (via AIS data)**  
```bash
https://www.marinetraffic.com/
```

🔹 **Find aircraft locations (real-time flight tracking)**  
```bash
https://www.flightradar24.com/
```

---

## **Satellite & Aerial OSINT**  

🔹 **View live satellite imagery (if available)**  
```bash
https://www.planet.com/explorer/
```

🔹 **Search for satellite images from past years**  
```bash
https://eos.com/landviewer/
```

🔹 **NASA Earth data for environmental tracking**  
```bash
https://earthdata.nasa.gov/
```

**Extract GPS from images (Exif metadata)**  
```bash
exiftool image.jpg | grep -E "GPS Latitude|GPS Longitude"
```

**Reverse image search location (Google)**  
```bash
curl -F 'encoded_image=@image.jpg' https://www.google.com/searchbyimage
```

**Find location from Wi-Fi BSSID**  
```bash
curl "https://wigle.net/api/v2/network/search?netid=XX:XX:XX:XX:XX:XX"
```

**Find location from an IP address**  
```bash
curl -s "http://ip-api.com/json/IP_ADDRESS"
```

**Get geolocation from phone number**  
```bash
python3 phoneinfoga.py -n +1234567890
```

**Check Google Maps Timeline (if accessible)**  
```bash
https://www.google.com/maps/timeline
```

**Get satellite images of a location**  
```bash
https://www.google.com/maps/place/lat,long
```

**Reverse Geocode Coordinates**  
```bash
curl -s "https://nominatim.openstreetmap.org/reverse?format=json&lat=LAT&lon=LON"
```

**Track Uber/Lyft ride details (if link available)**  
```bash
https://www.uber.com/track/XXXXXXXX
```

**Find location from social media posts**  
```bash
https://maps.google.com/?q=LAT,LON
```


```bash
# Search for keywords on Ahmia (Tor Search Engine)
torify curl -s "https://ahmia.fi/search/?q=your_keyword"

# Search on OnionLand (Dark Web Search Engine)
torify curl -s "https://onionlandsearchengine.com/search?q=your_keyword"

# Extract all .onion links from a webpage
torify curl -s "http://example.onion" | grep -oP '(?<=href=")http://[^"]+\.onion'

# Find indexed .onion sites on DuckDuckGo
torify curl -s "https://www.duckduckgo.com/html?q=site:onion your_keyword"

# Check if a dark web site is online
torify curl -Is http://example.onion | head -n 1
```

## **Paste Sites OSINT One-Liners**
```bash
# Search for leaked credentials on Pastebin
curl -s "https://www.google.com/search?q=site:pastebin.com your_keyword"

# Scrape Pastebin for recent pastes (requires API key)
curl -s "https://scrape.pastebin.com/api_scraping.php?limit=10"

# Check for mentions of an email in recent pastes
curl -s "https://www.google.com/search?q=site:pastebin.com your_email@example.com"

# Find pastes mentioning a specific domain
curl -s "https://www.google.com/search?q=site:pastebin.com yourdomain.com"

# Check for leaked credentials using DeHashed (API required)
curl -s "https://api.dehashed.com/search?query=email@example.com" -u "your_api_key"
```

---

### U.S. FOIA Request Guide (How to Request Public Records)
```bash
curl -s "https://www.foia.gov/how-to.html"
```
### U.S. State-Level FOIA Directories
```bash
curl -s "https://www.nfoic.org/coalitions/state-foi-resources/"
```
### UK Freedom of Information (FOI) Requests
```bash
curl -s "https://www.whatdotheyknow.com/"
```
### EU Public Documents & Transparency Database
```bash
curl -s "https://www.asktheeu.org/en/request/new"
```

## Law Enforcement & Criminal Records

### U.S. Department of Justice Press Releases (Cases & Convictions)
```bash
curl -s "https://www.justice.gov/news?q=John+Doe"
```
### Interpol Stolen Works of Art Database
```bash
curl -s "https://www.interpol.int/en/Crimes/Cultural-heritage-crime/Stolen-Works-of-Art-Database"
```
### U.S. Most Wanted by State
```bash
curl -s "https://www.usmarshals.gov/investigations/most_wanted/state.htm?q=Texas"
```
### DEA Fugitives List
```bash
curl -s "https://www.dea.gov/fugitives?q=John+Doe"
```
### Australia Criminal Records Check (National Police Certificates)
```bash
curl -s "https://www.afp.gov.au/what-we-do/services/criminal-records"
```

## Court Cases & Judgments

### U.S. Supreme Court Case Lookup (Oyez)
```bash
curl -s "https://www.oyez.org/cases?q=John+Doe"
```
### U.S. PACER (Federal Court Case Search) - Requires Login
```bash
curl -s "https://pacer.uscourts.gov"
```
### UK Supreme Court Case Tracker
```bash
curl -s "https://www.supremecourt.uk/cases/search.html?q=John+Doe"
```
### India Court Case Search (e-Courts Portal)
```bash
curl -s "https://ecourts.gov.in/services/cases?q=John+Doe"
```
### European Court of Human Rights Cases
```bash
curl -s "https://hudoc.echr.coe.int/eng#{%22fulltext%22:[%22John+Doe%22]}"
```

## Financial, Banking & Tax Records

### U.S. Federal Reserve Enforcement Actions
```bash
curl -s "https://www.federalreserve.gov/supervisionreg/enforcement-actions.htm?q=John+Doe"
```
### U.S. IRS Exempt Organizations Search (Nonprofits, Churches, etc.)
```bash
curl -s "https://apps.irs.gov/app/eos/details/?q=NonprofitName"
```
### U.S. Office of Foreign Assets Control (OFAC) Sanctions List
```bash
curl -s "https://sanctionssearch.ofac.treas.gov/"
```
### UK HMRC Tax Evasion & Fraud Reports
```bash
curl -s "https://www.gov.uk/government/collections/hmrc-annual-reports"
```
### European Central Bank (ECB) Enforcement Actions
```bash
curl -s "https://www.bankingsupervision.europa.eu/banking/sanctions/html/index.en.html?q=John+Doe"
```

## Property & Real Estate Records

### U.S. HUD Housing Data & Records
```bash
curl -s "https://www.hud.gov/program_offices/housing/rmra/oe/rpts/mfh_f47/mf_f47?q=123+Main+Street"
```
### Canada Land Registry (Province-Specific)
```bash
curl -s "https://www.lro.gov.on.ca/en/home"
```
### UK Land & Property Sales Data
```bash
curl -s "https://landregistry.data.gov.uk/app/ppd/"
```
### Germany Real Estate Transactions (Open Data)
```bash
curl -s "https://www.govdata.de/web/guest/suchen/-/results/q/immobilien"
```

## Intelligence, Security & Military Records

### U.S. CIA FOIA Reading Room (Declassified Documents)
```bash
curl -s "https://www.cia.gov/readingroom/search/site/John+Doe"
```
### FBI Vault (Declassified Government Records)
```bash
curl -s "https://vault.fbi.gov/search?q=John+Doe"
```
### U.S. Department of Defense Contracts & Spending
```bash
curl -s "https://www.defense.gov/News/Contracts/Search?q=CompanyName"
```
### UK Ministry of Defence FOI Disclosures
```bash
curl -s "https://www.gov.uk/government/publications?departments%5B%5D=ministry-of-defence&q=John+Doe"
```
### Russia & China Government Tenders & Defense Deals
```bash
curl -s "https://www.russiancontracts.ru/"  
curl -s "https://www.chinadefense.com.cn/"
```

## People, Identity & Vital Records

### U.S. Census Bureau Public Records Search
```bash
curl -s "https://data.census.gov/cedsci/?q=John+Doe"
```
### Canada Birth, Marriage & Death Certificates (Provincial-Level)
```bash
curl -s "https://www.canada.ca/en/revenue-agency/services/tax/individuals/identification-information/change-marital-status.html"
```
### UK Births, Marriages & Deaths (GRO Index)
```bash
curl -s "https://www.gro.gov.uk/gro/content/certificates/"
```
### Australia Births, Deaths & Marriages Registry
```bash
curl -s "https://www.bdm.vic.gov.au/research-and-family-history/search-your-family-history"
```
### India Aadhaar Card Verification (Limited Public Data)
```bash
curl -s "https://uidai.gov.in/ecosystem/authentication-services.html"
```

## Miscellaneous & Hidden OSINT Gems

### U.S. FCC License Database (Find Radio Operators, Companies, etc.)
```bash
curl -s "https://wireless2.fcc.gov/UlsApp/UlsSearch/searchAdvanced.jsp?q=John+Doe"
```
### U.S. Airline & Pilot License Verification (FAA Database)
```bash
curl -s "https://www.faa.gov/licenses-certificates/airmen-inquiry?q=John+Doe"
```
### U.S. Medical License Search (Doctors & Practitioners)
```bash
curl -s "https://www.npinumberlookup.org/?q=John+Doe"
```
### UK DVLA Vehicle & License Plate Lookup (Limited Public Access)
```bash
curl -s "https://vehicleenquiry.service.gov.uk/"
```
### India RTO Vehicle Registration Check
```bash
curl -s "https://vahan.parivahan.gov.in/vahanservice/vahan/ui/statevalidation/homepage.xhtml"
```
