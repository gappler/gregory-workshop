# Association Marketing Lifecycle
## A Navigation Map for Gregory AI Implementation Workshops

---

### How to Use This Document

This is not a curriculum. It is a map.

Associations don't move through this lifecycle in sequence — they're operating at every stage simultaneously, with varying levels of maturity at each. Use this map to locate where a participant's team is doing work, where Claude Code can have immediate impact, and where the bigger leverage is if they're ready for it.

Each entry includes:
- **What it is** — the task or deliverable
- **Where it lives** — lifecycle stage
- **How we do it** — method, inputs, human judgment required
- **What comes out** — output and where it lives
- **Gregory skill or tool** — what's been built to support it

---

## The Lifecycle

```
STAGE 1          STAGE 2          STAGE 3          STAGE 4          STAGE 5          STAGE 6
Brand &    →    Content &   →   Campaigns &  →   Member        →   Events &    →   Measurement
Identity        Voice            Programs         Engagement        Conferences      & Reporting
```

---

## Cross-Stage: Project Management & Operations

*Project management is not a lifecycle stage — it is the operating layer that runs underneath every stage simultaneously. It is also one of the highest-leverage AI applications in association marketing, precisely because it is high-frequency, high-tedium, and almost universally underdeveloped. Most association marketing teams have no formal PM practice at all. The ones that do spend disproportionate time on administrative coordination rather than strategic work.*

*AI doesn't replace project management judgment. It eliminates the grunt work that keeps teams from exercising it.*

---

### PM-A. Project & Campaign Templates

**What it is:** Reusable project structures for recurring work — campaign templates, content production templates, event marketing templates — so teams aren't rebuilding the same plan from scratch every cycle.

**Where it lives:** Cross-stage — used at the start of every major initiative

**How we do it:**
- Define the recurring project types in the organization's marketing operation
- For each type, build a standard template: phases, milestones, tasks, dependencies, owners, timing
- Encode institutional knowledge into the template (what always gets forgotten, what always runs late, what requires lead time most people underestimate)
- Adapt templates for different scales: full annual conference vs. regional event vs. webinar

**Inputs:** Prior project plans, post-mortem findings, team knowledge of what actually happens vs. what was planned

**Human judgment required:**
- Which templates are worth building vs. which projects are too variable to template
- Encoding the institutional knowledge that makes templates useful rather than generic

**What comes out:**
- `[org]-[project-type]-template.md` — reusable project template with phases, tasks, owners, timing
- `[org]-campaign-template.md`, `[org]-conference-template.md`, `[org]-content-production-template.md`

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — Claude can generate a first-draft template from a project description in minutes.

---

### PM-B. Work Breakdown Structure (WBS)

**What it is:** A hierarchical decomposition of a project into all its component tasks — the foundation of any project plan. The step most teams skip, which is why projects go sideways.

**Where it lives:** Cross-stage — applies to any project of meaningful complexity

**Why AI helps here:** A WBS for a conference marketing campaign might have 150+ tasks across 8 workstreams. Building it manually takes hours. Claude can generate a comprehensive first draft from a project brief in minutes — and it will catch dependencies and tasks that a team under pressure will forget.

**How we do it:**
- Define project scope, timeline, and deliverables
- Generate full task list organized by workstream and phase
- Identify dependencies between tasks
- Flag long-lead items that must start earlier than they feel like they should
- Assign effort estimates where possible

**Inputs:** Project brief or campaign brief, prior year plan if available, team structure

**Human judgment required:**
- Effort estimates — Claude can suggest, humans who've done the work know what's realistic
- Resource allocation — who does what given actual staff capacity
- Dependencies that are relationship-based rather than logical (e.g., "we can't send this until the board has seen it")

**What comes out:**
- `[org]-[project]-wbs.md` — full work breakdown structure with tasks, dependencies, and effort estimates

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — one of the clearest PM applications. Pairs with PM-C for scheduling.

---

### PM-C. Project Timeline & Schedule

**What it is:** A working timeline that translates the WBS into a calendar — with milestones, deadlines, and the critical path made visible.

**Where it lives:** Cross-stage — every significant project

**How we do it:**
- Take WBS output and assign dates working backward from hard deadlines
- Identify critical path — the sequence of tasks where any delay pushes the final deadline
- Flag conflicts: where multiple workstreams compete for the same resource at the same time
- Build milestone markers for leadership visibility

**Inputs:** WBS, hard deadlines (event date, board meeting, campaign launch), team availability and capacity

**Human judgment required:**
- Capacity reality-checking — Claude doesn't know that your one email developer is also supporting three other projects
- Negotiating deadline conflicts with internal stakeholders
- What to cut if the schedule is overloaded

**What comes out:**
- `[org]-[project]-timeline.md` — milestone-level schedule with critical path noted
- Can be exported to project management tools (Asana, Monday, Basecamp)

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for generation; human required for capacity and conflict resolution.

---

### PM-D. Creative & Project Brief

**What it is:** The written brief that kicks off any creative or strategic project — defining the goal, audience, message, deliverables, timeline, and success criteria before any work begins. The document that prevents scope creep and misaligned output.

**Where it lives:** Cross-stage — used for campaigns, content projects, agency engagements, design requests

**Why it matters:** Most association marketing teams brief by meeting or by example ("make it like last year's"). A written brief forces clarity before work starts and gives the team something to evaluate output against. AI can draft a brief from a conversation or a set of inputs faster than anyone can type one from scratch.

**How we do it:**
- Gather inputs: goal, audience, key message, deliverables, timeline, budget, constraints
- Generate brief using standard structure: background, objective, audience, message, tone, deliverables, timeline, success metrics
- Adapt for recipient: internal brief vs. agency brief vs. design brief

**Inputs:** Project or campaign goal, brand platform, audience persona, prior briefs if any

**Human judgment required:**
- What the brief is actually asking for — scope clarity is a human judgment
- Budget parameters
- Approvals and review process

**What comes out:**
- `[org]-[project]-brief.md` — complete project or creative brief

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — brief generation from inputs is a natural Claude task and immediately teachable in workshop.

---

### PM-E. Meeting Notes & Action Items

**What it is:** The synthesis of meeting content into structured notes, decisions, and action items — distributed to participants immediately after the meeting rather than days later or never.

**Where it lives:** Cross-stage — every team meeting, stakeholder review, agency check-in

**How we do it:**
- Record or transcribe meeting (via Otter, Zoom transcript, or manual notes)
- Claude synthesizes into: key decisions made, action items with owner and due date, open questions requiring follow-up, parking lot items
- Format for distribution

**Inputs:** Meeting transcript or rough notes

**Human judgment required:**
- Accuracy review — Claude will occasionally misattribute or mis-summarize
- Decisions that were implied rather than stated explicitly
- Sensitive content that shouldn't be in written distribution

**What comes out:**
- `[meeting-date]-[topic]-notes.md` — structured meeting notes with decisions and action items

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — one of the most immediately useful PM applications. Low barrier to entry for workshop participants.

---

### PM-F. Status Report

**What it is:** A regular (weekly or biweekly) summary of project status across active initiatives — what's on track, what's at risk, what needs a decision.

**Where it lives:** Cross-stage — recurring for any active project portfolio

**How we do it:**
- Gather status inputs from team (brief updates per project)
- Claude synthesizes into consistent format: RAG status (Red/Amber/Green), key accomplishments, upcoming milestones, issues requiring escalation
- Adapt for audience: team-level detail vs. leadership summary

**Inputs:** Team status updates, project timeline, prior status report

**Human judgment required:**
- Accurate RAG assessment — teams often understate risk
- What to escalate vs. handle internally
- Tone when surfacing problems to leadership

**What comes out:**
- `[org]-status-report-[date].md` — structured status report

**Gregory skill:** Not yet built
**Status:** Documented. Medium AI leverage — synthesis is fast; honest assessment is human.

---

### PM-G. Vendor & Agency Management

**What it is:** The written artifacts that make vendor and agency relationships work — RFPs, scopes of work, performance reviews, feedback documentation.

**Where it lives:** Cross-stage — wherever outside resources are engaged

**How we do it:**
- Draft RFPs from project brief and requirements
- Generate scope of work from agreed deliverables and timeline
- Write structured feedback on creative work (specific, actionable, tied to brief criteria)
- Draft performance review documentation

**Inputs:** Project brief, vendor/agency roster, deliverables received, evaluation criteria

**Human judgment required:**
- Vendor selection — relationships and track record matter
- Negotiation — budget and scope
- Relationship management — tone of feedback, handling of disputes

**What comes out:**
- `[org]-[project]-rfp.md` — request for proposal
- `[org]-[vendor]-sow.md` — scope of work
- `[org]-[vendor]-feedback-[date].md` — structured creative feedback

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for document drafting; human required for relationship management.

---

### PM-H. Collaborative Workflows & Version Control

**What it is:** The infrastructure and practices that allow marketing teams to work on shared content together — with version history, approval workflows, and a single source of truth. GitHub for marketers, not just developers.

**Where it lives:** Cross-stage — applies to any content or document that multiple people touch

**Why it matters for associations:** Most association marketing teams collaborate by emailing files, maintaining competing versions in Dropbox, or using Google Docs with no governance. The result is version confusion, lost institutional knowledge, and no audit trail. GitHub — used through Claude Code — solves this in a way that also makes AI assistance more powerful: when prompts, templates, and brand assets live in a shared repo, every team member benefits from improvements anyone makes.

**What this looks like in practice:**
- Brand platform, copy/voice guide, and approved messaging live in a shared repo — not someone's hard drive
- Campaign briefs and content drafts are versioned — you can see what changed and why
- Claude Code skills are shared across the team — one person builds a renewal campaign skill, everyone uses it
- Approval workflows are documented in the repo — what requires review, who reviews it, what the sign-off process looks like
- New staff onboard faster because institutional knowledge is in the repo, not in someone's head

**How we do it:**
- Set up shared GitHub organization or repo for marketing team
- Establish folder structure: brand assets, campaign templates, skills, approved copy, briefs
- Define commit conventions: what goes in, how it's labeled, what gets reviewed before merge
- Train team on basic Git workflow: pull, edit, commit, push, review
- Integrate with Claude Code so team members can invoke shared skills from their own machines

**Inputs:** Existing file structure, team size and technical comfort level, current collaboration tools

**Human judgment required:**
- What level of Git sophistication is realistic for a non-technical marketing team
- Which assets belong in version control vs. which stay in Google Drive or SharePoint
- Governance: who can merge, who reviews, who owns the repo

**What comes out:**
- A working shared GitHub repo for the marketing team
- `[org]-repo-structure.md` — documented folder structure and conventions
- `[org]-collaboration-guide.md` — simple guide for non-technical team members

**Gregory skill:** Not yet built
**Status:** Documented. One of the more technically ambitious workshop deliverables — but also one of the most differentiating. Teams that leave with a shared repo and a working collaboration workflow are operating at a different level than teams that don't.

*Note: This is where Claude Code's value as a team tool — not just an individual tool — becomes visible. The shared skills library is the payoff: one person builds a session description skill, the whole team runs it.*

---

## Project Management Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| PM-A | Project & Campaign Templates | Not built | Documented — high priority |
| PM-B | Work Breakdown Structure | Not built | Documented — high AI leverage |
| PM-C | Project Timeline & Schedule | Not built | Documented |
| PM-D | Creative & Project Brief | Not built | Documented — high priority |
| PM-E | Meeting Notes & Action Items | Not built | Documented — high AI leverage, low barrier |
| PM-F | Status Report | Not built | Documented |
| PM-G | Vendor & Agency Management | Not built | Documented |
| PM-H | Collaborative Workflows & Version Control | Not built | Documented — differentiating |

*Project management is arguably the most universally applicable section of this lifecycle — every association marketing team, regardless of size or sophistication, does this work. And almost none of them do it well. This is where Gregory can have immediate, visible impact from day one of a workshop.*

---

## Cross-Stage: AI-Powered Tools & Products

*AI-powered tools are a step above AI-assisted work. The lifecycle stages describe a human using AI to produce a deliverable. Tools are different — they run on their own and serve an audience directly, without a human in the loop for every interaction. Building them requires more technical infrastructure, but the leverage is dramatically higher: a member chatbot that answers 500 benefit questions a week doesn't require 500 staff hours.*

*This category is where associations start to feel like technology organizations.*

---

### TOOL-A. Member-Facing Chatbot

**What it is:** A conversational AI tool embedded on the association website or member portal that answers member questions about benefits, programs, events, CE requirements, membership categories, and organizational history — 24/7, without staff intervention.

**Where it lives:** Cross-stage — draws on brand platform, benefits inventory, program catalog, event details, and FAQ content from every stage

**How it works:**
- Build a knowledge base from existing content: website, member handbook, FAQ, benefits guide, program descriptions, policy documents
- Configure a Claude-powered chat interface with guardrails for tone, scope, and escalation
- Define escalation path: when the bot can't answer, it routes to a staff contact or support ticket
- Maintain and update knowledge base as programs and policies change

**Inputs:** Existing member-facing content, FAQ, benefits inventory, brand platform (for voice)

**Human judgment required:**
- Knowledge base curation — what the bot should and shouldn't answer
- Guardrail design — what topics to handle carefully (billing disputes, complaints, sensitive policy questions)
- Ongoing maintenance as content changes

**What comes out:**
- A deployed chatbot — not a document
- `[org]-chatbot-knowledge-base.md` — the underlying content that feeds it

**Gregory skill:** Not yet built
**Status:** Documented. Requires technical build; Claude API or similar. Strong demonstration of AI as product rather than tool.

---

### TOOL-B. Staff Knowledge Base & Internal Assistant

**What it is:** An internal AI tool that answers staff questions about brand guidelines, HR policies, organizational history, process documentation, approved copy blocks, and institutional knowledge — replacing the "ask someone who's been here forever" dynamic.

**Where it lives:** Cross-stage — especially relevant for organizations with high staff turnover or distributed teams

**Why it matters for associations:** Associations lose institutional knowledge constantly — to turnover, to retirement, to organizational restructuring. An internal knowledge base that can be queried conversationally preserves that knowledge and makes it accessible to anyone on the team.

**Inputs:** Brand platform, HR policies, process documentation, boilerplate library, organizational history, meeting notes archive

**What comes out:**
- A deployed internal assistant
- `[org]-internal-knowledge-base.md` — curated content inventory

**Gregory skill:** Not yet built
**Status:** Documented. Builds directly on brand platform and boilerplate library outputs from Stage 1 and SCALE-F.

---

### TOOL-C. Conference Assistant

**What it is:** A conference-specific chatbot available to attendees during the event — answering schedule questions, wayfinding, speaker information, session recommendations, and logistics details in real time.

**Where it lives:** Cross-stage — Stage 5 application, draws on all conference content

**What it replaces:** The information desk queue, the "I can't find my session" problem, the staff member who has to answer the same hotel shuttle question 200 times.

**Inputs:** Final session schedule, venue map, speaker bios, hotel and logistics information, FAQ, wayfinding copy

**What comes out:**
- A deployed conference assistant (web or SMS-based)
- `[org]-[event]-conference-assistant-kb.md` — knowledge base content

**Gregory skill:** Not yet built
**Status:** Documented. Well-scoped, time-bounded, strong pilot candidate for associations new to AI-powered tools.

---

### TOOL-D. Membership Recommendation Engine

**What it is:** A tool that helps prospective or current members identify the most relevant benefits, programs, communities, and next steps based on their career stage, interests, and engagement history.

**Where it lives:** Cross-stage — Stage 3 (acquisition), Stage 4 (engagement and retention)

**How it works:**
- Member answers a short intake (career stage, practice type, goals, interests)
- Tool surfaces the 3–5 most relevant benefits and programs with specific rationale
- Optionally connects to AMS data for personalized recommendations based on actual member history

**Inputs:** Benefits inventory, audience personas, AMS member data (optional)

**What comes out:**
- A deployed recommendation tool
- `[org]-recommendation-logic.md` — decision rules and persona mapping

**Gregory skill:** Not yet built
**Status:** Documented. Can start simple (rule-based) and grow toward personalization with AMS integration.

---

## AI-Powered Tools Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| TOOL-A | Member-Facing Chatbot | Not built | Documented |
| TOOL-B | Staff Knowledge Base & Internal Assistant | Not built | Documented |
| TOOL-C | Conference Assistant | Not built | Documented — strong pilot candidate |
| TOOL-D | Membership Recommendation Engine | Not built | Documented |

---

## Cross-Stage: Agentic Systems & Automation

*Agentic systems are the frontier. Where AI-assisted work requires a human at every step, and AI-powered tools serve users directly, agentic systems are autonomous pipelines — multiple AI agents working together on complex, multi-step tasks with minimal human intervention. One agent researches. One writes. One formats. One quality-checks. An orchestrator coordinates them all toward an outcome.*

*Most associations aren't ready for this yet. It requires technical infrastructure, well-defined processes, and organizational trust in AI outputs. But it belongs on the map — both because some organizations are ready, and because the trajectory of every organization is toward this tier.*

*Early Returns — the political intelligence research system built as a Gregory proof-of-concept — is an example of an agentic system: multiple research, synthesis, and writing agents orchestrated toward a published intelligence product.*

---

### AGENT-A. Membership Intelligence System

**What it is:** An autonomous system that monitors renewal risk across the membership, drafts personalized outreach for at-risk members, surfaces recommendations to the membership team each morning, and tracks outcomes — without requiring staff to manually pull reports or write individual messages.

**Where it lives:** Cross-stage — Stage 4 primary, draws on AMS data continuously

**How it works:**
- Renewal risk agent monitors AMS data for engagement signals: login activity, event attendance, benefit utilization, email engagement
- Scoring agent flags members crossing risk thresholds
- Writing agent drafts personalized outreach based on member profile and risk signals
- Reporting agent surfaces daily digest to membership team: who to contact, what to say, what's working
- Human reviews and approves outreach before send (or sets rules for automatic send)

**Inputs:** AMS with API access, email platform, engagement data across platforms

**Gregory skill:** Not yet built
**Status:** Documented. Requires AMS API integration; most appropriate for organizations with Salesforce, HubSpot, or AMS platforms with clean API access.

---

### AGENT-B. Conference Content Pipeline

**What it is:** An end-to-end automated pipeline that ingests raw session submissions, scores and categorizes them, drafts publication-ready descriptions, builds a balanced program, and produces all promotional copy — with human review at defined checkpoints.

**Where it lives:** Stage 5 primarily — but produces content that feeds Stages 2, 3, and 6

**How it works:**
- Ingestion agent pulls submissions from submission platform
- Review agent scores each submission against defined criteria
- Writing agent drafts polished session descriptions and speaker bios
- Programming agent identifies gaps and balance issues in the draft program
- Promotion agent generates copy for each channel once program is approved
- Human program committee reviews scoring and makes final selections

**Inputs:** Submission platform API or export, conference themes, scoring rubric, brand platform

**Gregory skill:** Not yet built — workflow library #3 and #4 are component pieces
**Status:** Documented. One of the clearest agentic applications in association marketing — high volume, well-defined process, significant time savings.

---

### AGENT-C. Media Monitoring & Communications System

**What it is:** An autonomous system that monitors media coverage of the organization and its issues, summarizes relevant coverage daily, drafts responses or talking points for significant stories, and alerts communications staff to anything requiring immediate human attention.

**Where it lives:** Cross-stage — communications function, connects to advocacy (Stage 3) and brand (Stage 1)

**How it works:**
- Monitoring agent tracks media sources, social mentions, and legislative activity
- Synthesis agent summarizes daily coverage and flags significant items
- Writing agent drafts response talking points or social reactions for staff review
- Alert agent surfaces anything requiring same-day human response

**Inputs:** Media monitoring service or RSS feeds, social listening, legislative tracking, brand platform, approved messaging

**Gregory skill:** Not yet built
**Status:** Documented. Requires integration with media monitoring infrastructure. High value for organizations with active advocacy or public affairs functions.

---

### AGENT-D. Research & Competitive Intelligence System

**What it is:** An autonomous research system that monitors peer organizations, tracks industry trends, surfaces competitive intelligence, and delivers a regular briefing to leadership — without requiring staff to do manual research.

**Where it lives:** Cross-stage — feeds brand strategy, program development, and competitive positioning

**How it works:**
- Research agents monitor peer organization websites, publications, and announcements
- Analysis agent identifies strategic moves, new programs, positioning changes, pricing shifts
- Synthesis agent produces weekly or monthly competitive intelligence briefing
- Human reviews and uses briefing for strategic planning

**Inputs:** List of peer organizations and monitoring targets, research parameters, briefing format

**Gregory skill:** Not yet built — Early Returns is a proof-of-concept for this architecture
**Status:** Documented. Early Returns demonstrates this pattern at a sophisticated level. Adaptable for association competitive intelligence.

---

## Agentic Systems Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| AGENT-A | Membership Intelligence System | Not built | Documented — requires AMS API |
| AGENT-B | Conference Content Pipeline | Not built | Documented — workflow library foundation exists |
| AGENT-C | Media Monitoring & Communications | Not built | Documented |
| AGENT-D | Research & Competitive Intelligence | Not built | Documented — Early Returns proof-of-concept |

*Agentic systems represent the ceiling of what's possible — not the starting point. Gregory's value is in meeting organizations where they are and building toward this tier as capability and trust develop. The lifecycle map exists to show the full range: from a better renewal email to a fully autonomous membership intelligence system. Both are real. Both are worth building toward.*

---



*Scaled content production is not a lifecycle stage — it is a capability that applies wherever high-volume, formatted, branded output is required. It is one of the most viscerally convincing AI demonstrations available: watching 600 session submissions become publication-ready descriptions in an hour, or a single campaign brief become 20 segmented email variants, makes the value of AI immediately concrete to even the most skeptical participant.*

*The difference between Stage 2 content work and scaled production is volume and format. Stage 2 is drafting one newsletter. Scaled production is generating 40 personalized email variants, 12 ad unit copy sets, and 300 course descriptions — in the same afternoon.*

---

### SCALE-A. Segmented Email Production

**What it is:** Generating multiple variants of an email — or a full sequence — personalized for different audience segments, in a single pass from one brief or data source.

**Where it lives:** Cross-stage — applies to Stage 3 campaigns, Stage 4 retention, Stage 5 event promotion

**How we do it:**
- Define segments and the variable factors for each (message emphasis, tone, offer, CTA)
- Build a single master brief or template
- Generate all variants in one pass, maintaining brand voice across segments
- Output formatted and labeled for easy handoff to email platform

**Inputs:** Campaign brief, audience personas, segmentation logic, brand platform

**What comes out:**
- `[org]-[campaign]-emails-segmented.md` — all variants organized by segment with subject lines, preview text, body, CTA

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — one of the clearest demonstrations of AI's volume advantage over manual production.

---

### SCALE-B. Ad Unit Copy Production

**What it is:** Generating copy for multiple ad formats and placements — digital display, social paid, search, retargeting — from a single campaign brief. Each unit has its own character count, CTA, and format constraint.

**Where it lives:** Cross-stage — Stage 3 campaigns, membership recruitment, event promotion

**How we do it:**
- Define campaign message and offer from campaign brief
- Specify all required formats with character counts and constraints
- Generate copy for each unit: headline, body, CTA, display URL
- Produce multiple headline and body variations for A/B testing
- Flag where visual direction is needed

**Inputs:** Campaign brief, ad specifications by platform, brand platform, landing page copy

**What comes out:**
- `[org]-[campaign]-ad-copy.md` — all ad units organized by platform and format, with variants

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — character-constrained copywriting at volume is a natural Claude task.

---

### SCALE-C. Course & CE Content Production

**What it is:** Generating publication-ready descriptions, learning objectives, speaker bios, and catalog copy for continuing education courses — at the volume associations typically manage (dozens to hundreds of courses per cycle).

**Where it lives:** Cross-stage — Stage 2 content, Stage 5 conference education programming

**How we do it:**
- Take raw course submissions or outlines as input
- Generate: course description (attendee-facing), learning objectives (formatted to CE standards), speaker bio (consistent length and style), catalog metadata
- Apply brand voice and CE credit language requirements
- Flag submissions that are too thin to work from without more input

**Inputs:** Raw course submissions, CE credit standards, brand platform, catalog format requirements

**What comes out:**
- `[org]-ce-catalog-[cycle].md` — full catalog copy for all courses, publication-ready

**Gregory skill:** Not yet built — workflow #3 and #4 in the Gregory workflow library are direct predecessors
**Status:** Documented. High AI leverage, high volume, high time savings. One of the strongest workshop demonstrations.

---

### SCALE-D. Conference Wayfinding & Signage Copy

**What it is:** Generating the copy for all conference signage — room labels, directional signs, session titles for monitors, sponsor recognition, wayfinding — from the session schedule and venue map.

**Where it lives:** Cross-stage — Stage 5, but often falls through the cracks between event logistics and marketing

**Why it's here:** Wayfinding copy is tedious, high-volume, and brand-relevant — and it almost always gets done at the last minute by someone who isn't a writer. AI can generate a complete first draft from the session schedule in minutes, consistent and on-brand.

**How we do it:**
- Take session schedule, room assignments, and venue layout as inputs
- Generate: room sign copy, session title display copy, directional signage text, sponsor recognition copy, welcome signage
- Apply conference brand voice
- Format for sign production vendor specifications

**Inputs:** Final session schedule with room assignments, venue map, sponsor list, brand platform, sign specifications

**What comes out:**
- `[org]-[event]-wayfinding-copy.md` — all signage copy organized by location and type

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage, underappreciated use case — strong workshop demonstration precisely because it's unglamorous work everyone recognizes.

---

### SCALE-E. Social Content Batches

**What it is:** Generating 2–4 weeks of social content across platforms in a single session — from a content calendar, campaign brief, or source material — rather than writing posts one at a time.

**Where it lives:** Cross-stage — Stage 2 ongoing content, Stage 3 campaign support, Stage 5 event promotion

**How we do it:**
- Define the content period, themes, and any campaign overlaps
- Identify source material: announcements, articles, member stories, statistics, event details
- Generate platform-specific posts for each piece of source material: LinkedIn, Instagram, X, Facebook
- Include alt text, hashtag suggestions, and notes for visual assets needed

**Inputs:** Content calendar, source material, brand platform, copy/voice guide, platform specifications

**What comes out:**
- `[org]-social-[month].md` — full monthly content batch organized by platform and date

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — batch production is significantly faster than one-at-a-time drafting.

---

### SCALE-F. Template & Boilerplate Library

**What it is:** A library of reusable copy blocks — boilerplate descriptions, standard disclaimers, recurring section copy, approved language for sensitive topics — that staff can pull from rather than rewrite every time.

**Where it lives:** Cross-stage — referenced across all content production

**Why it matters:** Most associations have staff rewriting the same boilerplate dozens of times a year — the AIA mission statement, the conference hotel block copy, the CE credit disclaimer, the membership benefit description. A curated library of approved, on-brand blocks eliminates that waste and improves consistency.

**How we do it:**
- Audit existing content for recurring copy blocks
- Identify highest-frequency reuse candidates
- Write approved versions of each block at multiple lengths where needed (full / short / social)
- Organize into searchable library

**Inputs:** Existing content archive, brand platform, copy/voice guide

**What comes out:**
- `[org]-boilerplate-library.md` — organized library of approved copy blocks by category and length

**Gregory skill:** Not yet built
**Status:** Documented. Medium AI leverage for initial creation; high value for ongoing reuse. Pairs well with the copy/voice guide (1D).

---

## Content Production at Scale Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| SCALE-A | Segmented Email Production | Not built | Documented — high priority |
| SCALE-B | Ad Unit Copy Production | Not built | Documented |
| SCALE-C | Course & CE Content Production | Not built | Documented — workflow library #3/#4 |
| SCALE-D | Conference Wayfinding & Signage Copy | Not built | Documented — strong demo candidate |
| SCALE-E | Social Content Batches | Not built | Documented |
| SCALE-F | Template & Boilerplate Library | Not built | Documented |

*Scaled production is where the volume advantage of AI becomes undeniable. A participant who isn't convinced by "AI can help you write better" will be convinced by "AI just did in 20 minutes what would have taken your team three days."*

---

## Beyond the Lifecycle: AI-Powered Tools & Products

*Everything in this document so far describes AI-assisted work — a human uses Claude to produce a deliverable faster and better. There is a second category that sits beyond the lifecycle: AI-powered products. Tools built with AI that run on their own and serve an audience directly, without a human in the loop for each interaction.*

*These are not covered in Gregory's intensive — they require a different skill set, different infrastructure, and a different engagement model. They are named here because they are the natural next question from participants who have mastered the lifecycle. The intensive is the foundation. These are what you build on top of it.*

**Examples:**
- **Member-facing chatbot** — answers benefit, policy, event, and CE questions 24/7 without staff involvement
- **Staff knowledge base** — internal tool that answers brand, HR, and process questions on demand
- **Conference assistant** — real-time schedule, wayfinding, and speaker questions during the event
- **Advocacy monitor** — watches legislation and surfaces relevant alerts to the right member segments automatically
- **Membership recommendation engine** — surfaces the right benefits, programs, and connections based on career stage and engagement history
- **Research assistant** — synthesizes member data and external research on demand for leadership

*These tools are built with the same foundation — Claude, structured data, well-designed prompts — that the intensive teaches. The intensive is where you learn to think this way. The tools are where that thinking compounds.*

---

## Stage 1: Brand & Identity

*Before you write anything, you need to know who you are and who you're talking to. This stage is typically done once and revisited every 3–5 years — or when leadership changes, a merger happens, or the member base shifts.*

---

### 1A. Brand Discovery & Intake

**What it is:** A structured process for collecting the raw material that feeds brand development — before any writing begins. Used when existing materials are thin, outdated, or don't reflect what leadership actually believes. The alternative entry point to the brand platform for organizations that can't be researched from the outside in.

**Where it lives:** Stage 1, upstream of brand platform — feeds directly into 1B

**How it works:**
- Key stakeholders complete a structured survey (board members, senior staff, chapter leaders, member representatives)
- Survey instrument draws on established brand methodology: Golden Circle (why/how/what), Brand Pyramid (attributes → benefits → values → personality → essence), Collins & Porras core ideology (purpose, values, BHAG)
- Optional: existing materials (website, annual report, strategic plan) scanned first to pre-populate known facts and identify gaps the survey needs to fill
- Responses synthesized by Claude: consensus surfaces, tensions flagged, vague or generic language called out
- First-draft brand platform generated from synthesis, returned to stakeholders for feedback
- Iterative review until final

**Survey distribution options:**
- Google Form or Typeform (online, asynchronous — good for distributed leadership teams)
- PDF or printed form (returned by email or in person — good for board members who prefer it)
- Facilitated session (Gregory or internal lead walks stakeholders through questions together)

**Established frameworks this draws on:**
- Simon Sinek — Golden Circle (Why / How / What)
- Collins & Porras — Core ideology (purpose separate from strategy)
- Brand Pyramid — Unilever/Ogilvy/Y&R convention
- Stakeholder interview protocols — standard practice at Landor, Interbrand, Siegel+Gale

**Human judgment required:**
- Survey instrument design and question selection
- Weighting stakeholder responses (a board chair and a chapter president may say different things)
- Identifying which tensions reflect genuine strategic ambiguity vs. simple misalignment
- Facilitating feedback loops with leadership

**What comes out:**
- Completed survey responses (raw input)
- Synthesis memo — where stakeholders agree, where they diverge, what's unresolved
- First-draft brand platform (feeds into 1B process)

**Gregory skill:** Not yet built — facilitated process, not self-serve
**Status:** Documented, not productized. Include in workshop as context for participants whose organizations need foundational alignment before brand work can begin.

---

### 1B. Brand Platform

**What it is:** The foundational document that defines organizational identity — mission, vision, values, positioning, brand promise, messaging hierarchy, voice, and audience profiles. The source of truth that every communicator references before writing anything.

**Where it lives:** Stage 1, organizational track

**How we do it:**
- Research primary web properties: homepage, about/mission, membership, advocacy, conference, newsroom
- Identify what the organization says about itself vs. what it actually does
- Surface proof points, differentiators, and competitive context
- Flag generic positioning ("category language") that could apply to any association
- Apply two-voice tests: (1) Could any other association say this? (2) Is there a specific fact that proves this claim?
- Synthesize into structured brand platform document
- Flag gaps between current copy (AS WRITTEN) and recommended positioning (RECOMMENDED)

**Inputs:** Existing website, conference site, member benefit pages, annual reports, strategic plans, any existing brand guidelines

**Human judgment required:**
- Which differentiators to lead with
- Competitive positioning decisions
- Whether recommended language aligns with leadership's intent
- Internal political sensitivities (e.g., not stepping on advocacy team's turf)

**What comes out:**
- `[org]-brand-platform-annotated.md` — working document with AS WRITTEN / RECOMMENDED flags
- `[org]-brand-platform.md` — clean version, all recommendations accepted, ready for designers and communicators

**Gregory skill:** `.claude/skills/brand-platform/SKILL.md`
**AIA example:** `.claude/skills/brand-platform/examples/aia/`

---

### 1C. Audience Personas

**What it is:** Profiles of the distinct audiences the organization serves, with enough specificity to inform message prioritization, channel selection, and content tone. Not marketing fiction — derived from actual member behavior and data.

**Where it lives:** Stage 1, audience track (parallel to brand platform, not sequential)

**How we do it:**
- Identify what member data exists: category breakdowns, tenure distribution, survey results, email segment performance, event attendance, renewal rates by segment
- Map career stage to membership category where possible
- Synthesize behavioral patterns and motivational drivers by segment
- Draft proto-personas for team to react to rather than build from scratch
- Validate against team's direct knowledge of the member base

**Inputs:** Membership database exports, survey results, email analytics, renewal/lapse data, event registration data, any existing persona work

**Human judgment required:**
- Which segments are strategically important vs. merely large
- What the data can't tell you (motivations, barriers, identity)
- How granular to go — too many personas is as useless as too few

**What comes out:**
- `[org]-audience-personas.md` — 4–8 persona profiles with demographic anchor, career context, primary motivation, key barrier, preferred channel, and message priority
- Optional: `[org]-member-journey.md` — how each persona moves through the membership lifecycle

**Gregory skill:** Not yet built

**AIA personas (illustrative career-stage arc):**
- Student member (architecture school, pre-graduation)
- Emerging professional (0–5 years, pre-licensure)
- Associate AIA (pursuing ARE / AXP, licensing path)
- Licensed architect (newly licensed, establishing practice)
- Mid-career AIA (10–20 years, project leadership)
- Senior AIA / Fellow (20+ years, firm leadership, legacy building)
- Firm owner / principal (business concerns as much as practice concerns)

*Note: NCARB has a captive relationship with students and pre-licensure architects through the AXP and ARE. AIA's value proposition at those stages needs to be distinct from NCARB's — belonging and community, not credentialing.*

---

### 1D. Copy & Voice Guide

**What it is:** The practical companion to the brand platform. Where the brand platform defines positioning and personality, the copy/voice guide gives writers concrete rules: word choices, sentence rhythm, what to avoid, examples of on-brand vs. off-brand copy.

**Where it lives:** Stage 1, bridges into Stage 2

**How we do it:**
- Derive from brand platform personality and voice sections
- Audit existing copy for patterns (what the organization actually sounds like vs. what it aspires to)
- Define the spectrum: formal/informal, technical/accessible, institutional/human
- Write positive and negative examples for each context type

**Inputs:** Brand platform, existing copy samples, any existing style guides

**What comes out:**
- `[org]-copy-voice-guide.md`

**Gregory skill:** Not yet built (AIA example exists as artifact)
**AIA example:** Available from previous session (artifact: `aia-copy-voice-guide.md`)

---

### 1E. Competitive Landscape Review

**What it is:** A structured look at how peer organizations position themselves — what they claim, what they emphasize, what language they use — so the brand platform can stake out distinct territory rather than echo the field.

**Where it lives:** Stage 1, feeds into brand platform and positioning statement

**How we do it:**
- Identify 4–6 peer or competitive organizations (similar mission, overlapping audience, or direct competition for membership dollars and attention)
- Research each organization's homepage, about/mission, membership value proposition, and tagline
- Map positioning claims across all organizations — where the field clusters, where there's open territory
- Flag language that appears across multiple organizations (category language — avoid)
- Identify white space: what no one is claiming that this organization could credibly own

**Inputs:** List of peer organizations, their websites

**Human judgment required:**
- Which organizations are actually competitive vs. merely adjacent
- Whether white space is unclaimed because it's valuable or because it's unappealing
- How aggressive to be in differentiation

**What comes out:**
- `[org]-competitive-landscape.md` — positioning map across peer set, white space analysis, language to avoid

**Gregory skill:** Not yet built
**Status:** Documented. Claude Code can research and synthesize; human judgment required for strategic interpretation.

---

### 1F. Naming & Tagline Review

**What it is:** An assessment of whether the organization's name, acronym, and tagline are doing their job — communicating what the organization is, to whom, and why it matters. Not a rebranding exercise; a diagnostic.

**Where it lives:** Stage 1, follows brand platform

**How we do it:**
- Evaluate name and acronym against brand platform: does it reflect current positioning or a legacy one?
- Audit tagline against two-voice tests: could any other organization say this? Does it make a specific promise?
- Review how name and tagline perform across contexts: email subject lines, conference signage, spoken introduction, social bio
- Flag gaps and recommend refinements (rarely wholesale changes)

**Inputs:** Brand platform, current tagline, any existing naming rationale

**Human judgment required:**
- Whether naming issues are worth addressing vs. working around
- Organizational appetite for change (name changes are politically costly)

**What comes out:**
- `[org]-naming-tagline-assessment.md` — diagnostic with specific recommendations

**Gregory skill:** Not yet built
**Status:** Documented. Primarily human judgment; Claude assists with research and draft language.

---

### 1G. Brand Architecture

**What it is:** A map of how the organization's sub-brands, programs, certifications, chapters, and conferences relate to the parent brand — and a governing framework for naming, visual relationships, and messaging hierarchy across the full portfolio. The foundation for integrated marketing.

**Where it lives:** Stage 1, follows brand platform — prerequisite for any integrated marketing effort

**Why it's foundational for integrated marketing:** You cannot run an integrated marketing program if your portfolio is fragmented. When the annual conference has its own identity disconnected from the parent brand, when programs are named inconsistently, when chapters operate as independent fiefdoms — every campaign requires extra explanation and every member touchpoint dilutes rather than reinforces brand equity. Brand architecture solves this by establishing the rules that make integration possible.

**Why it matters for associations specifically:** Most associations have accumulated sub-brands over decades with no governing logic. A certification program launched in 1998 has its own logo. A conference rebranded in 2008 without reference to the parent. A new digital platform launched last year chose its own name without consulting anyone. The result is a portfolio that confuses members and forces staff to constantly explain what connects to what.

**AIA example:** AIA, AIAU, Conference on Architecture, AIA Contract Documents, ArchiPac — five distinct identities, varying degrees of relationship to the parent brand, no explicit governing framework documented in the brand platform.

**The three architecture models:**
- **Monolithic (branded house)** — everything under the parent brand. AIA Conference on Architecture, AIA Contract Documents, AIA Foundation. Strong parent brand equity flows to everything. Less flexibility for sub-brands to develop distinct personalities.
- **Endorsed** — sub-brands have their own identity but carry the parent's endorsement. "Conference on Architecture, an AIA event." Parent brand provides credibility; sub-brand has room to breathe.
- **Pluralistic (house of brands)** — sub-brands operate independently with no visible parent connection. Rare for associations; more common in corporate portfolios. High maintenance cost.

**How we do it:**
- Inventory all named entities: programs, certifications, events, publications, platforms, chapters, foundations, political action committees
- Map current visual and verbal relationships to parent brand — what exists, what's implied, what's inconsistent
- Assess parent brand equity: is the parent brand strong enough to lend value to sub-brands, or do sub-brands need to stand on their own?
- Select architecture model appropriate to organizational strategy
- Draft naming conventions and relationship rules for the portfolio
- Apply rules to existing portfolio: what changes, what stays, what phases out
- Document rules for future additions: how new programs get named, how they relate to the parent

**Inputs:** Full portfolio inventory, existing brand guidelines, brand platform, member research on brand awareness by program

**Human judgment required:**
- Architecture model selection — strategic and political decision, not just analytical
- Change management — existing sub-brands have internal champions and external equity; changes require stakeholder management
- Sequencing — what changes immediately vs. what phases in over time
- Visual identity implications — brand architecture changes often trigger design work

**What comes out:**
- `[org]-portfolio-inventory.md` — complete inventory of all named entities with current brand relationship mapped
- `[org]-brand-architecture.md` — chosen model, naming conventions, relationship rules, application to existing portfolio, rules for future additions
- `[org]-brand-architecture-summary.md` — one-page summary for leadership and board alignment

**Gregory skill:** Not yet built
**Status:** Documented. Higher complexity than most Stage 1 skills — requires significant human facilitation and stakeholder alignment. Claude assists with inventory, mapping, and rules documentation. Strong workshop candidate for senior marketing leaders and CMOs.

*Note: Brand architecture is the prerequisite for integrated marketing. An organization cannot run a campaign that meaningfully connects membership, education, advocacy, and conference without first establishing that those things are visibly part of the same family. This is why it belongs in Stage 1 — not as administrative housekeeping, but as strategic infrastructure.*

---

### 1H. Visual Identity Brief

**What it is:** A written brief that defines what the visual identity should communicate, feel, and accomplish — before any design work begins. Not the design itself. The document that makes good design possible.

**Where it lives:** Stage 1, follows brand platform — hands off to designers

**Why it matters:** Most associations brief designers with a logo and a vague directive ("make it feel more modern"). A visual identity brief derived from the brand platform gives designers a specific target: the personality, the audience, the competitive context, the things the identity must communicate that the current one doesn't.

**How we do it:**
- Derive directly from brand platform: personality, positioning, audience profiles
- Define visual communication objectives: what should someone feel within 3 seconds of seeing this identity?
- Document what the current identity communicates vs. what it should communicate
- Include competitive visual landscape (what others look like — what to avoid, what to differentiate from)
- Define non-negotiables and open territory

**Inputs:** Brand platform, current visual identity, competitive landscape review

**Human judgment required:**
- Aesthetic direction and references
- What existing equity (if any) to preserve
- Designer selection and relationship management

**What comes out:**
- `[org]-visual-identity-brief.md` — written brief for design team or agency

**Gregory skill:** Not yet built
**Status:** Documented. Claude drafts from brand platform inputs; human refines before handing to designers.

---

### 1I. Internal Brand Launch

**What it is:** The process of socializing the new brand platform with staff, board, and key stakeholders before it goes external. Brand platforms fail most often not in the market but inside the organization — when staff don't understand it, don't believe it, or weren't part of it.

**Where it lives:** Stage 1, follows brand platform finalization — precedes any external rollout

**How we do it:**
- Develop internal presentation of brand platform: what changed, why, what it means for each team's work
- Create quick-reference materials for staff (one-pagers, talking points, FAQ)
- Facilitate internal Q&A or workshop session
- Identify internal champions in each department

**Inputs:** Final brand platform, org chart, understanding of internal culture and politics

**Human judgment required:**
- How to handle staff who are attached to old positioning
- How much detail different audiences need
- Sequencing: who hears it first

**What comes out:**
- `[org]-internal-brand-presentation.md` — slide outline or talking points
- `[org]-brand-quickref.md` — one-page staff reference card

**Gregory skill:** Not yet built
**Status:** Documented. Claude assists with materials; facilitation is human.

---

### 1J. Brand Governance

**What it is:** The rules, roles, and processes that keep the brand consistent after launch. Who owns brand decisions. What requires approval. How the brand platform gets updated. What happens when someone violates it.

**Where it lives:** Stage 1, final step before brand is considered operational

**Why associations get this wrong:** Brand governance is usually either absent (everyone does what they want) or over-engineered (a brand police function that creates resentment). The right model is lightweight and practical — clear enough that staff can make good decisions without asking permission every time.

**How we do it:**
- Define brand decision categories: no approval needed / team lead approval / brand owner approval
- Identify brand owner (usually CMO, Director of Marketing, or Communications VP)
- Document update cadence: when does the brand platform get reviewed?
- Create escalation path for edge cases

**Inputs:** Brand platform, org structure, existing approval workflows

**Human judgment required:**
- How much control vs. flexibility the organization culture can support
- Who has the authority and bandwidth to be brand owner

**What comes out:**
- `[org]-brand-governance.md` — decision framework, roles, update cadence

**Gregory skill:** Not yet built
**Status:** Documented. Template-driven; Claude assists with drafting.

---

### 1K. Brand Measurement Baseline

**What it is:** A definition of what brand success looks like and a baseline measurement taken before any brand changes go external — so the organization can know whether the brand is working over time.

**Where it lives:** Stage 1, final step — also connects forward to Stage 6 (Measurement & Reporting)

**What to measure:**
- Unaided awareness — do target audiences know the organization exists?
- Brand perception — what attributes do people associate with the organization?
- Message recall — which messages land, which don't
- Net Promoter Score (member NPS specifically)
- Share of voice — in media, in social, relative to peer organizations

**How we do it:**
- Define 3–5 measurable brand KPIs relevant to organizational goals
- Identify existing data that can serve as proxy baseline (NPS from last member survey, media mentions, website traffic to about/membership pages)
- Note gaps where new measurement is needed
- Set 12-month and 36-month targets

**Inputs:** Existing member survey data, NPS scores, media monitoring, website analytics, social analytics

**Human judgment required:**
- Which metrics actually matter to leadership
- What's realistic to measure given staff and budget
- How to present brand metrics to a board that thinks in membership numbers

**What comes out:**
- `[org]-brand-measurement-baseline.md` — KPI definitions, current baseline, targets

**Gregory skill:** Not yet built
**Status:** Documented. Claude assists with framework and data synthesis; human sets targets and interprets.

---

## Stage 1 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 1A | Brand Discovery & Intake | Not built | Documented — facilitated process |
| 1B | Brand Platform | Built ✓ | AIA example complete |
| 1C | Audience Personas | Not built | Documented |
| 1D | Copy & Voice Guide | Not built | AIA example exists |
| 1E | Competitive Landscape Review | Not built | Documented |
| 1F | Naming & Tagline Review | Not built | Documented |
| 1G | Brand Architecture | Not built | Documented |
| 1H | Visual Identity Brief | Not built | Documented |
| 1I | Internal Brand Launch | Not built | Documented |
| 1J | Brand Governance | Not built | Documented |
| 1K | Brand Measurement Baseline | Not built | Documented |

*Not every association needs all eleven. The brand platform (1B) is the anchor. Everything else depends on where the organization is and what it's trying to accomplish.*

---

## Stage 2: Content & Voice

*With brand and audience defined, the organization can produce content that is consistent, differentiated, and targeted. This is where most marketing teams spend most of their time — and where Claude Code delivers the most immediate productivity gains. The shift from Stage 1 to Stage 2 is from "who are we" to "what do we say, to whom, and when."*

---

### 2A. Content Strategy & Editorial Calendar

**What it is:** A plan for what content the organization will produce, for which audiences, on which channels, and when. The bridge between brand platform and execution.

**Where it lives:** Stage 2, foundational — everything else in this stage flows from it

**How we do it:**
- Map audience personas to content needs and consumption habits
- Identify content categories aligned to messaging hierarchy (from brand platform)
- Define channel mix: email, web, social, print, events
- Establish publishing cadence by channel
- Build 12-month editorial calendar with themes, campaigns, and evergreen content

**Inputs:** Brand platform, audience personas, program/event calendar, prior year content inventory

**Human judgment required:**
- Which content categories to prioritize given staff capacity
- How aggressive to be on channels where the audience is but the org has no presence
- How to balance organizational priorities with what members actually want

**What comes out:**
- `[org]-content-strategy.md` — strategic framework, channel rationale, content categories
- `[org]-editorial-calendar.md` — 12-month calendar with themes and deliverables

**Gregory skill:** Not yet built
**Status:** Documented. Claude can draft framework from brand platform inputs; human populates specific dates and organizational priorities.

---

### 2B. Website Copy

**What it is:** The copy for key website pages — homepage, about/mission, membership value proposition, program pages — rewritten to reflect the brand platform.

**Where it lives:** Stage 2, highest-visibility content deliverable

**Why it matters:** The website is usually the most read-and-ignored content asset in any association. Most association websites read as institutional catalogs rather than member recruitment tools. The brand platform exists to fix this — but someone has to rewrite the pages.

**How we do it:**
- Audit existing pages against brand platform: what's misaligned, what's missing, what's generic
- Prioritize pages by traffic and conversion importance
- Draft revised copy for each priority page, applying voice and messaging hierarchy
- Flag where copy requires factual input from staff (program details, statistics, quotes)
- Annotate with rationale for each change

**Inputs:** Brand platform, copy/voice guide, current website, Google Analytics (page traffic and bounce rates)

**Human judgment required:**
- Final approval on positioning language
- Accuracy of program details and statistics
- Sensitivity to internal stakeholders who own specific pages

**What comes out:**
- `[org]-website-copy-audit.md` — page-by-page gap analysis
- `[org]-[pagename]-copy.md` — revised copy for each priority page, annotated

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — Claude can draft full page copy from brand platform inputs with minimal human setup.

---

### 2C. Email Sequences

**What it is:** Multi-email sequences for key member lifecycle moments — welcome series for new members, onboarding for first-year members, renewal series, lapsed member re-engagement, event promotion.

**Where it lives:** Stage 2, high-frequency content deliverable — also connects to Stage 4

**How we do it:**
- Define trigger and goal for each sequence (what event starts it, what action it drives)
- Map sequence length and timing (e.g., welcome series: 5 emails over 30 days)
- Draft each email: subject line, preview text, body, CTA
- Apply persona-specific variants where segments exist
- Write plain-text versions alongside HTML

**Inputs:** Brand platform, copy/voice guide, audience personas, current email templates, ESP platform (Informz, Mailchimp, HubSpot, etc.)

**Human judgment required:**
- Sequence length and timing — organizational norms and member tolerance
- CTA design — what action is realistic at each stage
- Integration with existing email platform and automation rules

**What comes out:**
- `[org]-[sequence-name]-emails.md` — full sequence with subject lines, body copy, CTAs, timing notes

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — one of the clearest workflow opportunities in this stage.

---

### 2D. Social Media Content

**What it is:** On-brand social content for the organization's active channels — LinkedIn, Instagram, X, Facebook — adapted for each platform's format and audience behavior.

**Where it lives:** Stage 2, ongoing content deliverable

**How we do it:**
- Define channel strategy: which platforms, what role each plays, what content categories belong where
- Draft content batches (typically 2–4 weeks of posts) from source material: blog posts, member stories, program announcements, advocacy wins, statistics
- Adapt each piece for platform: LinkedIn long-form vs. Instagram visual caption vs. X short-form
- Write alt text for images
- Flag content that needs visual assets

**Inputs:** Brand platform, copy/voice guide, content calendar, source material (articles, announcements, event info)

**Human judgment required:**
- Voice calibration — social tends to be warmer and less formal than other channels
- What's appropriate to post during sensitive news cycles
- Approval workflow before publishing

**What comes out:**
- `[org]-social-content-[month].md` — monthly content batch, organized by platform and date

**Gregory skill:** Not yet built
**Status:** Documented. Medium AI leverage — drafting is fast, but platform judgment and timing require human oversight.

---

### 2E. Thought Leadership Content

**What it is:** Long-form content that establishes the organization's authority and perspective — articles, white papers, op-eds, research summaries, member spotlights, blog posts.

**Where it lives:** Stage 2, brand-building content — feeds media relations and search

**How we do it:**
- Identify thought leadership topics aligned to messaging hierarchy and member interests
- Research existing data, reports, and perspectives the org can credibly own
- Draft content from source material: interviews, research, policy positions
- Adapt for target outlet: association publication, trade press, general business media
- Write executive bylines from interview notes or talking points

**Inputs:** Brand platform, messaging hierarchy, staff/member interview notes, existing research, policy positions

**Human judgment required:**
- Which topics the organization can credibly own vs. merely comment on
- Executive review and approval for bylined content
- Relationship management with editors and publications

**What comes out:**
- `[org]-[topic]-article.md` — draft article with sourcing notes
- `[org]-thought-leadership-calendar.md` — 12-month topic plan

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for drafting from source material; human required for original insight and approval.

---

### 2F. Member Communications

**What it is:** Routine communications to the full membership or specific segments — newsletters, announcements, advocacy alerts, benefit reminders, program updates.

**Where it lives:** Stage 2, ongoing — highest-volume content category for most associations

**How we do it:**
- Establish templates for each communication type aligned to brand platform
- Draft routine communications from source material and organizational calendar
- Apply audience segmentation where relevant
- Maintain consistent voice across high volume

**Inputs:** Brand platform, copy/voice guide, organizational calendar, program updates, staff input

**Human judgment required:**
- What rises to the level of member communication vs. website update
- Tone calibration during sensitive moments (advocacy issues, leadership transitions)
- Final approval

**What comes out:**
- `[org]-newsletter-template.md` — reusable newsletter structure
- `[org]-[date]-newsletter.md` — individual newsletter drafts

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for routine drafting; human for editorial judgment.

---

## Stage 2 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 2A | Content Strategy & Editorial Calendar | Not built | Documented |
| 2B | Website Copy | Not built | Documented |
| 2C | Email Sequences | Not built | Documented — high priority |
| 2D | Social Media Content | Not built | Documented |
| 2E | Thought Leadership Content | Not built | Documented |
| 2F | Member Communications | Not built | Documented |

---

## Stage 3: Campaigns & Programs

*Structured, time-bound marketing efforts with defined goals: membership recruitment drives, annual fund appeals, award programs, certification promotion, advocacy calls to action. Campaigns are Stage 2 content in formation — same raw material, organized around a deadline and a conversion goal.*

---

### 3A. Campaign Brief

**What it is:** The strategic document that defines a campaign before any creative work begins — goal, audience, message, channels, timeline, success metrics. The brief everyone on the team works from.

**Where it lives:** Stage 3, upstream of all campaign execution

**How we do it:**
- Define campaign goal in specific, measurable terms (not "increase awareness" — "generate 200 new member applications in Q1")
- Select target audience from persona set
- Pull relevant messages from messaging hierarchy
- Define channel mix and timeline
- Establish success metrics and reporting cadence

**Inputs:** Brand platform, audience personas, organizational goals, program calendar, prior campaign results

**Human judgment required:**
- Goal-setting — what's realistic given history and resources
- Budget allocation across channels
- Internal alignment before launch

**What comes out:**
- `[org]-[campaign-name]-brief.md` — one-page campaign brief

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — Claude can generate a first-draft brief from brand platform and goal inputs quickly.

---

### 3B. Membership Recruitment Campaign

**What it is:** A structured campaign to acquire new members — targeted to non-members who match the profile of current members, or to specific segments the organization wants to grow.

**Where it lives:** Stage 3, highest-priority campaign category for most associations

**How we do it:**
- Define target segment (lapsed members, students graduating into professional membership, geographic targets, firm employees not yet individually joined)
- Develop campaign message from membership value proposition
- Build multi-touch sequence: awareness → consideration → conversion
- Write copy for each channel: email, social, paid, event, direct outreach
- Define offer if applicable (trial, discount, peer referral)

**Inputs:** Campaign brief, brand platform, membership value proposition, target list, prior campaign benchmarks

**Human judgment required:**
- Offer design — what incentive is appropriate without cheapening membership
- List selection and suppression
- Compliance with data privacy requirements

**What comes out:**
- `[org]-membership-recruitment-[year].md` — full campaign with copy for each channel and touchpoint

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for copy production across channels once brief is set.

---

### 3C. Renewal Campaign

**What it is:** The annual (or rolling) campaign to retain expiring members — the highest-ROI marketing activity for most associations, almost always underdeveloped.

**Where it lives:** Stage 3, connects forward to Stage 4

**How we do it:**
- Map the renewal timeline: first notice, second notice, expiration, grace period, lapse
- Develop message sequence that escalates urgency without becoming transactional
- Write persona-specific variants where segment data exists (early-career vs. senior members renew for different reasons)
- Design win-back sequence for members who lapse despite the renewal series

**Inputs:** Campaign brief, brand platform, audience personas, renewal timeline, current renewal rates by segment

**Human judgment required:**
- How aggressive to be on urgency messaging
- Whether to offer a discount and at what stage
- How to handle members on payment plans or hardship waivers

**What comes out:**
- `[org]-renewal-campaign-[year].md` — full renewal sequence with timing, subject lines, body copy, CTAs

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — one of the clearest high-value workflow opportunities in Gregory's portfolio.

---

### 3D. Event/Conference Promotion Campaign

**What it is:** The campaign that drives registration for the annual conference or major events — typically the second-largest revenue driver after membership dues.

**Where it lives:** Stage 3, connects forward to Stage 5

**How we do it:**
- Map the promotional timeline from save-the-date through post-event
- Develop message arc: awareness → program reveal → speaker announcements → early bird → regular registration → last chance
- Write copy for each stage and channel
- Develop audience-specific messaging (first-time attendees vs. returning, members vs. non-members)
- Build post-event re-engagement sequence

**Inputs:** Campaign brief, event details, speaker lineup, program highlights, prior year attendance data, registration platform

**Human judgment required:**
- Timing of announcements (speaker reveals, program announcements)
- Pricing and discount strategy
- Integration with event team's own communications

**What comes out:**
- `[org]-[event-name]-promotion-[year].md` — full promotional campaign with timeline and copy

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for copy production; human required for event-specific details and timing.

---

### 3E. Advocacy Campaign

**What it is:** A campaign that mobilizes members to take a specific action on a legislative or regulatory matter — contacting elected officials, submitting public comments, signing a petition, attending a fly-in.

**Where it lives:** Stage 3, requires close coordination with government affairs/advocacy team

**How we do it:**
- Define the specific ask: what action, by when, to whom
- Develop the case in member-relevant terms (not policy language — member impact language)
- Write the call-to-action sequence: alert, follow-up, thank you/results
- Adapt for channels: email, social, website, direct outreach
- Track response rates and report to leadership

**Inputs:** Policy brief from government affairs team, member impact analysis, action timeline, advocacy platform (VoterVoice, Phone2Action, etc.)

**Human judgment required:**
- Policy accuracy — copy must be reviewed by government affairs staff
- Tone — advocacy copy walks a line between urgency and partisanship
- Timing relative to legislative calendar

**What comes out:**
- `[org]-[issue]-advocacy-campaign.md` — alert copy, follow-up sequence, thank you message

**Gregory skill:** Not yet built
**Status:** Documented. Medium AI leverage — drafting is fast but policy accuracy requires government affairs review at every step.

---

## Stage 3 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 3A | Campaign Brief | Not built | Documented — high priority |
| 3B | Membership Recruitment Campaign | Not built | Documented |
| 3C | Renewal Campaign | Not built | Documented — high priority |
| 3D | Event/Conference Promotion Campaign | Not built | Documented |
| 3E | Advocacy Campaign | Not built | Documented |

---

## Stage 4: Member Engagement & Retention

*The ongoing work of keeping members active, connected, and renewing. Not campaigns — the steady state. The difference between a member who renews automatically and one who needs to be persuaded every year is almost entirely determined by what happened in between. This stage is chronically underfunded and underbuilt in most associations.*

---

### 4A. New Member Onboarding

**What it is:** The structured experience that turns a new member into an engaged one — within the first 90 days, when the decision to renew is effectively made.

**Where it lives:** Stage 4, highest-leverage engagement investment

**How we do it:**
- Map the new member journey: join → confirm → welcome → first engagement → habit formation
- Design onboarding sequence: email series, benefit introduction, community connection, early win
- Write copy for each touchpoint
- Define success metric: what does an "activated" new member look like? (logged in, attended an event, made a connection, used a benefit)

**Inputs:** Brand platform, audience personas, membership benefits inventory, current welcome sequence if any, activation rate data

**Human judgment required:**
- Which benefits to lead with for each persona
- How much to ask of a new member before they've seen value
- Integration with membership database and email platform

**What comes out:**
- `[org]-new-member-onboarding.md` — full onboarding sequence with copy, timing, and activation metrics

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — clear workflow with defined inputs and outputs.

---

### 4B. Member Benefits Audit & Communication

**What it is:** A systematic review of which benefits members are aware of, which they're using, and which are invisible — followed by a targeted communication plan to close the gap.

**Where it lives:** Stage 4, feeds renewal and reduces lapse

**Why it matters:** Most associations have more member value than members know about. The benefits exist; the communication doesn't. An audit surfaces where the gap is largest, and targeted communication fills it before renewal season.

**How we do it:**
- Inventory all member benefits with usage data where available
- Segment by awareness (do members know it exists?) vs. utilization (are they using it?)
- Identify highest-value underutilized benefits — the ones most likely to drive renewal if surfaced
- Develop targeted benefit highlight sequence: email, social, in-newsletter features
- Track utilization lift post-communication

**Inputs:** Benefits inventory, usage data from AMS/LMS/event platform, member survey data, renewal correlation analysis if available

**Human judgment required:**
- Which benefits are genuinely valuable vs. legacy benefits no one uses
- How to present benefits without sounding like a sales pitch to existing members
- Data access and integration across platforms

**What comes out:**
- `[org]-benefits-audit.md` — benefits inventory with awareness/utilization gaps flagged
- `[org]-benefits-communication-plan.md` — targeted sequence for underutilized high-value benefits

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for synthesis and copy; human required for data access and benefit evaluation.

---

### 4C. Lapsed Member Re-engagement

**What it is:** A campaign targeting members who did not renew — within a window when re-engagement is still possible (typically 3–12 months post-lapse).

**Where it lives:** Stage 4, last line of defense before a member is lost

**How we do it:**
- Segment lapsed members by tenure, category, and last engagement (recent lapse is more recoverable than long-lapse)
- Develop re-engagement message: acknowledge the lapse, remind of value, make returning easy
- Write sequence: initial outreach, follow-up, final offer, close
- Define win-back offer if applicable
- Track re-engagement rate and revenue recovered

**Inputs:** Lapsed member list with segmentation data, renewal history, last engagement date, brand platform, membership value proposition

**Human judgment required:**
- Tone — re-engagement copy must not feel transactional or guilt-inducing
- Offer design — what's worth offering to re-activate without setting a bad precedent
- When to stop the sequence and accept the lapse

**What comes out:**
- `[org]-lapsed-member-reengagement.md` — full sequence with segmentation logic, copy, and timing

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for copy; human required for segmentation logic and offer design.

---

### 4D. Member Survey & Feedback Analysis

**What it is:** The design, distribution, and synthesis of member surveys — satisfaction, needs assessment, benefit utilization, NPS — turned into actionable findings rather than slide decks that get filed.

**Where it lives:** Stage 4, feeds strategy across all stages

**How we do it:**
- Design survey instrument aligned to strategic questions (not a kitchen-sink survey)
- Write clear, unbiased question copy
- Analyze results: segment by persona, tenure, category
- Synthesize findings into strategic recommendations
- Draft board/leadership presentation from findings

**Inputs:** Strategic questions the organization needs answered, prior survey results, AMS data for segmentation

**Human judgment required:**
- Question design — what to ask and what not to ask
- How to present findings that challenge leadership assumptions
- Survey fatigue management — how often and how long

**What comes out:**
- `[org]-survey-instrument.md` — draft survey questions with rationale
- `[org]-survey-findings.md` — synthesized findings with strategic recommendations

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for synthesis and presentation drafting; human required for question design and strategic interpretation.

---

## Stage 4 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 4A | New Member Onboarding | Not built | Documented — high priority |
| 4B | Member Benefits Audit & Communication | Not built | Documented |
| 4C | Lapsed Member Re-engagement | Not built | Documented |
| 4D | Member Survey & Feedback Analysis | Not built | Documented |

---

## Stage 5: Events & Conferences

*Events are the highest-touch member experience and the most labor-intensive marketing operation in most associations. The annual conference is often the largest revenue line after dues — and the one where the brand is most viscerally felt. This stage has its own internal lifecycle: planning → promotion → on-site → post-event.*

---

### 5A. Call for Speakers / Abstract Review

**What it is:** The process of soliciting, reviewing, and selecting session proposals for the annual conference or other events.

**Where it lives:** Stage 5, first step in conference content development — typically 8–12 months before the event

**How we do it:**
- Draft call for speakers copy — what the conference is looking for, submission requirements, review criteria
- Design submission form categories aligned to conference themes
- Review submitted abstracts against criteria: relevance, speaker credibility, audience appeal, topic freshness
- Score and rank abstracts
- Draft acceptance and decline communications

**Inputs:** Conference themes and strategic goals, prior year program, submission platform (Cadmium, ex Ordo, OpenWater, etc.), review criteria

**Human judgment required:**
- Final speaker selection — AI scoring informs but doesn't decide
- Diversity and balance across the program
- Relationship management with declined speakers

**What comes out:**
- `[org]-call-for-speakers-[year].md` — call for speakers copy and submission guidance
- `[org]-abstract-review-scoring.md` — scoring rubric and ranked results
- `[org]-speaker-acceptance-decline-emails.md` — communication templates

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for abstract review and scoring at scale; human makes final selections.

---

### 5B. Session Descriptions & Program Copy

**What it is:** The polished session descriptions, speaker bios, and program copy that appear in the conference app, website, and printed materials — rewritten from raw speaker submissions.

**Where it lives:** Stage 5, follows speaker selection

**Why it matters:** Raw speaker submissions are almost universally written for the review committee, not the attendee. Polished session descriptions written for the attendee — what they'll learn, why it matters, what they'll be able to do differently — drive session attendance and satisfaction scores.

**How we do it:**
- Rewrite each session description in attendee-facing language: benefit-led, specific, jargon-free
- Edit speaker bios for consistency and appropriate length
- Write program intro copy (conference theme, opening remarks, track descriptions)
- Apply conference voice and brand

**Inputs:** Accepted speaker abstracts and bios, conference themes, brand platform, prior year program

**Human judgment required:**
- Review with speakers before publishing — some will push back on rewrites
- Accuracy of speaker credentials
- Final approval from conference team

**What comes out:**
- `[org]-[event]-session-descriptions-[year].md` — all polished session descriptions and bios

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — one of the clearest high-volume content tasks in the conference lifecycle.

---

### 5C. Attendee Communication Sequence

**What it is:** The end-to-end sequence of communications to registered attendees from confirmation through post-event — logistics, program highlights, engagement prompts, follow-up.

**Where it lives:** Stage 5, runs from registration through 2 weeks post-event

**How we do it:**
- Map communication timeline: confirmation, pre-event series (4–6 weeks out through day before), on-site communications, post-event follow-up
- Write each touchpoint: what to communicate, why, what action to prompt
- Personalize where possible (first-time vs. returning, session selections, hotel status)
- Write post-event survey and follow-up content

**Inputs:** Conference details, registration platform data, session schedule, speaker roster, hotel and logistics information

**Human judgment required:**
- Timing relative to program announcement schedule
- What to communicate vs. what to let attendees discover
- Tone calibration — conference communications should feel warmer than routine membership communications

**What comes out:**
- `[org]-[event]-attendee-communications-[year].md` — full sequence with timing and copy

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for copy production; human required for logistics accuracy and timing.

---

### 5D. Post-Event Content Repurposing

**What it is:** Turning conference content — session recordings, presentations, key takeaways, speaker quotes — into ongoing content assets that extend the event's value throughout the year.

**Where it lives:** Stage 5, bridges into Stage 2

**How we do it:**
- Identify highest-value sessions for repurposing based on attendance and feedback scores
- Transcribe or summarize session content
- Develop derivative content: article from session, social quote cards from speaker remarks, newsletter feature on key themes, white paper from research-heavy sessions
- Write on-demand/recorded session promotional copy for members who didn't attend

**Inputs:** Session recordings or transcripts, presentation decks, attendee feedback scores, conference themes

**Human judgment required:**
- Speaker permission for repurposed content
- Which sessions have content worth extending vs. which were time-sensitive
- Quality threshold for published content

**What comes out:**
- `[org]-[event]-content-repurposing-plan.md` — prioritized repurposing plan with content formats and assignments

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for content drafting from transcripts; human required for speaker relations and quality control.

---

## Stage 5 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 5A | Call for Speakers / Abstract Review | Not built | Documented — high AI leverage at scale |
| 5B | Session Descriptions & Program Copy | Not built | Documented — high priority |
| 5C | Attendee Communication Sequence | Not built | Documented |
| 5D | Post-Event Content Repurposing | Not built | Documented |

---

## Stage 6: Measurement & Reporting

*Closing the loop. Measurement is where most association marketing teams are weakest — not because they lack data, but because they lack time to synthesize it into something useful. This is one of the highest-leverage applications of AI in the entire lifecycle: turning data into narrative, narrative into decisions.*

---

### 6A. Marketing Dashboard & Narrative

**What it is:** A regular (monthly or quarterly) report that synthesizes marketing performance data across channels into a clear narrative — what's working, what isn't, what to do about it.

**Where it lives:** Stage 6, recurring deliverable

**Why it matters:** Most marketing dashboards are data dumps. Leaders don't need more numbers — they need interpretation. Claude can turn a spreadsheet of metrics into a narrative that a board member can read in 5 minutes and understand.

**How we do it:**
- Establish standard metric set by channel (email: open rate, click rate, conversion; web: sessions, bounce rate, conversion; membership: new joins, renewals, lapse rate; events: registration, attendance, satisfaction)
- Pull data from source platforms
- Synthesize into narrative: what moved, why it likely moved, what it means for next period
- Flag anomalies and recommend actions

**Inputs:** Email platform metrics, web analytics, AMS membership data, event registration data, social analytics, prior period benchmarks

**Human judgment required:**
- Contextualizing anomalies (was the email spike because of great copy or a news event?)
- Setting benchmarks — what's good for this organization specifically
- Decisions that follow from the data

**What comes out:**
- `[org]-marketing-dashboard-[period].md` — narrative report with key metrics and recommendations

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — narrative generation from structured data is a core Claude capability.

---

### 6B. Board Report

**What it is:** The marketing section of the regular board report — written for a non-marketing audience, focused on strategic implications rather than tactical metrics.

**Where it lives:** Stage 6, typically quarterly

**How we do it:**
- Translate marketing metrics into business outcomes (not "email open rate increased 4%" — "membership inquiry volume is up 18% year over year, ahead of recruitment campaign launch")
- Connect marketing activity to organizational goals
- Flag risks and opportunities at the strategic level
- Keep to 1–2 pages — board members do not read long reports

**Inputs:** Marketing dashboard, organizational strategic goals, prior board report

**Human judgment required:**
- What to surface and what to omit — board time is limited
- How to frame underperformance honestly without alarming unnecessarily
- Final approval by CMO or ED

**What comes out:**
- `[org]-board-report-marketing-[period].md` — 1–2 page board section draft

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage — translating operational data into executive narrative is a natural Claude task.

---

### 6C. Campaign Post-Mortem

**What it is:** A structured review of each major campaign after it concludes — what the goal was, what was executed, what the results were, what to do differently next time.

**Where it lives:** Stage 6, follows each major campaign — feeds into next campaign brief

**How we do it:**
- Compare results to goals defined in campaign brief
- Identify which elements performed (subject lines, channels, offers, timing)
- Document what was learned for institutional memory
- Generate recommendations for next iteration

**Inputs:** Campaign brief, execution record, results data from all channels

**Human judgment required:**
- Honest assessment of what went wrong without finger-pointing
- Separating execution failures from strategic failures
- Deciding what to change vs. what to give more time

**What comes out:**
- `[org]-[campaign-name]-postmortem.md` — structured review with results, findings, and recommendations

**Gregory skill:** Not yet built
**Status:** Documented. Medium AI leverage — Claude can structure and draft; human must provide honest assessment.

---

### 6D. Annual Marketing Review

**What it is:** A comprehensive annual review of marketing performance — results against goals, key learnings, strategic recommendations for the coming year. The input to next year's planning.

**Where it lives:** Stage 6, annual — bridges back to Stage 2 and 3 planning

**How we do it:**
- Aggregate full-year data across all channels and campaigns
- Assess performance against annual goals
- Identify 3–5 key strategic learnings
- Develop recommendations for next year's priorities, budget allocation, and capability investments
- Draft presentation for leadership and board

**Inputs:** Full-year metrics, all campaign post-mortems, prior year review, organizational strategic plan

**Human judgment required:**
- Strategic interpretation — what the data means for organizational direction
- Budget recommendations — requires organizational financial context
- Leadership alignment before presenting to board

**What comes out:**
- `[org]-annual-marketing-review-[year].md` — comprehensive review document
- `[org]-annual-marketing-review-[year]-presentation.md` — slide outline for leadership presentation

**Gregory skill:** Not yet built
**Status:** Documented. High AI leverage for synthesis and drafting; human required for strategic interpretation and budget context.

---

### 6E. Benchmark Analysis

**What it is:** A comparison of the organization's marketing performance against peer associations and industry benchmarks — used to calibrate goals and identify where performance is genuinely strong vs. where it lags the field.

**Where it lives:** Stage 6, annual or as-needed

**How we do it:**
- Identify relevant benchmark sources: Marketing General Incorporated (MGI) Membership Marketing Benchmarking Report, Informz email benchmarks, M+R Nonprofit Benchmarks, ASAE data
- Pull organization's metrics for the same measures
- Compare and contextualize: where are we above benchmark, at benchmark, below?
- Identify the gaps most worth closing given organizational strategy

**Inputs:** Organization's own metrics, published benchmark reports, peer data where available

**Human judgment required:**
- Which benchmarks are actually relevant to this organization's size and type
- How to present benchmark gaps without demoralizing the team
- Whether underperformance reflects a problem or a strategic choice

**What comes out:**
- `[org]-benchmark-analysis-[year].md` — comparative analysis with contextualized findings

**Gregory skill:** Not yet built
**Status:** Documented. Medium AI leverage — Claude can structure analysis; benchmark data requires human sourcing.

---

## Stage 6 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 6A | Marketing Dashboard & Narrative | Not built | Documented — high priority |
| 6B | Board Report | Not built | Documented — high AI leverage |
| 6C | Campaign Post-Mortem | Not built | Documented |
| 6D | Annual Marketing Review | Not built | Documented |
| 6E | Benchmark Analysis | Not built | Documented |

---

### 6F. Advanced Member Analytics

**What it is:** Sophisticated analysis of member value over time — lifetime value, customer equity, cohort retention, product profitability vs. customer profitability. The metrics that connect marketing performance to organizational financial health.

**Where it lives:** Stage 6, advanced — requires data infrastructure and analytical maturity most associations haven't built yet

**Why it's on the map:** Most associations measure activity (how many emails sent, how many members joined) rather than value (what is a member worth over their lifetime, which segments are most profitable to acquire and retain). The shift from activity metrics to value metrics is a strategic leap — and one that positions an organization to make better budget and program decisions.

**Key concepts:**
- **Customer lifetime value (LTV)** — the total revenue a member generates over their full membership tenure, discounted to present value
- **Customer profitability** — revenue minus cost-to-serve by member segment; not all members are equally profitable
- **Customer equity** — sum of lifetime values across the entire membership; the brand's financial value to the organization
- **Cohort analysis** — tracking how different joining classes (2019 cohort, 2022 cohort) retain and engage over time; reveals whether the member experience is improving
- **Acquisition ROI by channel** — which recruitment channels produce members who stay vs. members who lapse after year one

**How we do it:**
- Define LTV model appropriate to the organization: dues revenue + event revenue + education revenue + ancillary revenue, minus cost-to-serve
- Pull historical data by member cohort from AMS
- Build cohort retention curves
- Segment by acquisition channel, membership category, geographic region, career stage
- Synthesize into strategic recommendations: where to invest in acquisition, which benefits drive retention, which segments to prioritize

**Inputs:** Multi-year AMS export with revenue by member and transaction type, program cost data, acquisition channel data

**Human judgment required:**
- Model design — which revenue streams to include, how to estimate cost-to-serve
- Strategic interpretation — what the numbers mean for budget and program decisions
- Board-level communication of financial implications

**What comes out:**
- `[org]-member-ltv-model.md` — LTV framework and assumptions
- `[org]-cohort-analysis.md` — retention curves by cohort and segment
- `[org]-advanced-analytics-summary.md` — strategic findings and recommendations

**Gregory skill:** Not yet built
**Status:** Documented. Requires significant data infrastructure; most appropriate for large associations with mature AMS data. Positions Gregory as capable of the full analytical range — not just content production.

*Note: This level of analysis was standard practice at AIA. It is not yet standard practice at most associations — which makes it both a differentiator for Gregory and a growth opportunity for clients ready to invest in it.*

---

## Stage 6 Summary

| # | Deliverable | Gregory Skill | Status |
|---|-------------|---------------|--------|
| 6A | Marketing Dashboard & Narrative | Not built | Documented — high priority |
| 6B | Board Report | Not built | Documented — high AI leverage |
| 6C | Campaign Post-Mortem | Not built | Documented |
| 6D | Annual Marketing Review | Not built | Documented |
| 6E | Benchmark Analysis | Not built | Documented |
| 6F | Advanced Member Analytics | Not built | Documented — large association / Gregory positioning |

---

## Documentation Template

*Use this template for each Gregory skill or workflow added to this repository.*

---

### [Skill or Workflow Name]

**Type:** Skill / Workflow / Template  
**Status:** In development / Complete / Needs update  
**Last updated:** [date]

**Lifecycle stage:** Stage [N] — [Stage Name]  
**Track:** Organizational / Audience / Content / Campaign / Engagement / Events / Measurement

**What it does:**
[One paragraph. What task does this address? What problem does it solve?]

**Inputs required:**
- [What the user needs to bring]
- [Data sources, existing documents, URLs]

**How it works:**
[Step-by-step method. What does Claude Code actually do? What research does it conduct? What judgments does the human need to make?]

**Human judgment checkpoints:**
- [Where the human must review, decide, or validate]

**Output:**
- `filename.md` — [description]
- `filename-annotated.md` — [description if applicable]

**Where output lives:**
`[repo]/[path]/`

**Example:**
`[repo]/[path]/examples/[org]/`

**Known limitations:**
- [What this skill can't do or doesn't handle well]

**Related skills:**
- [Links to upstream or downstream skills]

---

## Cross-Stage: Product & Program Development

*Product and program development is where AI moves from efficiency and optimization into innovation — the highest tier of value. Everything else in this lifecycle makes existing work faster and better. This section is about using AI to discover and develop things that don't exist yet: new member benefits, new certification programs, new publications, new revenue streams.*

*Most associations launch new programs based on gut instinct, board enthusiasm, or staff initiative — rarely on rigorous member needs research. AI changes the research economics enough that evidence-based product development becomes practical for organizations that couldn't afford it before.*

**This section is a placeholder.** Entries will be developed as Gregory's workshop practice matures and client demand signals which product development workflows are most valuable to build.

**Anticipated entries include:**
- Member needs research and synthesis
- Concept validation (AI-assisted survey design and analysis)
- Program brief and business case development
- Competitive program analysis
- Go-to-market planning for new offerings
- Pricing analysis and positioning
- Pilot program design and measurement

**Gregory skill:** Not yet built
**Status:** Placeholder — expansion candidate as Gregory's practice develops.

---

## A Framework for Thinking About AI in Association Marketing

*Everything in this document can be organized along two dimensions: where it sits in the lifecycle, and what kind of value it delivers. Greg Appler, founder of Gregory, uses three categories:*

**Efficiency** — doing the same work faster with less effort. Email drafting, meeting notes, status reports, boilerplate copy. The immediate win. Every association can benefit here regardless of size or sophistication.

**Optimization** — doing existing work better, with more precision and personalization. Segmented campaigns, renewal sequences tailored by tenure, session descriptions written for attendees rather than review committees. Requires some data and process maturity.

**Innovation** — doing things that weren't practical before. Agentic membership intelligence systems, AI-powered member chatbots, evidence-based product development at a fraction of traditional research costs. Requires technical infrastructure and organizational trust in AI outputs.

*The lifecycle map covers all three tiers. Gregory workshops meet participants where they are — and show them where they can go.*

---

*Document maintained in `gappler/gregory-workshop`. Questions: greg@gregoryco.ai*
