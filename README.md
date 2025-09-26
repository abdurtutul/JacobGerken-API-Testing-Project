# JacobGerken API Testing Project

This repository contains the API testing artifacts for the **JacobGerken** project.  
All APIs were tested using **Postman** and automated with **Newman**, with detailed reports attached.  

---

## 📌 Project Information
- **Project Name**: JacobGerken  
- **Frontend URL**: [jacobgerken-react-frontend.netlify.app](https://jacobgerken-react-frontend.netlify.app/)  
- **Figma Design**: [Figma Prototype](https://www.figma.com/design/ydW4mAIXI7MDkp4rCbjtRx/jacobgerken647-%7C%7C-WP_Monkey-%7C%7C-FO313F96566C3?node-id=5628-930&t=Buvn3lc69KEykVcY-0)  
- **Test Report (Google Sheet)**: [API Test Report](https://docs.google.com/spreadsheets/d/1gMH65etfC6vbWoAE5g6_jmdqo0asUswyUK3ggZ9e-6o/edit?usp=sharing)  

---

## 📂 Repository Structure
```
jacobgerken-api-testing/
│── reports/
│   ├── newman-auth-user-report.html           # Newman HTML report
│   └── test-report-google-sheet-link.txt      # Reference to Google Sheet
│── docs/
│   ├── figma-design-link.txt                  # Reference to Figma
│   ├── frontend-url.txt                       # Reference to frontend
│── README.md                                  # Documentation
```

---

## ✅ Modules Tested
- **Auth**
- **User**
- **Home**
  - CMS
  - Solution Page
  - Solution Section
  - Solution Icon
- **Quote**
- **Reward**
- **Team**
- **Order**
- **Contact Request**

---

## 🧪 Testing Tools
- **Postman** – API manual testing  
- **Newman** – CLI automation for Postman collections  
- **Google Sheets** – Manual test reporting  

---

## ▶️ How to Run Tests
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/jacobgerken-api-testing.git
   cd jacobgerken-api-testing
   ```

2. Install **Newman** (if not installed):
   ```bash
   npm install -g newman
   ```

3. Run the Postman collection:
   ```bash
   newman run postman/JacobGerken.postman_collection.json -e postman/JacobGerken.postman_environment.json -r html,cli --reporter-html-export reports/newman-report.html
   ```

---

## 📊 Reports
- **Manual Test Report (Google Sheet)**: [View Report](https://docs.google.com/spreadsheets/d/1gMH65etfC6vbWoAE5g6_jmdqo0asUswyUK3ggZ9e-6o/edit?usp=sharing)  
- **Newman Automation Report**: [`reports/newman-auth-user-report.html`](reports/newman-auth-user-report.html)  

---

## 📝 Demo Test Case Structure

Here’s an example of how API test cases are documented in this project:  

| Test Case ID | Module | Request Name | Endpoint   | Testing Type     | HTTP Method | Status Code | Issue Type        | Description                                                    | Expected Result                        | Actual Result    | Status   | Attachments | Remarks | Developer Comments | Re-test Date |
|--------------|--------|--------------|------------|------------------|-------------|-------------|-------------------|----------------------------------------------------------------|----------------------------------------|------------------|----------|-------------|---------|--------------------|--------------|
| **TC_ID_001** | Auth   | Register     | `/register` | Positive testing | POST        | 200 OK      | N/A               | Register with valid data (name, phone, email, password)        | Response should return **200**         | Found as expected | ✅ Passed | N/A         | N/A     | N/A                | 9/24/2025    |
| **TC_ID_002** | Auth   | Register     | `/register` | Negative testing | POST        | 200 OK      | Mail server issue | After signup successfully, OTP not sent to registered email    | OTP should be sent to registered email | OTP not received | ❌ Failed | Screenshot  | N/A     | Needs Fix          | 9/24/2025    |

---

## 🐞 Sample Bug Report Format

| Module | Feature  | Bug Type    | Bug Title        | Bug Description                           | Steps to Reproduce                                   | Actual Result         | Expected Result                 |
|--------|----------|-------------|------------------|-------------------------------------------|------------------------------------------------------|-----------------------|---------------------------------|
| Auth   | Register | Functional  | OTP not received | OTP email not sent after successful signup | 1. Register with valid details <br> 2. Check inbox   | OTP email not received | OTP email should be sent        |

---

## 👨‍💻 Contributor
**SQA Engineer**: *MD Abdur Rahaman Tutul*  

---
