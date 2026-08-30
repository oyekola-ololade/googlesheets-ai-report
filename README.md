# Google Sheets → AI Executive Summary

Pulls the last 7 days from a tracking sheet and has Claude write an executive summary, emailed and archived daily.

![n8n](https://img.shields.io/badge/-n8n-333?style=flat-square) ![Google Sheets API](https://img.shields.io/badge/-Google%20Sheets%20API-333?style=flat-square) ![Claude (Anthropic API)](https://img.shields.io/badge/-Claude%20(Anthropic%20API)-333?style=flat-square) ![SendGrid](https://img.shields.io/badge/-SendGrid-333?style=flat-square) ![Google Drive API](https://img.shields.io/badge/-Google%20Drive%20API-333?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-workflow-EA4B71?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

---

**[Open the visual project page →](./index.html)**

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Workflow](#workflow)
- [Tech Stack](#tech-stack)
- [Demo status](#demo-status)
- [Setup](#setup)
- [Repository Structure](#repository-structure)
- [Disclaimer](#disclaimer)

## Overview

**Trigger:** Webhook (daily report trigger)

Pulls the last 7 days from a tracking sheet and has Claude write an executive summary, emailed and archived daily.

### Key Features

- Rolling 7-day window analysis
- LLM-written executive summary
- Automatic email + Drive archive

## Architecture

Open the [visual project page](./index.html#architecture) for the flow derived from the sanitized export.


## Workflow

1. Daily report trigger fires the workflow
2. Fetch the tracking sheet from Google Sheets
3. Slice out the last 7 days of data
4. Claude generates an executive summary (growth, top product, trends)
5. Email the report to the team and archive a copy to Google Drive

## Tech Stack

- n8n
- Google Sheets API
- Claude (Anthropic API)
- SendGrid
- Google Drive API

## Demo status

A configured live-run recording is not included yet. Credentials and service identifiers remain placeholders.


## Setup

1. Import `workflow/T22_GoogleSheets_AI_Report.json` into your n8n instance (**Workflows → Import from File**).
2. Replace every placeholder credential/URL in the workflow (e.g. `YOUR_..._API_KEY`, `YOUR_..._URL`) with your own service credentials.
3. Activate the workflow and point the relevant integration (webhook source, scheduled trigger, etc.) at the generated webhook URL.
4. Test with a sample payload before going live.

## Repository Structure

```text
.
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── workflow/
    └── T22_GoogleSheets_AI_Report.json
```


## Disclaimer

This workflow was built as a portfolio/template project to demonstrate n8n workflow automation and AI integration. API credentials and sensitive configuration have been removed before publication — replace all `YOUR_..._KEY` / `YOUR_..._URL` placeholders with your own before use.

---

Designed and engineered by

**Oyekola Ololade**

AI Systems & Integration Engineer

- LinkedIn: <http://linkedin.com/in/ololade-oyekola-5b1797397>
- Email: <oyekolaololade69@gmail.com>
