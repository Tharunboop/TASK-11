# Task 11: Phishing Attack Simulation using GoPhish

## 📌 Objective

To perform a phishing attack simulation in a controlled lab environment using GoPhish and analyze the campaign results.

---

## 🖥️ Environment Details

- OS: Kali Linux
- Tool: GoPhish v0.12.1
- SMTP: Gmail (App Password)
- Admin Panel: https://127.0.0.1:3333

---

# 🔹 Step 1: System Update

Updated system packages before installation.

Commands used:

sudo apt update  
sudo apt upgrade -y  


---

# 🔹 Step 2: Download GoPhish

Downloaded GoPhish from official GitHub release.

Command used:

wget https://github.com/gophish/gophish/releases/latest/download/gophish-v0.12.1-linux-64bit.zip



---

# 🔹 Step 3: Extract Files

Extracted the downloaded ZIP file.

Command used:

unzip gophish-v0.12.1-linux-64bit.zip

---

# 🔹 Step 4: Run GoPhish Server

Provided execution permission and started GoPhish.

Commands used:

chmod +x gophish  
sudo ./gophish  

Server started at:
https://127.0.0.1:3333  



---

# 🔹 Step 5: Access Admin Panel

Opened browser and navigated to:

https://127.0.0.1:3333  

Accepted self-signed SSL certificate warning.

Logged in using:
Username: admin  
Password: Generated in terminal  


---

# 🔹 Step 6: Create Email Template

Created phishing email template.

Subject:
Important: Password Reset Required  

Body included phishing link using:
{{.URL}}

Template saved successfully.


---

# 🔹 Step 7: Create Landing Page

Created fake login page with:

- Username field  
- Password field  
- Submit button  

Enabled:
✔ Capture Submitted Data  
✔ Capture Passwords  


---

# 🔹 Step 8: Create User Group

Created user group and added test user.

Details used:
First Name: Test  
Last Name: User  
Email: test@example.com  

---

# 🔹 Step 9: Configure SMTP Profile

Configured Gmail SMTP settings.

SMTP Host: smtp.gmail.com  
Port: 587  
Username: Gmail address  
Password: Gmail App Password  

Initially received authentication error (535).  
Resolved by generating Gmail App Password.


---

# 🔹 Step 10: Send Test Email

Sent test email successfully after SMTP configuration.

Confirmation message:
Email Sent!

---

# 🔹 Step 11: Launch Campaign

Created and launched phishing campaign using:

- Email Template  
- Landing Page  
- SMTP Profile  
- User Group  


---

# 🔹 Step 12: Campaign Results

Viewed campaign dashboard results.

Results observed:

- Email Sent: 1  
- Email Opened: 0  
- Clicked Link: 0  
- Submitted Data: 0  


---

# 🔹 Step 13: Email Delivery Verification

Verified email delivery in Gmail inbox.

Observed:

- Default Email from GoPhish  
- Phishing email content  
- Email header details  
- Bounce message for invalid domain  


---

# ✅ Task Completed

Successfully performed phishing simulation using GoPhish, configured SMTP, launched campaign, and analyzed results in a controlled lab environment.
