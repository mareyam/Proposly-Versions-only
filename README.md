## Proposly — Project Summary
# Proposly — Project Summary

What it is

SaaS AI tool that generates tailored Upwork proposals. Users upload their own past winning proposals as style templates; AI generates new proposals matching their voice for each job post.

Tagline: "Write winning Upwork proposals in seconds — in your own voice."

MVP Feature Scope

Core (build first)


My Templates tab — paste/save past proposals with a label, list/edit/delete
Generate tab — paste job post text, AI generates proposal styled after saved templates, editable output, copy button
Auth (email/password via Supabase)
Usage limit — 3 free generations, then paywall
Stripe billing (Pro plan)


Explicitly cut from MVP


Browser extension (auto-detect/autofill on Upwork)
Job URL scraping (paste text only for now)
Proposal history & win-rate analytics
Team/agency accounts
Multi-language support
A/B testing


Future roadmap (post-MVP)


Browser extension for autofill
Tone/length controls
Bid amount + timeline suggestions
Job post quality scoring (red flags: low budget, unverified payment)
Team seats + shared template library
Referral program


Tech Stack


Frontend: Next.js, Tailwind CSS
Auth + DB: Supabase (auth.users + profiles table)
AI: OpenAI API (gpt-4o — gpt-3.5-turbo was tested and failed to reliably match template style)
Billing: Stripe
API route: /app/api/generate/route.js — server-side call, keeps API key off the client


Design System

Palette

Pastel, low-saturation, high-brightness.


Hero / social proof: light lavender
How it works: sage/mint green
Features: light purple
Pricing: light pink/rose
Final CTA: purple-to-pink gradient


UI Conventions


Text: black/near-black headlines, gray body text
Buttons: solid black pills (primary), white/outline pills (secondary)
Cards: white bg, rounded corners (~16–20px), subtle shadow
Feature tags: small purple pill badges
Pricing "Pro" card: inverted (black bg, white text)
Hero visual: glassy translucent purple/pink orbs


Landing Page Sections


Nav — logo, links, CTA pill
Hero — headline, subtext, dual CTA, glassy orb visual
How it works — 3-step cards
Features — 3 tagged feature cards
Pricing — Free / Pro ($19) / Agency ($49)
Social proof — 3 testimonials
Final CTA — gradient band
Footer


Build Progress So Far


Landing page (all sections above) built and reviewed
Generate tab UI (frontend) — job post input, output textarea, copy button
/api/generate route — server-side OpenAI call, moved off client to protect API key
Prompt engineering — strengthened buildPrompt() to explicitly analyze template style (sentence length, tone, structure, sign-off) before writing
In progress: verifying AI output actually follows template style (partial success after gpt-4o switch + stronger prompt)
Not started: My Templates tab backend, login/signup + Supabase Auth wiring, Stripe billing
