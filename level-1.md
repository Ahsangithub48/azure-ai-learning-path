# 🤖 Level 1: Nanobots – Beginner AI Builders

### 🎯 Objective: Create fun and functional bots without writing code
### ⏱️ Format: 30-minute guided, hands-on lessons

---

## 📘 Overview of Level 1: Nanobots

Level 1 is designed to empower young students to create their very first bots using logic-based automation. Each "nanobot" is a simple, no-code application that connects services to perform small but exciting tasks.

Examples of Nanobot Lessons:
- 🔊 Text-to-Voice Bot
- ✉️ Logic App Bot that sends emails
- 🎙️ Voice-to-Text Bot

---

# 🚀 Lesson 1: Nanobot – HTTP Request → Send Email

In this lesson, we will create a **Nanobot** that:
- Listens for an incoming web request
- Sends an email in response to that request
- Returns a `200 OK` HTTP response to confirm success

---

## 📋 Prerequisites

Before starting, make sure you have the following ready:

🔗 [Microsoft Azure Account](https://portal.azure.com)  
📧 An **Office 365 email account**  
🌐 Basic knowledge of logging into Azure Portal  

🔧 Full list of prerequisites:  
👉 [Logic App Prerequisites Guide](https://learn.microsoft.com/en-us/azure/logic-apps/create-single-tenant-workflows-azure-portal#prerequisites)

---

## 📹 Study Materials

- [📺 Video Tutorial: Create Logic App Nanobot](https://youtu.be/HWxb7KPPJ9o?si=lM8z1WWvFwQnLlT0)
- [📘 Microsoft Docs: Create Logic App Workflow](https://learn.microsoft.com/en-us/azure/logic-apps/create-single-tenant-workflows-azure-portal)

---

## 🧱 Step-by-Step Guide

### 🔨 Step 1: Create a Logic App

1. Go to the [Azure Portal](https://portal.azure.com)
2. Search for **Logic App** in the search bar and click **Create**
3. Choose the following:
   - Subscription: (Your active subscription)
   - Resource Group: Create new or select existing
   - Logic App name: `nanobot-http-email`
   - Region: Select your closest region
   - Plan type: `Standard`
4. Click **Review + Create**, then **Create**

📖 More details:  
👉 [Create a Standard Logic App Resource](https://learn.microsoft.com/en-us/azure/logic-apps/create-single-tenant-workflows-azure-portal#create-a-standard-logic-app-resource)

---

### 🧩 Step 2: Add the HTTP Request Trigger

1. In your Logic App Designer, click **Blank workflow**
2. Click **+ Add a trigger**
3. Search for and select **"Request"** trigger → Choose **When an HTTP request is received**
4. Click **Use sample payload to generate schema**
   - Paste this sample:
     ```json
     {
       "name": "Student Bot"
     }
     ```
5. Click **Done**

---

### ✉️ Step 3: Add Action to Send Email

1. Click **+ New step**
2. Search for **Office 365 Outlook**
3. Choose **Send an email (V2)**
4. Sign in using your Office 365 credentials
5. Fill in the email fields:
   - **To:** (Enter your email)
   - **Subject:** New Request Received
   - **Body:** Hello, this is a message from your Nanobot! Name: `@{triggerBody()?['name']}`

---

### 🧪 Step 4: Test Your Nanobot

1. Click **Save**
2. Copy the **HTTP POST URL** from the Request trigger
3. Use browser to send a request using the url given by the trigger. 
     ```
4. Check your email inbox. You should receive the message!

---

### ✅ Final Output

- ✔️ An email is received when the endpoint is hit
- ✔️ HTTP response `200 OK` is returned
- ✔️ No code used — just pure logic automation!

---

# 🚀 Lesson 2: Nanobot – Return 200 on HTTP Request

This nanobot is simpler. It listens for an HTTP request and just responds with `200 OK`.

---

## 📋 Prerequisites

Same as Lesson 1. Azure account required.

---

## 🧱 Step-by-Step Guide

### 🔨 Step 1: Create Another Logic App

1. Repeat the same steps from Lesson 1 to create a new Logic App
   - Name it: `nanobot-http-200`
   - Use the same Standard plan

---

### 🔁 Step 2: Add the HTTP Request Trigger

1. Open Logic App Designer → Blank workflow  
2. Add **When an HTTP request is received** trigger  
3. Leave schema and payload fields blank

---

### 🔄 Step 3: Add Response Action

1. Click **+ New step**
2. Search for **Response**
3. Set **Status Code** to `200`
4. Optional: Add a message like `"Success from Nanobot!"` in the body

---

### 🧪 Step 4: Test It

1. Save the app  
2. Copy the HTTP endpoint URL  
3. Use Postman or ReqBin to make a `POST` request  
4. You should get a `200 OK` response with your success message

---

## 🧠 What You Learned

- How to create Logic App bots with no code
- How to set up HTTP triggers
- How to build mini bots that send emails and return responses

---

## 🧰 Next Steps

Stay tuned for more Nanobots:

- 📢 Text-to-Speech Bot  
- 🎧 Voice Command Bot  
- 🗂️ File-to-Action Trigger Bot

---

Happy Bot Building! 🤖✨  
