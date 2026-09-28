# TheAriLab

A full-stack playground for app requests, games, and AI tools, built by Ari with AI assistance. The frontend uses Angular 21, the Python services use FastAPI, and the data layer uses PostgreSQL on Supabase. The frontend runs on Vercel and backend services on Railway.

Live site: https://thearilab.com (account required for most features)

## What the project includes

- A request flow where friends and family can propose app ideas and track them.
- YourFundAI, a multi-agent stock analysis pipeline built with LangGraph and an Anthropic model. It orchestrates six parallel agents, streams progress to the UI, and generates PDF reports. Its output is exploratory, not financial advice.
- AI Study Lab, which turns uploaded notes, slides, and PDFs into flashcards and practice tests.
- MorningBrief, a scheduled AI-generated news briefing with summaries and contrasting viewpoints.
- Daily games with scores and leaderboards.

## Architecture

```text
Angular frontend (Vercel)
  |-- Supabase Auth and PostgreSQL data/storage
  |-- FastAPI services (Railway)
        |-- YourFundAI: agent workflow and report generation
        |-- AI Study Lab: file intake and flashcard generation
        `-- MorningBrief: scheduled brief generation
```

## Engineering notes

The frontend is organized into feature areas. The Python services are separate FastAPI applications. Database migrations are managed through Supabase. The application uses streaming for the stock-analysis workflow and guardrails around paid model usage.

## Showcase status

This repository is a text-only case study, not a copy of the private production repository. It contains no screenshots, production code, or third-party assets. The production repo remains private.
