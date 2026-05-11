# Smart Recruitment Pipeline 🚀
An automated AI-driven recruitment screening system built with **n8n**, **Docker**, and **Google Gemini AI**.

## 📖 Overview
This project automates the initial screening of resumes. It monitors a Google Drive folder, extracts text from PDF resumes, uses the Gemini 1.5 Flash model to evaluate candidates against specific criteria (SWE/BA roles), and logs structured results into Google Sheets.

## 🛠️ Tech Stack
- **Automation:** n8n (Self-hosted via Docker)
- **AI:** Google Gemini 1.5 Flash API
- **Cloud:** Google Drive API, Google Sheets API
- **Logic:** JavaScript (JSON parsing and data transformation)
- **Infrastructure:** Docker Desktop

## ⚙️ How it Works
1. **Trigger:** Polls a specific Google Drive folder for new PDF uploads.
2. **Extraction:** Downloads the file and converts PDF content to raw text.
3. **Analysis:** Passes text to Gemini with a specialized recruiter prompt.
4. **Parsing:** Uses JavaScript to transform the AI's response into a valid JSON object.
5. **Output:** Appends a new row to a recruitment tracker with Name, Score, and Reasoning.

## 📸 Demo
![Workflow Canvas](./screenshots/workflow_canvas.png)
![Resulting Sheet](./screenshots/result_sheet.png)

## 🚀 Setup
1. Import the `workflow.json` into your n8n instance.
2. Configure your Google Cloud and Gemini API credentials.
3. Update the Folder and Sheet IDs in the respective nodes.