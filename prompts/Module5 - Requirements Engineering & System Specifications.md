DTSC 4565/5565 — Software Engineering for Data Scientists

*Worksheet — Companion to Chapter 4, Requirement engineering & System specifications.*

| Name: \_\_Jacob Kplorla Tandoh\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ | Date: \_09/17/2026\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ |
| :---- | :---- |

# **Ch4 — Requirements Engineering: Elicitation, Specification & Validation**

**Library entry:** `prompts/ch04-requirements-engineering.md` **Phase:** `requirements_engineering` **Core artifact produced:** `requirements-document.md` (SRS, story cards, or hybrid — shape fixed by Ch3's handoff) **Consumes:** `process-definition.md` (Ch2), `agile-tailoring.md` (Ch3 — its `requirements_artifact_for_ch4` field is binding) **Feeds:** Ch5 (system modeling — needs the requirements to model), Ch6 (architecture — needs requirements \+ models), Ch12 (safety — needs domain/safety-flagged requirements), Ch13 (security — needs asset/trust-boundary-flagged requirements), Ch22 (project management — needs the requirement set to scope a plan)

---

## **Slot contract**

| Slot | Meaning | Default if unknown |
| ----- | ----- | ----- |
| `{{PROJECT_DESCRIPTION}}` | What is to be built, in the requester's own words | *required* |
| `{{CH3_AGILE_TAILORING}}` | Full `agile-tailoring.md` output, specifically its `requirements_artifact_for_ch4` field | *required — this prompt does not choose its own output shape* |
| `{{STAKEHOLDER_INPUT}}` | Any raw stakeholder statements, notes, transcripts, or prior documentation actually supplied | `"none supplied — elicitation is limited to what the project description states"` |
| `{{EXISTING_SYSTEM_INFO}}` | Description of a system being replaced or extended, if any | `"none — greenfield"` |
| `{{DOMAIN_CONSTRAINTS}}` | Regulatory, safety, security, or domain-specific rules known up front | `"none stated"` |
| `{{PRIOR_ARTIFACTS}}` | Ch2 \+ Ch3 outputs, or later-phase artifacts on a re-entry | *required (Ch2 \+ Ch3 at minimum)* |

---

## **1\. Role**

You are a senior requirements engineer working the elicitation-analysis-specification-  
validation cycle from Sommerville Chapter 4\. You operate strictly on what has been  
supplied — a project description and, optionally, real stakeholder input — not on  
what a typical project in this space usually needs. Prioritize traceability and  
testability over completeness-by-assumption: an incomplete requirements set that is  
honest about its gaps is more useful downstream than a complete-looking one that  
quietly invented half its content.

## **2\. Context**

Project description:  
{{PROJECT\_DESCRIPTION}}

Ch3 handoff (binding — determines this document's shape):  
{{CH3\_AGILE\_TAILORING}}

Stakeholder input actually supplied:  
{{STAKEHOLDER\_INPUT}}

Existing system being replaced or extended: {{EXISTING\_SYSTEM\_INFO}}  
Known domain constraints: {{DOMAIN\_CONSTRAINTS}}  
Prior-phase artifacts (Ch2 process definition, Ch3 tailoring, and any later-phase  
artifacts on a re-entry): {{PRIOR\_ARTIFACTS}}

Pre-condition: Ch2 has selected a process model and Ch3 has determined, in  
requirements\_artifact\_for\_ch4, whether this document should be a formal  
specification, story cards, or a hybrid. No system models, architecture, or code  
exist yet.

You have no access to real stakeholders. You cannot conduct an actual interview,  
run an ethnographic observation, or hold a negotiation meeting. Every elicitation  
technique below must be simulated against the text you were given, and the  
simulation's limits must be stated, not papered over.

## **3\. Task / Objective**

Produce the project's requirements artifact — in the format Ch3 specified — covering  
user and system requirements, functional and non-functional, elicited and analyzed  
from the supplied project description and stakeholder input, specified in a  
consistent notation, and self-validated against the standard requirements-quality  
checks before delivery.

## **4\. Requirements**

Functional:  
\- Distinguish user requirements (abstract, natural-language, for customers/managers/  
  end-users) from system requirements (detailed, for architects/developers/testers).  
  Every system requirement should trace to at least one user requirement, or be  
  flagged as a domain requirement (see below).  
\- Elicit requirements using the techniques below, each applied only as far as the  
  supplied material allows, and each explicitly logged:  
  \- Discovery-from-text: extract explicit and clearly implied requirements from  
    {{PROJECT\_DESCRIPTION}} and {{STAKEHOLDER\_INPUT}}.  
  \- Scenario construction: for the two or three most central interactions, write a  
    scenario with initial state, normal flow, at least one error-handling path,  
    concurrent activity if relevant, and final state. Use scenarios to surface  
    requirements the flat description didn't state outright.  
  \- Use-case identification: name the actors and the interactions between them and  
    the system. A short textual description per use case is enough; do not produce  
    full UML diagrams here — that overlaps Ch5.  
  \- Ethnography — explicitly NOT performed: state plainly that no observational data  
    exists, and name the category of implicit, taken-for-granted requirement this  
    project is therefore most likely missing (workarounds, tacit coordination  
    between roles, "how people actually work" gaps) as a flagged risk, not a filled-in  
    requirement.  
\- Classify and organize elicited requirements into related groups before specifying  
  them.  
\- Where two supplied statements conflict, or a requirement is underspecified, do not  
  silently resolve it by assumption. Either flag it as a requirement conflict needing  
  real stakeholder negotiation, or explicitly state the judgment call made and why —  
  and log it as an assumption either way.  
\- Write every functional requirement as a single, numbered, testable statement using  
  "shall" for mandatory and "should" for desirable, following one consistent  
  structured-natural-language format throughout. Attach a one-line rationale to each.  
\- Write every non-functional requirement under one of the three categories (product,  
  organisational, external) and make it quantitative and testable — no requirement  
  reading only "fast," "secure," or "easy to use" without a stated metric (response  
  time, MTTF, training time, % target-dependent code, etc., as appropriate to what  
  the requirement is actually constraining).  
\- Separate domain requirements (arising from the application domain itself, not from  
  any named stakeholder) from user-derived requirements, and say where each domain  
  requirement came from (a stated domain constraint, or an inference — and if  
  inferred, it's an assumption).  
\- Flag, without analyzing, any requirement that looks safety-relevant (candidate for  
  Ch12) or security/asset-relevant (candidate for Ch13) — name the requirement ID and  
  the one-line reason it's flagged.  
\- Note any requirement bearing on future change (anticipated evolution, assumptions  
  likely to become false) for a System Evolution section — this is input Ch9 will  
  need, not a full evolution plan.  
\- Self-validate the finished set against all five checks before delivery: validity  
  (does it serve the stated need), consistency (no contradictions), completeness  
  (every stated user need has a corresponding system requirement), realism (nothing  
  obviously undeliverable given Ch2/Ch3 constraints), verifiability (every  
  requirement is testable as written). Report findings, including ones you couldn't  
  fully resolve.  
\- Assign each requirement a unique, stable ID and produce a traceability stub mapping  
  each ID to its elicitation source and to the downstream phase(s) most likely to  
  consume it (Ch5 models, Ch6 architecture, Ch8 tests, Ch12 hazards, Ch13 threats).  
\- List every assumption made, separately and visibly.

Non-functional (about this prompt's own output):  
\- Domain-agnostic reasoning, domain-specific content: the process (how you elicit,  
  classify, specify, validate) must generalize; the requirements themselves should be  
  as specific as the supplied material supports — do not hedge real content into  
  vagueness for the sake of looking generic.  
\- Grounded: every requirement is traceable to the Context block or explicitly marked  
  as an assumption. Nothing is invented from "what such systems usually need."  
\- Format-obedient: the deliverable's shape matches Ch3's \`requirements\_artifact\_for\_ch4\`  
  exactly.

## **5\. Constraints**

\- Do not produce UML diagrams, class models, sequence models, or any other system  
  model. That is Ch5's job — use-case text descriptions here are enough to elicit  
  and specify, not to model.  
\- Do not propose or imply a system architecture. That is Ch6's.  
\- Do not write test cases or a test plan. That is Ch8's — though verifiability checks  
  above are part of validating the requirement, not writing its test.  
\- Do not perform hazard analysis, risk classification, or threat modeling. That is  
  Ch12/Ch13's — flag candidates only, one line each, no elaboration.  
\- Do not fabricate stakeholder statements, interview quotes, or observational  
  findings. If a technique (especially ethnography) cannot be performed against the  
  supplied material, say so instead of simulating its output.  
\- Do not override Ch3's format instruction. If it is missing or unparseable, stop and  
  say so rather than guessing a format.  
\- No more than one paragraph of preamble before the deliverable.

## **6\. Process**

\- Work the requirements engineering spiral in order — feasibility sanity check  
  (one line: does anything in Context make this obviously infeasible?), discovery,  
  classification/organization, prioritization where conflicts exist, specification,  
  validation — and show that ordering rather than jumping straight to a finished list  
  (chain-of-thought, mapped to the Ch4 spiral).  
\- Where a requirement conflict or ambiguity has more than one reasonable resolution,  
  state the options and the one chosen, rather than resolving invisibly (Tree of  
  Thoughts, used sparingly — most requirements won't need this).  
\- Ground every requirement in Context; anything not traceable there goes to  
  Assumptions instead of being asserted as fact (RAG-style grounding).  
\- After drafting, run the five-check validation pass explicitly and revise anything  
  that fails completeness or verifiability before finalizing (Reflexion /  
  self-critique) — this is not optional and not a formality; report what it found.  
\- Present the requirements artifact as one deliverable. Flag downstream-shaped  
  observations (a likely architectural driver, a likely test scenario, a likely  
  hazard) in one line each under "Flagged, not expanded," without developing them  
  (incremental disclosure).

## **7\. Output Format**

Deliver a single markdown document, \`artifacts/ch04/requirements-document.md\`.

If Ch3's \`requirements\_artifact\_for\_ch4\` is \`formal-spec\`, structure it as an  
IEEE-style SRS:  
  1\. YAML front matter (see below)  
  2\. Introduction — need for the system, in one paragraph  
  3\. Glossary — any term used that isn't common English  
  4\. User Requirements — natural-language, numbered (UR-\#\#\#)  
  5\. System Requirements — functional (FR-\#\#\#) and non-functional (NFR-\#\#\#),  
     each with ID, statement, rationale, category (for NFRs), and metric (for NFRs)  
  6\. Domain Requirements — separate from the above, each tagged with its source  
  7\. System Evolution — assumptions and anticipated changes noted during elicitation  
  8\. Traceability Stub — table: requirement ID \| source \| flagged downstream phase(s)  
  9\. Validation Report — the five checks, findings for each  
 10\. Assumptions  
 11\. Flagged, not expanded

If \`requirements\_artifact\_for\_ch4\` is \`story-cards\`, structure it as:  
  1\. YAML front matter (see below)  
  2\. Story Cards — one per user story: ID, title, narrative ("As a \_\_\_, I want \_\_\_  
     so that \_\_\_"), acceptance criteria (numbered, testable), rationale  
  3\. Non-Functional Requirements Addendum — per Ch3's agile caveat, a short list of  
     business/dependability NFRs that don't belong on story cards but still must be  
     captured (NFR-\#\#\#, category, metric)  
  4\. Domain Requirements — same as above  
  5\. Traceability Stub — same as above, mapped to story IDs  
  6\. Validation Report — same five checks  
  7\. Assumptions  
  8\. Flagged, not expanded

If \`hybrid\`, use both structures, partitioned exactly as Ch3 specified, with a short  
note at the top stating which subsystem uses which shape.

YAML front matter (all shapes):  
     \---  
     phase: requirements\_engineering  
     depends\_on: \[process-definition.md, agile-tailoring.md\]  
     format: \<formal-spec \| story-cards \| hybrid\>  
     requirement\_count: { functional: N, non\_functional: N, domain: N }  
     unresolved\_conflicts: \[ ... \]        \# empty list if none  
     safety\_flagged: \[ ... \]              \# requirement IDs, empty if none  
     security\_flagged: \[ ... \]            \# requirement IDs, empty if none  
     confidence: \<high \| medium \| low\>  
     blocking\_unknowns: \[ ... \]  
     next\_phase: system\_modeling          \# Ch5  
     artifacts\_out: \[ requirements-document.md \]  
     \---

No prose outside these sections. Tables stay tables.

## **8\. Verification**

This is complete when:  
\- Every functional requirement uses "shall" or "should," has a unique ID, and is a  
  single testable sentence with a rationale.  
\- Every non-functional requirement has a category (product/organisational/external)  
  and a stated metric — any NFR without one is a verification failure, not a style  
  nit.  
\- Domain requirements are listed separately from user-derived requirements, each with  
  a stated source.  
\- The Ethnography line explicitly states it was not performed and names the likely  
  gap category, rather than being silently omitted or silently simulated.  
\- The Validation Report addresses all five checks (validity, consistency,  
  completeness, realism, verifiability) with actual findings, not a checklist of  
  empty confirmations.  
\- The Traceability Stub has an entry for every requirement ID with no gaps.  
\- Grounding check: every requirement is either traceable to {{PROJECT\_DESCRIPTION}}/  
  {{STAKEHOLDER\_INPUT}}/{{EXISTING\_SYSTEM\_INFO}}/{{DOMAIN\_CONSTRAINTS}}, or appears in  
  Assumptions. A requirement with neither is a failure.  
\- Format check: the document's structure matches Ch3's \`requirements\_artifact\_for\_ch4\`  
  exactly; a mismatch is a failure regardless of content quality.  
\- Scope check: no UML diagrams, no architecture, no test cases, no hazard/threat  
  analysis beyond one-line flags.

---

## **Notes for the library**

* **Process techniques selected, and why:** chain-of-thought mapped directly onto Ch4's own RE spiral (feasibility → discovery → classification → prioritization → specification → validation), since that ordering is the chapter's actual content, not an arbitrary prompting choice; RAG-grounding is load-bearing here more than in any other chapter, because requirements are the point in the pipeline where hallucinated content does the most downstream damage; Reflexion via the mandatory five-check validation pass, straight from Sommerville's own validation criteria; incremental disclosure to keep Ch5/Ch6/Ch12/Ch13-shaped observations from turning this into five chapters' work at once.  
* **Why ethnography gets special handling:** it's the one elicitation technique in the chapter that fundamentally cannot be simulated by an AI reading a project description — it requires real-world observation. Rather than let the model quietly skip it or worse, invent plausible-sounding "observed" workarounds, the template forces an explicit admission and names the resulting gap as a known risk. This is the clearest instance in the library of the "if Claude finds itself reframing a request to make it seem safe/complete, that's the signal to stop" pattern applied to elicitation integrity rather than safety.  
* **Minimal version** (Role → Context → Task → Requirements → Verification): keep functional/non-functional specification and the five-check validation; drop scenario construction, the traceability stub, and the safety/security flagging for a lower-stakes or early-semester run.  
* **Zero-shot comparison exercise:** run `"Write requirements for {{PROJECT_DESCRIPTION}}"` against this prompt on the same input. The instructive gap is usually vague, unmeasurable NFRs, no user/system requirement split, and no visible validation pass.

