# GitHub Profile README Revamp Design

**Date:** 2026-07-12
**Status:** Approved direction; awaiting written-spec review

## Objective

Revamp Calvin Berndt's GitHub profile README for an audience of technical
peers. The profile should position Calvin as an **Applied AI Systems Engineer**
and show the breadth of his public, private, and professional work without
exposing proprietary information. The existing `CalvinBerndtreadme.gif` is a
fixed design element and will remain near the top of the profile.

## Audience and Positioning

The primary audience is engineers, technical collaborators, and open-source
peers. The README should read as a compact map of systems Calvin has built and
operated rather than as a conventional recruiter-facing résumé.

The opening identity will be:

> **Applied AI Systems Engineer**

The supporting copy will explain that Calvin builds voice, audio, and real-time
AI systems across telephony, data pipelines, intelligent agents, product
interfaces, and production infrastructure.

## Content Principles

1. **Lead with evidence.** Tie skills to professional work, named projects, or
   concrete systems rather than presenting an undifferentiated badge wall.
2. **Separate visibility levels.** Clearly distinguish public repositories from
   private and professional work.
3. **Protect AnSer information.** Describe engineering domains, system
   boundaries, and outcomes without naming customers, exposing sensitive data,
   linking private repositories, or publishing proprietary implementation
   details.
4. **Prefer current depth over historical completeness.** Feature the skills
   that best represent Calvin's present direction. Older languages and
   coursework may appear in the toolkit but should not define the opening.
5. **Keep personality.** Preserve the existing animated GIF and a direct,
   first-person voice.
6. **Stay scannable.** Use short paragraphs, concise bullets, and a curated
   number of badges or icons.

## README Structure

### 1. Header and Identity

- Friendly first-person greeting
- `Applied AI Systems Engineer` title
- Two-sentence introduction describing the end-to-end systems focus
- Links to `calvinberndt.com` and LinkedIn

### 2. Existing GIF

Keep `CalvinBerndtreadme.gif` at its current 640-pixel width, centered beneath
the introduction and contact links. Preserve the descriptive alt text.

### 3. What I'm Building at AnSer

Present AnSer as professional applied-AI systems work. Summarize the relevant
domains:

- Voice and call-analysis systems
- Transcription, diarization, and speaker-processing workflows
- Retrieval-augmented assistants and context-aware interfaces
- Automated QA and evaluation pipelines
- Real-time data, telephony, and communications infrastructure

The final prose must avoid claims that cannot be supported and must not expose
private code, customer details, credentials, operational addresses, or internal
architecture diagrams.

### 4. Engineering Focus

Group skills by problems and systems rather than by language:

- **Applied AI and agents:** LLM applications, RAG, tool use, evaluation, and
  agent workflows
- **Voice, audio, and telephony:** speech-to-text, audio processing, real-time
  media, LiveKit, SIP/VoIP concepts, and call-quality constraints
- **Data and retrieval:** Python pipelines, PostgreSQL, pgvector, embeddings,
  event-driven processing, and data validation
- **Product engineering:** TypeScript, React, Next.js, APIs, dashboards, and
  embeddable interfaces
- **Infrastructure and delivery:** Linux services, Docker, cloud deployment,
  observability, browser QA, and reproducible developer tooling

Only technologies supported by current work or repository evidence should be
featured. Java, C#, C++, HTML, and CSS can remain represented as background
skills, but they should not receive the same prominence as current AI and
systems work.

### 5. Selected Work

Feature three to five items. Each item should include:

- Project or system name
- Public, private, or professional label
- One-sentence problem statement
- One concise implementation or outcome detail
- Link only when a safe public destination exists

Candidate areas include AnSer voice/AI engineering, transcription tooling,
machine-learning studies, voice-agent prototypes, RAG chatbot work, and
production web or developer-tooling systems. Final selections will favor depth,
recency, and relevance to the profile title.

### 6. Technical Toolkit

Use a restrained set of categorized badges or inline technology names. The
toolkit should support the narrative above, not repeat it. Avoid activity
widgets, trophy counters, skill percentages, and other automatically generated
metrics that add visual noise without demonstrating engineering judgment.

### 7. Currently Exploring

Include a short, maintainable list reflecting active areas such as local model
workflows, agent tooling, evaluation, production voice systems, and reliable AI
infrastructure. Phrase these as current learning or exploration rather than
completed expertise.

### 8. Contact

Close with concise links to the personal site and LinkedIn. Do not expose a
personal email address in the README unless Calvin explicitly requests it.

## Visual Direction

The visual hierarchy will remain lightweight and GitHub-native:

1. Identity and concise introduction
2. Contact links
3. Existing GIF
4. Evidence-based technical sections
5. Curated toolkit and current interests

HTML alignment may be retained around the header, links, GIF, and badges where
GitHub Markdown does not provide equivalent control. Content sections should use
ordinary Markdown headings for accessibility and maintainability.

## Accuracy and Privacy Checks

Before completion:

- Verify every public link resolves.
- Confirm public/private/professional labels are accurate.
- Remove unsupported performance numbers and unverified claims.
- Scan AnSer copy for customer information, PII, credentials, private URLs, and
  proprietary implementation details.
- Ensure the GIF path and rendering remain unchanged.
- Preview the README using GitHub-compatible Markdown rendering when practical.

## Acceptance Criteria

- The profile identifies Calvin as an **Applied AI Systems Engineer** above the
  fold.
- The current GIF remains centered and visible near the top.
- The README explains what Calvin builds, not only which languages he knows.
- AnSer work is represented substantively without disclosing private details.
- Public and non-public work are distinguishable.
- Current AI, voice, data, product, and infrastructure skills receive greater
  emphasis than older coursework.
- The document remains concise enough for a technical peer to scan in roughly
  two minutes.
- All links and Markdown render correctly.

## Out of Scope

- Replacing or editing the GIF
- Redesigning `calvinberndt.com`
- Publishing private repositories or internal AnSer materials
- Creating new project screenshots or diagrams
- Adding live GitHub-statistics widgets
