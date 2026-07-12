# GitHub Profile README Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the current language-only GitHub profile with a concise, evidence-based profile positioning Calvin as an Applied AI Systems Engineer while preserving the existing GIF.

**Architecture:** This is a single-document change. `README.md` will use a centered HTML header and GIF, followed by accessible Markdown sections for professional focus, engineering capabilities, a curated toolkit, and contact links.

**Tech Stack:** GitHub Flavored Markdown, limited inline HTML, Shields.io badges

## Global Constraints

- Keep `CalvinBerndtreadme.gif` centered near the top at 640 pixels wide.
- Do not add Selected Work or Currently Exploring sections.
- Keep a Contact section.
- Describe AnSer work without customer information, private URLs, credentials, PII, or proprietary implementation details.
- Distinguish current applied-AI systems skills from older background languages.
- Keep the profile scannable in roughly two minutes.

---

### Task 1: Rewrite and verify the GitHub profile

**Files:**
- Modify: `README.md`
- Reference: `CalvinBerndtreadme.gif`

**Interfaces:**
- Consumes: GitHub profile rendering for the `calvinberndt/calvinberndt` repository
- Produces: A self-contained GitHub profile README with no runtime dependencies

- [ ] **Step 1: Confirm the existing visual asset and destination links**

Run:

```bash
test -f CalvinBerndtreadme.gif
curl -LIsS --max-time 15 https://calvinberndt.com/ | head -n 1
curl -LIsS --max-time 15 https://www.linkedin.com/in/calvin-berndt | head -n 1
```

Expected: the GIF check exits `0`; both URLs return an HTTP response without a DNS or connection error.

- [ ] **Step 2: Replace the README with the approved structure and copy**

Write `README.md` with this content:

```markdown
<div align="center">

# Hi, I'm Calvin Berndt 👋

### Applied AI Systems Engineer

I build voice, audio, and real-time AI systems—from telephony and data pipelines to intelligent agents and production infrastructure.

[Website](https://calvinberndt.com/) · [LinkedIn](https://www.linkedin.com/in/calvin-berndt)

<img src="CalvinBerndtreadme.gif" width="640" alt="Coding outdoors animated GIF" />

</div>

## About Me

I'm a software engineer focused on turning AI capabilities into dependable systems. My work spans the full path from audio and communications infrastructure through data processing, retrieval, agent orchestration, evaluation, and user-facing applications.

I enjoy the engineering between a promising model demo and a system people can actually operate: understanding constraints, connecting the right components, measuring behavior, and making the result observable and maintainable.

## At AnSer

At **AnSer**, I work at the intersection of applied AI, communications infrastructure, and software engineering. My work includes:

- Voice and call-analysis workflows grounded in real telephony and audio constraints
- Transcription, diarization, speaker processing, and structured extraction pipelines
- Retrieval-augmented assistants and context-aware AI interfaces
- Automated QA and evaluation systems for analyzing agent interactions
- Real-time data flows and supporting infrastructure for production AI applications

## Engineering Focus

- **Applied AI & Agents** — LLM applications, RAG, tool use, agent workflows, prompt design, and evaluation
- **Voice, Audio & Telephony** — speech-to-text, audio processing, real-time media, LiveKit, and SIP/VoIP systems
- **Data & Retrieval** — Python pipelines, PostgreSQL, pgvector, embeddings, event-driven processing, and data validation
- **Product Engineering** — TypeScript, React, Next.js, APIs, dashboards, and embeddable interfaces
- **Infrastructure & Delivery** — Linux services, Docker, cloud deployment, observability, browser QA, and reproducible developer tooling

## Technical Toolkit

<div align="center">

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

</div>

Additional experience includes JavaScript, Java, C#, C++, HTML, CSS, machine learning workflows, cloud platforms, and developer automation.

## Contact

- [calvinberndt.com](https://calvinberndt.com/)
- [LinkedIn](https://www.linkedin.com/in/calvin-berndt)

<!--
**calvinberndt/calvinberndt** is a special repository because its README.md appears on the GitHub profile.
-->
```

- [ ] **Step 3: Run structural and privacy checks**

Run:

```bash
rg -n "Applied AI Systems Engineer|CalvinBerndtreadme.gif|## At AnSer|## Engineering Focus|## Technical Toolkit|## Contact" README.md
! rg -n "Selected Work|Currently Exploring|TODO|TBD" README.md
! rg -n -i "password|secret|token|customer|patient|@[[:alnum:]._-]+\\.[[:alpha:]]{2,}" README.md
git diff --check
```

Expected: every required heading/string is found; forbidden-section, placeholder, sensitive-content, and whitespace checks exit successfully.

- [ ] **Step 4: Review the rendered profile locally**

Inspect the Markdown or use a GitHub-compatible preview and confirm:

- The title and professional identity appear above the fold.
- The original GIF renders at 640 pixels wide.
- The AnSer wording describes engineering domains without private details.
- Badge rows wrap acceptably at narrow and wide widths.
- Heading hierarchy and links are readable.

- [ ] **Step 5: Commit the verified README**

Run:

```bash
git add README.md docs/superpowers/specs/2026-07-12-github-profile-readme-design.md docs/superpowers/plans/2026-07-12-github-profile-readme.md
git commit -m "docs(profile): present applied AI systems work"
```

Expected: one commit records the approved scope update, implementation plan, and verified profile rewrite.
