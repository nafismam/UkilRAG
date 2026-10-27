# Slide-by-slide speaking guide

Aim for 3–4 minutes. Ask permission before presenting.

## 1. Why this demonstration

About 35 seconds. “My earlier legal-research contribution covered literature review, problem identification and initial design. I later moved to an LLM inference project while another sub-team continued that work. UkilRAG is a separate recent demonstration exploring the rules, source links and tests in this internship brief.” Earlier work concerned Bangladeshi law, not Italian legal expertise. Do not imply the prototype is the original research implementation. Describe personal implementation work and assistance accurately when discussing ownership.

## 2. How the ideas connect

About 35 seconds. “Earlier research taught me why legal passages need source labels and sensible boundaries. The internship adds a different requirement: selecting document paragraphs through explicit, approved conditions. This demo connects those ideas by linking paragraphs to sources and checking the result.” It uses section-level educational summaries, not complete official legal texts. Act names help source identity, but production also needs jurisdiction, official-source and version information. The prototype demonstrates requirements from the brief, not their existing architecture.

## 3. Follow one case

About 45 seconds. “The fictional case requests the procedural route, has records and requests relief. The engine checks each prepared block’s conditions and prerequisites, then rejects any active configured conflicts. It selects jurisdiction, facts, procedural defense, records and relief, fills the supplied facts into templates, and returns a decision record.” Same facts and rule version yield the same output. M5 requires both has_records=True and selected M3. Other route flags default to False. The legacy limitation_defense name requests a sample procedural block; it does not calculate whether a legal deadline was breached. The source review later checks citation markers and manually recorded judgment dates, not legal applicability.

## 4. What the tests establish

About 40 seconds. “I use regression checks to detect unexpected changes. The suite repeats one case 25 times, compares four synthetic cases with written expectations, requests conflicting routes to test rejection, and adds a simulated source update to check the right warnings.” The suite also asserts missing-citation and retrieval paths. It is a role-focused demonstration, not the paper’s evaluation suite. Historical approval is not real despite the interface variable name. Judgment warnings depend on entered source notes and links; the program does not discover new judgments or determine their applicability.

## 5. Limits and first contribution

About 35 seconds. “This is a small prototype with summaries and fictional cases. It does not implement every capability in the brief: there is no generative review model, production database or structured appeals workflow. With the team, I would start from one approved example, clarify the conditions and exceptions, agree on expected outputs, and build a bounded pilot for review.” The TF-IDF retrieval threshold is uncalibrated and can reject ordinary questions. Missing-citation checks inspect markers, not semantic support. Do not promise production readiness or universal legal accuracy. Close by asking which workflow is the most useful first target.
