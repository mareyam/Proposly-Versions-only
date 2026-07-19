# Proposly — Project Summary

## What it is
SaaS AI tool that generates tailored Upwork proposals. Users upload their own past winning proposals as style templates; AI generates new proposals matching their voice for each job post.

MVP Feature Scope
Core (build first)

My Templates tab — paste/save past proposals with a label, list/edit/delete
Generate tab — paste job post text, AI generates proposal styled after saved templates, editable output, copy button
Auth (email/password via Supabase)
Usage limit — 3 free generations, then paywall

Tech Stack
Frontend: Next.js, Tailwind CSS
Auth + DB: Supabase (auth.users + profiles table)
AI: OpenAI API (gpt-4o)
