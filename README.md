# Fundraising Agent

> **Agentic AI** — Helps women's health founders sharpen their investor narrative

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)]()
[![Agentic AI](https://img.shields.io/badge/Agentic-AI-6B46C1?style=flat-square)]()
[![Women's Health](https://img.shields.io/badge/Women's-Health-E91E8C?style=flat-square)]()
[![Healthcare AI](https://img.shields.io/badge/Healthcare-AI-red?style=flat-square)]()

## The Problem

Women's health founders are often building in a sector investors don't fully understand. The technology may be strong, but the narrative — market size framing, clinical validation positioning, go-to-market storytelling — often falls flat in investor meetings. This agent closes that gap.

## What It Does

An AI advisory agent that:
- Reviews founder pitch context and identifies narrative weaknesses
- Reframes market opportunity using women's health-specific framing
- Strengthens clinical validation and evidence positioning
- Generates sharpened investor narrative sections ready for deck integration
- Provides tailored feedback based on investor type (VC, strategic, angel)

## Tech Stack

| Layer | Technology |
|---|---|
| Agent Framework | Python + LLM orchestration |
| LLM | OpenAI GPT-4 |
| Language | Python 3.11+ |

## Getting Started

```bash
git clone https://github.com/jsfaulkner86/fundraising-agent
cd fundraising-agent
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
python main.py
```

## Environment Variables

```
OPENAI_API_KEY=your_key_here
```

## Background

Built by [John Faulkner](https://linkedin.com/in/johnathonfaulkner), founder of [The Faulkner Group](https://thefaulknergroupadvisors.com). Draws from direct advisory experience helping early-stage women's health tech founders prepare for institutional fundraising.

## What's Next
- Investor persona profiles for tailored narrative tuning
- Pitch deck section generator with slide-ready output
- Integration with the Women's Health Fundraising Tracker

---
*Part of The Faulkner Group's advisory AI toolset. See all projects at [github.com/jsfaulkner86](https://github.com/jsfaulkner86)*
