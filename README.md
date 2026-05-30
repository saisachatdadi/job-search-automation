# Job Search Automation 🤖

A sophisticated 78-node n8n workflow that automates the entire job search pipeline - from LinkedIn discovery to AI relevance scoring, and structured tracking in Google Sheets.

## What It Actually Does

This is not a simple job scraper. It is a fully automated, AI-powered recruitment pipeline that handles every stage of the job search process without manual intervention.

### Stage 1 - Multi-Role Job Discovery
The workflow runs parallel searches across 7 distinct job roles simultaneously:
- Business Analyst
- Junior Project Manager
- Analyst
- Project Support Officer
- Implementation Coordinator
- Operations Coordinator
- Project Coordinator

Each role has its own dedicated LinkedIn search URL, feeding into 8 separate Apify Actor instances that scrape up to 100 job listings per search, filtered specifically to Ireland (IE).

### Stage 2 - AI Relevance Scoring
Every scraped job listing is passed through an OpenAI LLM that:
- Reads the full job description
- Compares it against a live version of my CV (fetched directly from Google Docs)
- Assesses relevance based on skills, experience, and job title alignment
- Returns a structured relevance score
- Filters out irrelevant roles automatically using conditional logic

### Stage 3 - Structured Tracking
All relevant jobs and their details are appended to a Google Sheet for organised tracking, giving a clean overview of every opportunity discovered, scored, and acted upon.

## Why I Built This

During my job search, I realised that discovering, filtering, and applying to relevant roles was an enormously time-consuming manual process. Rather than accepting that inefficiency, I built this end-to-end pipeline to handle discovery, relevance assessment, and Google Docs appending - freeing me up to focus entirely on tailoring cover letters, preparing for interviews, and engaging with hiring managers.

This workflow processes hundreds of job listings per run and produces relavant job-postings in minutes - a process that would otherwise take days of manual effort.

## Tech Stack

- **n8n** - Workflow orchestration platform (78 nodes)
- **Apify** - LinkedIn job scraping via Apify Actor (8 parallel instances, up to 100 jobs each)
- **OpenAI (LLM)** - AI relevance scoring.
- **Google Docs API** - Live CV fetching.
- **Google Sheets** - Structured job tracking and pipeline management
- **JavaScript** - Custom data transformation nodes

## Workflow Architecture

***Trigger
└── 7 Parallel Job Search URL Nodes (by role)
└── 8 Apify Scrape Actors (up to 100 jobs each)
└── Loop Over Items (batch processing)
└── Fetch base CV from Google Docs
└── AI Relevance Check (OpenAI)
└── Filter (relevant only)
└── Upload via Drive API
└── Append to Google Sheets***

## How to Use

1. Import `Linkedin Job Scraper.json` into your n8n instance
2. Connect your Apify account and configure LinkedIn search URLs for your target roles
3. Link your OpenAI API key for relevance scoring
4. Connect your Google account (Docs, Drive, Sheets)
5. Add your master CV to Google Docs and update the document URL in the workflow
6. Run the workflow and let it handle the rest

## About Me

MSc Business Analytics graduate passionate about automation, Project Coordination, AI, and building tools that solve real problems.

🔗 [EaSi Analytics](https://github.com/saisachatdadi/EaSi-Analytics) - My intelligent self-adaptive analytics platform
