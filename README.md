# Proposly-Releases — Project Summary
# https://proposly-by-zamoog.vercel.app/

## What it is
SaaS AI tool that generates tailored Upwork proposals. Users upload their own past winning proposals as style templates, and the AI generates new proposals matching their voice for each job post.

## Core Features
- My Templates — save and manage past proposals as style references (add, edit, delete); two sample templates are pre-loaded for new users
- Generate — paste a job post or select one from Find Jobs, choose 2-5 templates as style reference, and get an editable AI-generated proposal
- Find Jobs — search live Upwork listings using filters (budget, experience level, job type, and more), then generate a proposal directly from a listing in one click
- Proposals — full history of every generated proposal, with a list view and detail panel

## Tech Stack
- Frontend: Next.js, Tailwind CSS
- Auth + Database: Supabase
- AI: OpenAI (GPT-4o)
- Job data: Apify (Upwork scraper)
