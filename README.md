# 🎓 Academic Stack Planner (n8n Workflow)

This project is an **n8n workflow** that generates a customized 6-month academic roadmap for B.Tech/BCA students based on their tech stack preferences, and schedules them via Gmail and Google Calendar. It uses **Google Gemini API** to generate semester-specific HTML roadmaps.

---

## 🚀 Features

- 📋 Interactive form to collect student details and preferences
- 🧠 Gemini-powered roadmap generation using HTML format
- 📧 Sends the generated roadmap to the user’s email
- 📆 Automatically creates tasks as Google Calendar events
- 🛠️ Minimal setup, fully customizable in n8n

---

## 🛠 How It Works

1. The user fills out a form with discipline, year, stack, and skill level.
2. Gemini API returns an HTML-formatted semester roadmap.
3. A Code node extracts and processes this HTML into clean text.
4. Another Code node converts the text into dated tasks across the semester.
5. Gmail node sends the roadmap.
6. Google Calendar node schedules roadmap tasks evenly over the semester.

---

## 🔑 Required Setup

- **Gmail OAuth2 Credentials** for sending emails
- **Google Calendar OAuth2 Credentials** for event creation
- **Google Gemini API Key** for roadmap generation (via Google AI Studio)

---

## 📂 How to Use

1. Import the JSON file in your n8n editor.
2. Configure your Gmail, Calendar, and Gemini credentials.
3. Activate the workflow.
4. Share the form link and start generating plans!

---

## 📧 Default Email Fallback

If the user email is not detected, fallback email used: `krishnabhatia09@gmail.com`

---

## 📁 File Structure

- `academic_stack_planner.json` – The core n8n workflow
- `README.md` – Project documentation

---

## 🔒 Notes

- This project stores no user data persistently.
- Tasks are evenly spaced between **July 15 – November 15** by default.
