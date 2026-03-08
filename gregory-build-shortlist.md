# Gregory Build Shortlist
## Prioritized Skills for Workshop Curriculum

*Generated from the Association Marketing Lifecycle map. Ten skills selected to collectively span all three value tiers, cover the most universally applicable association marketing tasks, and demonstrate the full range of what Claude Code can do for a non-technical marketing team. Ordered by lifecycle sequence — first things first.*

---

## The Three Tiers

**Efficiency** — doing the same work faster with less effort  
**Optimization** — doing existing work better, with more precision and personalization  
**Scale** — producing high volumes of formatted, branded output in a single pass  

---

## Automation Potential

**Low** — Claude produces a document; human takes it from there  
**Medium** — output connects to one other tool or triggers a next step  
**High** — multi-step pipeline; output flows automatically into downstream actions  

---

## The Ten

| # | Skill | Lifecycle Ref | Tier | Integration Required | Automation Potential | Build Priority |
|---|-------|--------------|------|---------------------|----------------------|----------------|
| 1 | Brand Context Setup | 1B / 1D / PM-H | Foundation | None — file setup | Low | Prerequisite |
| 2 | Brand Architecture | 1G | Strategy | Low — web research | Low | High |
| 3 | Creative & Project Brief | PM-D | Efficiency | None | Medium | High |
| 4 | Meeting Notes & Action Items | PM-E | Efficiency | None → High | Low → High | High |
| 5 | Session Descriptions | 5B / SCALE-C | Scale | Low — file input | Medium | High |
| 6 | New Member Onboarding Sequence | 4A | Optimization | Medium — AMS export | High | High |
| 7 | Renewal Campaign | 3C | Optimization | Medium — AMS export | High | High |
| 8 | Board Report — Marketing Section | 6B | Efficiency | Low — data input | Medium | High |
| 9 | Conference Wayfinding & Signage Copy | SCALE-D | Scale | Low — schedule input | Low | Medium |
| 10 | Collaborative Workflows & Version Control | PM-H | Efficiency | GitHub | Medium | Medium |

---

## Notes on Each

**#1 — Brand Context Setup**
The prerequisite. Brand platform, copy/voice guide, and audience personas loaded into the `.claude/brand/` folder with a CLAUDE.md that tells Claude Code when and how to reference them. Without this, every copy skill runs cold. With it, every copy skill runs on-brand from the first prompt. Build this before anything else.

**#2 — Brand Architecture**
Foundational for integrated marketing. A fragmented portfolio — programs, certifications, events, chapters with no governing logic — makes integration impossible. Claude assists with inventory, mapping, and rules documentation. Strong entry point for senior marketing leaders and CMOs. Builds on Brand Context Setup.

**#3 — Creative & Project Brief**
Every project needs one. Almost nobody writes them rigorously. Claude generates a solid first draft from a conversation in minutes, no integration required. **Automation upside:** brief generation can trigger project template creation in Asana or Monday, folder structure setup in GitHub, and timeline generation — turning a 20-minute document task into a fully scaffolded project launch.

**#4 — Meeting Notes & Action Items**
Two very different versions of this skill. **Version 1 (simple):** transcript in, structured notes out. Saves 20 minutes, tier 1 efficiency. **Version 2 (connected):** transcript → notes → action items extracted → tasks created in project management tool → assignments sent via Slack → calendar invites generated → reminders triggered before due dates. The simple version is the entry point. The connected version is the demonstration of what automation multiplies.

**#5 — Session Descriptions**
Highest visible time savings on the map — 600 raw submissions to publication-ready descriptions in hours. Best single workshop demonstration. Workflow library #3 predecessor already scoped. **Automation upside:** connect to submission platform API for automatic ingestion; output feeds directly to conference app and website CMS.

**#6 — New Member Onboarding Sequence**
The 90-day window where renewal is effectively decided. Most associations have a weak or nonexistent onboarding sequence. Clear inputs, clear outputs, dramatic before/after. **Automation upside:** trigger from AMS new member event → personalized sequence deployed automatically by persona/category → engagement tracked → at-risk members flagged for staff follow-up.

**#7 — Renewal Campaign**
Every association runs one annually. Well-defined inputs, segmented by tenure and persona. Workflow library #2 flags as strong cohort candidate. **Automation upside:** AMS renewal data feeds segmentation automatically → variants deployed by segment → non-responders escalated to win-back sequence → results reported back to AMS. One of the clearest end-to-end automation opportunities in the entire lifecycle.

**#8 — Board Report — Marketing Section**
Turning a spreadsheet of metrics into a 2-page board narrative is something Claude does exceptionally well. Surprises participants because it doesn't feel like "AI content" — it feels like strategic translation. **Automation upside:** connect to analytics platforms for automatic data pull → narrative generated on schedule → formatted for board packet distribution.

**#9 — Conference Wayfinding & Signage Copy**
The unglamorous one. Every conference planner recognizes the pain immediately. Nobody expects AI to solve it. Strong demonstration of "AI handles the tedious so you can do the strategic." Low automation upside but high demonstration value precisely because it's so universal and so underappreciated.

**#10 — Collaborative Workflows & Version Control**
The team multiplier. When brand assets, campaign templates, and Claude Code skills live in a shared GitHub repo, every team member benefits from improvements anyone makes. One person builds a renewal campaign skill — the whole team runs it. Comes last in the build sequence because it's the infrastructure that makes everything else shareable.

---

## The Automation Principle

Several skills on this list exist at two levels: the document and the pipeline. Meeting notes is a 20-minute time saver as a document. It's a workflow transformation as a pipeline connected to Asana, Slack, and Google Calendar.

The workshop teaches the skill first — so participants understand what's possible and can evaluate output quality. Then it shows the automation layer — so participants can see the multiplier. The skill is the starting point. The automation is the leverage.

This is also the progression from Tier 1 to Tier 2 to Tier 3:
- **Tier 1 (efficiency):** Claude produces the document
- **Tier 2 (optimization):** Claude produces the document and triggers the next step
- **Tier 3 (innovation):** An agent team produces, distributes, monitors, and reports — without a human initiating each step

---

## Recommended Build Sequence

1. Brand Context Setup — no build required, just structure and documentation
2. Meeting Notes (simple version) — zero integration, immediate demo value
3. Creative & Project Brief — zero integration, universal application
4. Session Descriptions — high demo value, clear input/output
5. Renewal Campaign — high strategic value, connects to automation story
6. New Member Onboarding — builds on renewal campaign pattern
7. Board Report — surprise factor, senior audience
8. Brand Architecture — strategic depth, senior audience
9. Conference Wayfinding — unglamorous, undeniable
10. Collaborative Workflows / GitHub — infrastructure, comes last

---

## What's Not On This List (Yet)

- **FEC / campaign finance workflow** — Early Returns project, AGENT-D tier, separate build track
- **Member-facing chatbot** — TOOL-A, requires more technical infrastructure
- **Membership intelligence system** — AGENT-A, requires AMS API access
- **Content repurposing pipeline** — workflow library #9, strong candidate once these ten are built
- **Segmented email production at scale** — SCALE-A, natural extension of renewal campaign skill

---

*Maintained in `gappler/gregory-workshop`. Questions: greg@gregoryco.ai*
