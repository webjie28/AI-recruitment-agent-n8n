# 🤖 AI Recruiter Agent: End-to-End Recruitment Automation with n8n

A production-grade recruiter AI agent built using **n8n**, **Google Gemini (1.5 Flash)**, and **Google Sheets** that automates the screening of incoming resumes from Gmail, filters spam, logs candidate data, and drafts customized responses.

---

## 🎯 Features
*   **Smart Pre-AI Spam Filter**: Blocks promotional emails and newsletters based on keywords and attachment presence before hitting the Gemini API (reducing token costs).
*   **PDF Resume Extraction**: Ingests candidate resumes in PDF format, parses the text contents, and structures the profile with AI.
*   **Duplicate Candidate Prevention (Upsert)**: Replaces standard row appending with an Upsert action, updating existing rows by matching candidates' email addresses (`Contact`).
*   **Awaiting Resume Handler**: If a candidate emails without a resume attachment, the system logs their status as `Incomplete - No Resume` and drafts an automated follow-up email.
*   **4-Route Router**: Classifies candidates and creates tailored email drafts in Gmail:
    *   `Route 0`: Intern/Fresh Grad invitation templates.
    *   `Route 1`: Senior/Experienced candidate invitations.
    *   `Route 2`: Spam archiver.
    *   `Route 3`: Needs Review (routing ambiguous applications to HR for manual inspection).

---

## 📐 Workflow Architecture

![n8n Recruitment Workflow Layout](assets/media__1784072156548.png)

---

## 🛠️ Project Structure
*   `portfolio.html`: The HTML structure of the project build case study (designed as a premium documentation page).
*   `portfolio.css`: Decoupled custom styling for the portfolio page (dark slate layout with custom interactive details).
*   `assets/`: Local screenshots of n8n parameters, debugging logs, and execution outputs.

---

## 🔧 Installation & Local Setup

### 1. View the Portfolio Locally
Simply open the `portfolio.html` file in any browser to view the interactive project journal:
```bash
# Open using explorer on Windows
explorer.exe portfolio.html
```

### 2. Import the n8n Workflow
1. Download or export the workflow JSON from n8n.
2. In your n8n workspace, click **Add Workflow** ➡️ **Import from File** and select the JSON file.
3. Configure your node credentials (Gmail OAuth2, Gemini API Key, Google Sheets OAuth2).

---

## 💡 Developer
Built by **[Benjie Lipalam](https://github.com/your-username)** as a showcase of agentic AI workflow automation and low-code integrations.
