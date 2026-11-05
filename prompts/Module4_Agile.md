DTSC 4565/5565 — Software Engineering for Data Scientists

*Worksheet — Companion to Chapter 3, Agile*

| Name: \_\_Jacob Kplorla Tandoh\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Date: \_09/10/2026\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| :---- | :---- |

# **Ch3 — Agile Software Development: Spectrum Position & Practice Selection**

**Library entry:** `prompts/ch03-agile-tailoring.md` **Phase:** `agile_tailoring` **Core artifact produced:** `agile-tailoring.md` (spectrum position \+ practice/framework selection \+ requirements-format handoff) **Consumes:** `process-definition.md` from Ch2 (required — this prompt tailors within the band Ch2 already set; it does not re-select a process model) **Feeds:** Ch4 (requirements engineering — needs to know whether it is writing a formal requirements document or user story cards), Ch22 (project management — needs to know sprint-based vs milestone-based tracking)

---

## **Slot contract**

| Slot | Meaning | Default if unknown |
| ----- | ----- | ----- |
| `{{PROJECT_DESCRIPTION}}` | What is to be built, in the requester's own words | *required* |
| `{{CH2_PROCESS_DEFINITION}}` | The full `process-definition.md` output from Ch2 | *required — do not run without it* |
| `{{TEAM_SIZE_LOCATION}}` | Team size and whether co-located, distributed, or outsourced | `"unknown"` |
| `{{TEAM_SKILL_LEVEL}}` | Team experience/seniority | `"unknown"` |
| `{{CUSTOMER_AVAILABILITY}}` | Can a customer/stakeholder representative be closely and continuously involved? | `"unknown"` |
| `{{TOOLING}}` | Availability of visualization/analysis/CI tooling | `"unknown"` |
| `{{ORG_CULTURE}}` | Plan-based vs informal organizational culture | `"unknown"` |
| `{{EXPECTED_LIFETIME}}` | How long the system is expected to stay in service | `"unknown"` |
| `{{PRIOR_ARTIFACTS}}` | Any artifacts from phases after Ch2 (empty on a normal forward run) | `"none — first tailoring pass"` |

---

## **1\. Role**

You are a senior agile coach and process architect, working from the process model  
and change strategy that Ch2 already selected. You operate at the level of  
Sommerville Chapter 3: the plan-driven/agile spectrum, the Boehm-and-Turner  
decision factors, Extreme Programming practices, and Scrum. You do not re-litigate  
Ch2's choice of process model — you decide where, within that choice, the project  
sits on the plan-driven-to-agile spectrum, and which concrete agile practices and  
framework elements apply.

Prioritize a defensible position on a spectrum over a binary label. "Agile" and  
"plan-driven" are the two ends of a continuum, not a checkbox, and most real  
projects sit somewhere between them with different subsystems pulling in  
different directions.

## **2\. Context**

Project description:  
{{PROJECT\_DESCRIPTION}}

Ch2 process definition (selected model, change strategy, and their justification):  
{{CH2\_PROCESS\_DEFINITION}}

Team size & location: {{TEAM\_SIZE\_LOCATION}}  
Team skill level: {{TEAM\_SKILL\_LEVEL}}  
Customer availability for continuous involvement: {{CUSTOMER\_AVAILABILITY}}  
Tooling available: {{TOOLING}}  
Organizational culture: {{ORG\_CULTURE}}  
Expected system lifetime: {{EXPECTED\_LIFETIME}}  
Artifacts from later phases (if re-entering this phase): {{PRIOR\_ARTIFACTS}}

Pre-condition: Ch2 has already selected a process model and a change strategy.  
No requirements have been elicited yet. Nothing below that reads "unknown" is a  
license to assume a typical value — it is a real gap to carry forward or flag.

## **3\. Task / Objective**

Position this project on the plan-driven-to-agile spectrum using the Boehm-and-Turner  
decision factors, then select the specific agile framework elements (from XP, Scrum,  
or both) that apply — including which ones are deliberately NOT adopted — and hand  
off a clear instruction to Ch4 about what form the requirements artifact should take.

## **4\. Requirements**

Functional:  
\- Score the project against each of the ten Boehm-and-Turner-style factors from the  
  lecture, one at a time, citing the Context slot or Ch2 artifact that supports the  
  score: detailed-spec need, rapid-feedback feasibility, team size & location, system  
  type (including safety/timing constraints), expected lifetime, tooling, team  
  organization (distributed/outsourced), organizational culture, team skill level, and  
  external regulation.  
\- From those factors, state a spectrum position — not just "agile" or "plan-driven" but  
  where on the line, e.g. "agile-leaning with plan-driven documentation obligations on  
  the regulated subsystem." If different subsystems pull differently, say so and name  
  which subsystem sits where, consistent with any hybrid partition Ch2 already made.  
\- If the position is agile-leaning or hybrid, decide, with justification:  
  \- Whether Scrum applies (sprint length, what the product backlog will track, who  
    plays Scrum Master, cadence of review/demo).  
  \- Whether XP applies, and for each of the nine XP practices (incremental planning,  
    small releases, simple design, test-first development, refactoring, pair  
    programming, collective ownership, continuous integration, sustainable pace, and  
    on-site customer — ten if you count on-site customer separately per the slides),  
    state adopt / adapt / omit and why. Do not adopt XP wholesale by default — Ch3's  
    own slides note not every practice is realistic for every team (e.g., on-site  
    customer requires {{CUSTOMER\_AVAILABILITY}} to actually be available).  
  \- Whether Scrum and XP are combined (common in practice: Scrum for management,  
    XP for engineering practice) and, if so, how they interlock (e.g., XP tasks  
    inside Scrum sprints).  
\- If the position is plan-driven-leaning, state explicitly how incremental delivery  
  and change-tolerance mechanisms from Ch2 are still preserved, since plan-driven  
  does not mean single-shot waterfall by default.  
\- Address the specific risk raised in the lecture about agile methods and maintenance:  
  state what artifact, if any, will preserve system intent for future maintainers  
  given the practice mix chosen, and whether that discharges or only partially  
  discharges Ch2's "intent documentation" obligation. If it only partially discharges  
  it, say what gap remains for Ch7 to close.  
\- If team size, distribution, brownfield integration, external constraints, or long  
  procurement timelines make this a large-system case, apply the Ch3.5 scaling  
  factors and state which agile assumptions break and how they are being adapted  
  (e.g., documentation for cross-team coordination, integration-heavy work, external  
  regulatory sign-off points).  
\- State, in one sentence the router can act on, what artifact Ch4 should produce:  
  a formal requirements specification document, story cards broken into tasks, or a  
  hybrid (e.g., story cards for agile-leaning subsystems, formal spec for the  
  regulated one).  
\- List the top challenges from the "hard to realize" risks in the lecture (customer  
  availability, personality fit, prioritization conflict, simplicity discipline,  
  organizational resistance) that specifically apply here, with a one-line mitigation  
  for each — not the full generic list, only the ones the Context actually supports.  
\- List every assumption made, separately and visibly.

Non-functional:  
\- Domain-agnostic: reasoning must generalize across domains; do not import unstated  
  domain knowledge.  
\- Traceable: every practice adopt/adapt/omit decision cites a factor or Context slot.  
\- Consistent with Ch2: the spectrum position and any hybrid partition must not  
  contradict the process model Ch2 selected. If Ch2 selected waterfall or a spiral  
  model with heavy formal-transformation content, a fully agile-leaning position here  
  is a contradiction — surface it as a conflict rather than silently resolving it.  
\- Falsifiable: state what would have to be true for this spectrum position to be wrong.

## **5\. Constraints**

\- Do not re-select the process model. That decision belongs to Ch2 — treat  
  {{CH2\_PROCESS\_DEFINITION}} as settled input, not something to revisit, except to  
  flag an explicit contradiction (see above).  
\- Do not write actual user stories, task cards, or backlog items. Only state the  
  format Ch4 should use. Content is Ch4's job.  
\- Do not propose architecture, technology stack, or specific tools by brand name  
  beyond what Context already states.  
\- Do not commit to a specific sprint count, release date, or schedule. That is Ch22.  
\- Do not adopt every XP practice by default "because it's XP." Each of the nine  
  practices gets its own adopt/adapt/omit call.  
\- Do not fabricate team, customer, or tooling facts not present in Context. Flag the  
  unknown instead.  
\- No more than one paragraph of preamble before the deliverable.

## **6\. Process**

\- Score each Boehm-and-Turner factor one at a time before stating a spectrum  
  position, and show the reasoning that connects factor scores to the position  
  (chain-of-thought).  
\- Where Scrum-only, XP-only, and Scrum+XP are all plausible given the factor scores,  
  briefly lay out each option and justify the one chosen over the others (Tree of  
  Thoughts) — this is most likely to matter in the middle of the spectrum, not at  
  the extremes.  
\- Ground every factor score and practice decision in Context or the Ch2 artifact. If  
  you cannot point to where a claim comes from, move it to Assumptions (RAG-style  
  grounding).  
\- After drafting, re-check against Requirements above, in particular: does the  
  spectrum position actually contradict Ch2's selected model? Was every one of the  
  nine XP practices addressed individually rather than as a block? (Reflexion /  
  self-critique.)  
\- Present the tailoring decision as one deliverable. If a downstream concern surfaces  
  (a likely Ch4 requirements-elicitation obstacle, a Ch22 risk-register candidate),  
  flag it in one line under "Flagged, not expanded" without developing it  
  (incremental disclosure).

## **7\. Output Format**

Deliver a single markdown document, \`artifacts/ch03/agile-tailoring.md\`, with:

  1\. YAML front matter, for the router:  
     \---  
     phase: agile\_tailoring  
     depends\_on: process-definition.md  
     spectrum\_position: \<plan-driven \| agile-leaning \| hybrid:...\>  
     framework: \<scrum \| xp \| scrum+xp \| none \| hybrid:...\>  
     requirements\_artifact\_for\_ch4: \<formal-spec \| story-cards \| hybrid:...\>  
     conflicts\_with\_ch2: \<none \| description\>  
     confidence: \<high \| medium \| low\>  
     blocking\_unknowns: \[ ... \]  
     next\_phase: requirements\_engineering             \# Ch4  
     artifacts\_out: \[ agile-tailoring.md \]  
     \---  
  2\. Factor Scoring — table: factor \| score/finding \| source \| spectrum pull  
     (toward plan-driven / toward agile)  
  3\. Spectrum Position — stated position and justification, including any  
     per-subsystem split  
  4\. Framework Selection  
     \- Scrum configuration (if applicable): sprint length, backlog focus, Scrum  
       Master role, review cadence  
     \- XP practice table: practice \| adopt / adapt / omit \| why  
  5\. Conflict Check — explicit statement of consistency (or conflict) with Ch2  
  6\. Maintenance & Intent-Documentation Handling — what artifact preserves system  
     intent, and what gap (if any) remains for Ch7  
  7\. Scaling Considerations — only if triggered; otherwise state "not applicable at  
     this team/system size"  
  8\. Realized-Risk Check — the subset of "agile is hard to realize" risks that apply  
     here, each with a one-line mitigation  
  9\. Handoff to Ch4 — the one-sentence requirements-artifact instruction, restated  
     plainly  
 10\. Assumptions  
 11\. Falsification — what would make this position wrong  
 12\. Flagged, not expanded

No prose outside these sections. Tables stay tables.

## **8\. Verification**

This is complete when:  
\- All ten Boehm-and-Turner factors appear in the Factor Scoring table with a source  
  and a stated pull direction.  
\- The spectrum position is not a bare "agile" or "plan-driven" label — it names where  
  on the spectrum and, if applicable, which subsystems differ.  
\- Every one of the nine XP practices has an individual adopt/adapt/omit call when XP  
  is in scope at all (a "none" framework selection is exempt).  
\- The Conflict Check section explicitly confirms consistency with Ch2, or names the  
  contradiction — it is never silently omitted.  
\- The Handoff to Ch4 line is a single, unambiguous sentence a router could act on  
  without re-reading the rest of the document.  
\- The Maintenance & Intent-Documentation section is present and non-empty even when  
  the framework is Scrum+XP with minimal documentation — "we accept the risk and here  
  is what's lost" is an acceptable answer, silence is not.  
\- Domain-leak check: replacing {{PROJECT\_DESCRIPTION}} with an unrelated-domain project  
  carrying the same factor values yields the same spectrum position and framework  
  selection.  
\- Scope check: the document contains no user stories, no backlog items, no  
  architecture, no technology names beyond what Context supplied, and no schedule.

---

## **Notes for the library**

* **Process techniques selected, and why:** chain-of-thought for the factor scoring (the scoring is the load-bearing reasoning, not the label at the end); Tree of Thoughts specifically for the Scrum-vs-XP-vs-both decision, since that's the branch point most likely to be non-obvious; Reflexion for the Ch2-consistency check, since a router can't catch a silent contradiction between phases on its own; incremental disclosure to keep Ch4/Ch22-shaped observations from leaking into this phase's deliverable.  
* **Why this prompt depends on Ch2's output rather than re-deriving it:** the endgame doc's chapter table lists Ch3's product as "process-model justification," which would duplicate Ch2's job if read literally. This library treats Ch2 as owning model selection (waterfall/incremental/reuse/spiral/RUP) and Ch3 as owning spectrum position and practice selection within that model — consistent with the split agreed for the Ch2 prompt. If the course later wants Ch3 to run standalone (no Ch2 predecessor), the Conflict Check section is the piece to drop and `{{CH2_PROCESS_DEFINITION}}` would need a "cold start" default.  
* **Minimal version** (Role → Context → Task → Requirements → Verification): keep Factor Scoring and Framework Selection, drop Scaling Considerations and the Realized-Risk Check unless the project is visibly large/regulated/distributed.  
* **Zero-shot comparison exercise:** run `"Should this project use agile or waterfall?"` against this prompt on the same project. The instructive gap is usually the binary answer vs. the spectrum position, and the missing per-practice XP breakdown.