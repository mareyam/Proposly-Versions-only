# Proposly-Releases — Project Summary

## What it is
SaaS AI tool that generates tailored Upwork proposals. Users upload their own past winning proposals as style templates; AI generates new proposals matching their voice for each job post.

MVP Feature Scope
Core (build first)

My Templates tab — paste/save past proposals with a label, list/edit/delete
Generate tab — paste job post text, AI generates proposal styled after saved templates, editable output, copy button
Proposals tab — history of past generated proposals (title + preview list on the left, full view on the right when clicked)
Auth (email/password via Supabase, with email confirmation via custom SMTP)

Tech Stack
Frontend: Next.js, Tailwind CSS
Auth + DB: Supabase (auth.users + profiles table)
AI: OpenAI API (gpt-4o)


Database Schema
profiles — id, email, proposals_generated (usage counter), created_at
templates — id, user_id, email, title, content, created_at
generations — id, user_id, email, job_post, proposal, created_at
flagged_submissions — id, user_id, email, reason, input_snippet, created_at (admin-only, no user-facing read policy)
