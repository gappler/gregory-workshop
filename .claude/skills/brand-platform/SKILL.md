---
name: brand-platform
description: Build a brand platform and copy/voice guide for a professional association using its public web presence. Use this skill whenever the user wants to create brand guidelines, a brand platform, a style guide, a voice and tone document, or foundational brand documentation for an organization or association. Trigger when the user provides a URL and asks for brand documentation, copy guidelines, messaging frameworks, or AI prompting context for an organization. Also trigger when the user says things like "build a brand guide for", "create brand documentation", "synthesize brand signals", or "what is this org's voice and tone".
---

# Brand Platform Skill

Builds two foundational markdown documents for a professional association:
1. `brand-platform.md` — positioning, mission/vision/values, messaging hierarchy, audience profiles
2. `copy-voice-guide.md` — tone attributes, do's/don'ts, channel guidance, AI prompting context

Outputs are designed to be shared across the org, with partners, vendors, and chapters — and to serve as AI context documents for any Claude-powered content workflow.

---

## Inputs

- **Primary URL** (required): The organization's main website
- **Org description** (optional): Any additional context the user provides
- **Supplementary URLs** (optional): Conference sites, chapter sites, social profiles

---

## Research Methodology

### Phase 1: Site Crawl
Fetch and analyze these pages in order of priority:

1. Homepage — positioning language, headline copy, value propositions
2. About/Mission page — mission, vision, values statements
3. Membership page — audience definition, member value proposition
4. Advocacy/Issues page — strategic priorities, public stance
5. Conference or Events page — tone in promotional copy
6. Newsroom/Press — how they announce things, language patterns
7. Social media (LinkedIn, Twitter/X) — voice in short-form content

For each page, extract:
- Exact phrases that feel most "on brand"
- Repeated words or concepts
- Audience language (who they're talking to)
- Tone signals (formal/informal, aspirational/practical, bold/cautious)

### Phase 2: Signal Synthesis
After crawling, identify:
- **3-5 voice keywords** that consistently describe how the org communicates
- **Core positioning** — what they claim to be, for whom, why it matters
- **Messaging hierarchy** — primary message, secondary messages, proof points
- **Audience segments** — who they actually talk to and how
- **Gaps** — what's missing, inconsistent, or underdeveloped

### Phase 3: Improvement Recommendations
Where brand signals are weak, inconsistent, or absent — make specific recommendations. Flag all recommendations clearly with `[RECOMMENDED]` so the reader knows what's documented vs. suggested.

---

## Output 1: brand-platform.md

Use this structure:

```markdown
# [Org Name] Brand Platform
*Synthesized from public web presence — [date]*
*[RECOMMENDED] flags indicate suggested additions, not documented statements*

---

## Organization Overview
Brief factual description: founded, size, scope, membership.

---

## Mission
[Exact statement if documented, or closest synthesis]

## Vision  
[Exact statement if documented, or closest synthesis]

## Values
[List with brief descriptions. Flag any that are inferred.]

---

## Positioning Statement
A single paragraph: who we are, who we serve, what we do, why it matters, what makes us different.

---

## Brand Promise
One sentence. What members/audiences can always count on from this organization.

---

## Messaging Hierarchy

### Primary Message
The single most important thing to communicate.

### Secondary Messages
3-5 supporting messages that reinforce the primary.

### Proof Points
Specific, factual evidence that supports the messages (numbers, programs, history).

---

## Audience Profiles

### [Audience 1 Name]
- Who they are
- What they need from this org
- How to talk to them
- What to emphasize

[Repeat for each distinct audience segment]

---

## Strategic Priorities
Current focus areas drawn from strategic plan, advocacy, and recent communications.

---

## Brand Personality
5 adjectives that describe how this org should feel to interact with.
For each: what it means in practice, and what it does NOT mean.

---

## [RECOMMENDED] Gaps & Opportunities
Honest assessment of what's missing or inconsistent in current brand expression.
```

---

## Output 2: copy-voice-guide.md

Use this structure:

```markdown
# [Org Name] Copy & Voice Guide
*Companion to the Brand Platform — [date]*
*[RECOMMENDED] flags indicate suggested additions, not documented statements*

---

## Voice vs. Tone
Brief explanation: voice is consistent, tone adapts to context.

---

## Voice Keywords
3-5 words that define how this org always sounds.
For each keyword:
- What it means
- What it looks like in copy
- What to avoid

---

## Tone by Context
How tone shifts across situations:
- Member communications (email, newsletter)
- Advocacy and public policy
- Conference and events promotion  
- Social media
- Crisis or sensitive topics

---

## Copy Standards

### Do
- List of active guidance

### Don't  
- List of things to avoid

### Preferred Terms
Key terminology the org uses — and what NOT to say instead.

### Grammar & Style
AP Style or house style notes. Capitalization, punctuation, acronym usage.

---

## Channel-Specific Guidance

### Email / Newsletter
Tone, length, CTA language, subject line approach.

### Website
Headline style, body copy length, CTA conventions.

### Social Media
Platform-by-platform tone guidance.

### Press / Official Statements
Register, attribution, boilerplate.

---

## AI Prompting Context
A ready-to-use context block for pasting into Claude or other AI tools:

```
You are writing on behalf of [Org Name]. 

ORGANIZATION: [one sentence description]
VOICE: [3-5 keywords]
TONE: [2-3 sentences describing how they sound]
AUDIENCE: [primary audience description]
ALWAYS: [3-5 things to always do]
NEVER: [3-5 things to never do]
STYLE: [AP Style / key house style notes]
```

---

## Copy Examples by Channel
2-3 before/after examples showing voice in practice.
Label clearly: OFF BRAND vs. ON BRAND.
```

---

## File Output

Save both files to the current working directory:
- `brand-platform.md`
- `copy-voice-guide.md`

Name them with org slug if multiple orgs: `aia-brand-platform.md`, `aia-copy-voice-guide.md`

---

## Quality Check

Before delivering, verify:
- [ ] All `[RECOMMENDED]` flags are clearly marked
- [ ] No invented facts — every claim is sourced or flagged
- [ ] AI Prompting Context block is self-contained and usable as-is
- [ ] Both documents are under 500 lines each
- [ ] Copy examples are specific to this org, not generic
