# n8n AI Job Search Agent

An automated n8n workflow that functions as a smart job-hunting assistant. It accepts either plain-text job queries or uploaded PDF resumes, analyzes them using Google Gemini, and aggregates relevant remote job listings from both job boards and direct company career pages.

<img width="1090" height="527" alt="image" src="https://github.com/user-attachments/assets/bef12bde-2705-4a63-b39a-e7776950fe1e" />



## Features
* **Multi-Input Handling:** Accepts direct chat queries or parses uploaded PDF resumes.
* **AI-Powered Reasoning:** Uses Google Gemini (gemini-3.1-flash-lite) to interpret candidate skills and infer job roles.
* **Dual Sourcing:** Queries the Remotive API for job board listings and uses Firecrawl to find roles posted directly on company career pages.
* **Structured JSON Output:** Deduplicates and parses results into a clean format containing the job title, company, salary, country, and direct application link.

## Prerequisites
* An active n8n workspace.
* Google Gemini API Key.
* Firecrawl API Key.

## Installation
1. Download the `My workflow.json` file from this repository.
2. Open your n8n workspace and click **Add Workflow**.
3. Click the `...` menu in the top right corner and select **Import from File**.
4. Upload `My workflow.json`.
5. Open the **Google Gemini Chat Model** and **Career Page Search** nodes to add your respective API credentials.

## Usage
Activate the chat trigger in n8n and either type a direct request (e.g., "Find me remote data engineering jobs") or upload a PDF resume to let the agent infer your best-fit roles and find matching listings.

