# Task 11: Phishing Attack Simulation & Detection

## 📌 Objective

To simulate a phishing attack in a controlled lab environment using GoPhish, track campaign results, and understand phishing detection and prevention techniques.

---

## 🖥️ Environment Details

- Operating System: Kali Linux
- Tool Used: GoPhish v0.12.1
- SMTP Server: Gmail (App Password)
- Local Server: https://127.0.0.1:3333

---

## 🔹 Step 1: System Update

Updated the system packages before installation.

Command used:
sudo apt update
sudo apt upgrade -y

---

## 🔹 Step 2: Download GoPhish

Downloaded the latest GoPhish Linux 64-bit version from GitHub.

Command used:
wget https://github.com/gophish/gophish/releases/latest/download/gophish-v0.12.1-linux-64bit.zip

Download completed successfully (100%).

---

## 🔹 Step 3: Extract GoPhish

Extracted the downloaded ZIP file.

Command used:
unzip gophish-v0.12.1-linux-64bit.zip

Files such as:
- config.json
- templates/
- static/
were extracted successfully.

---

## 🔹 Step 4: Run GoPhish

Provided execution permission and started the GoPhish server.

Command used:
chmod +x gophish
sudo ./gophish

Terminal displayed:
- Username: admin
- Auto-generated password
- Starting admin server at https://127.0.0.1:3333

---

## 🔹 Step 5: Access Admin Panel

Opened browser and navigated to:

https://127.0.0.1:3333

Encountered SSL self-signed certificate warning.
Selected:
Advanced → Accept the Risk and Continue

Logged in using:
Username: admin  
Password: (generated in terminal)

---

## 🔹 Step 6: Create Email Template

Created a phishing email template with:

Subject:
Important: Password Reset Required

Body:
Included a link using {{.URL}} to redirect to landing page.

Template saved successfully.

---

## 🔹 Step 7: Create Landing Page

Created a fake login page containing:

- Username field
- Password field
- Submit button

Enabled:
✔ Capture Submitted Data  
✔ Capture Passwords  

Landing page saved successfully.

---

## 🔹 Step 8: Create User Group

Created a test group with one user:

First Name: Test  
Last Name: User  
Email: test@example.com  

Group added successfully.

---

## 🔹 Step 9: Configure SMTP Sending Profile

Configured Gmail SMTP settings:

SMTP Host: smtp.gmail.com  
Port: 587  
Username: Gmail address  
Password: Gmail App Password  

Initially received error:
535 5.7.8 Username and Password not accepted

Resolved by:
- Enabling 2-Step Verification
- Generating Gmail App Password
- Updating SMTP profile

Profile saved successfully.

---

## 🔹 Step 10: Send Test Email

Sent test email successfully.
Confirmation message:
Email Sent!

Verified email delivery.

---

## 🔹 Step 11: Launch Campaign

Created a new campaign using:

- Email Template
- Landing Page
- Sending Profile
- User Group

Campaign launched successfully.

---

## 🔹 Step 12: Campaign Results

Campaign results dashboard displayed:

- Email Sent: 1
- Email Opened: 0
- Clicked Link: 0
- Submitted Data: 0

Campaign tracking working correctly.

---

## 📊 Observations

- Self-signed SSL certificate warning is normal in localhost environment.
- Gmail blocks normal password authentication for SMTP.
- App Password is required for secure SMTP authentication.
- Campaign statistics provide real-time tracking.

---

## 🚩 Phishing Red Flags Identified

- Urgent language in email
- Suspicious link redirection
- Credential collection page
- Unknown sender

---

## 🛡️ Prevention Methods

- Multi-Factor Authentication (MFA)
- Email filtering systems
- User awareness training
- SPF, DKIM, DMARC implementation
- Avoid clicking unknown links

---

## 🎯 Conclusion

Successfully performed a phishing attack simulation using GoPhish in a controlled environment.

Understood:
- How phishing campaigns are created
- How credentials can be captured
- How to track campaign performance
- How to detect and prevent phishing attacks

---

## 📁 Repository Structure

README.md  
screenshots/  
    - System Update  
    - Download  
    - Unzip  
    - GoPhish Running  
    - Email Template  
    - Landing Page  
    - User Group  
    - SMTP Profile  
    - Campaign Results  

---

✅ Task Completed Successfully
