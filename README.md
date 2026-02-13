# 🤖 AI Email Agent

AI Email Agent is an automated email assistant built with **n8n**, **OpenAI**, **Gmail**, and **Airtable**.  
It reads incoming emails, classifies them using AI, generates contextual replies, applies labels, and stores structured data for tracking and organization.

## 📊 Workflow Architecture

![AI Email Agent Workflow](/workflow.png)

---

## 🚀 Features

- 📥 Automatic Gmail trigger for new messages  
- 🧠 AI-powered email classification  
- ✍️ Context-aware reply generation  
- 🏷️ Dynamic Gmail label assignment  
- 🗂️ Structured logging in Airtable  
- 🔀 Conditional routing using switch logic  
- ⏱️ Timezone handling with custom JavaScript node  

---

## 🛠️ Tech Stack

- n8n (workflow automation)
- OpenAI Chat Model
- Gmail API
- Airtable API
- JavaScript

---

## 📊 Workflow Overview

1. Gmail Trigger receives a new email  
2. AI Agent analyzes and classifies the email  
3. Structured output parser formats JSON response  
4. Airtable stores email metadata  
5. Switch node routes by category  
6. Gmail applies appropriate label  
7. Optional auto-reply is sent  

---

## 🧾 AI Output Format

```json
{
  "category": "Work | Personal | University | Finance | Urgent | Spam",
  "priority": "Low | Medium | High",
  "requires_reply": true,
  "reply_text": "Generated email response",
  "summary": "Short summary of the email"
}
