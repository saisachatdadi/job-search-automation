# Job Search Automation 🤖

An n8n workflow that automates LinkedIn job discovery, AI-powered relevance filtering, and structured tracking - built to eliminate manual job searching and ensure no relevant opportunities are missed.

## What It Does

- Scrapes LinkedIn job listings automatically using an Apify Actor
- Uses AI to assess the relevance of each role based on predefined criteria such as job title, skills, and location
- Filters out irrelevant listings before they ever reach you
- Outputs structured, organised results directly into a Google Sheet for easy tracking and management
- Reduces hours of manual job searching to a fully automated, intelligent pipeline

## Why I Built This

During my job search, I realised the process of discovering, filtering, and tracking applications was highly repetitive and time-consuming. Rather than accepting that inefficiency, I built this workflow to automate the entire discovery pipeline - freeing up time to focus on tailoring applications and preparing for interviews.

## Tech Stack

- **n8n** - Workflow automation platform
- **Apify** - LinkedIn job scraping via Apify Actor
- **AI (LLM)** - Relevance scoring and filtering of job listings
- **Google Sheets** - Structured output and application tracking
- **JSON** - Workflow export format

## How to Use

1. Import `Linkedin Job Scraper.json` into your n8n instance
2. Set up your Apify API key and configure your LinkedIn search parameters
3. Connect your Google Sheets account and target spreadsheet
4. Run the workflow and let it handle discovery, filtering, and tracking automatically

## About Me

MSc Business Analytics graduate passionate about automation, AI, and building tools that solve real problems.

🔗 [EaSi Analytics](https://github.com/saisachatdadi/EaSi-Analytics) - My intelligent self-adaptive analytics platform
