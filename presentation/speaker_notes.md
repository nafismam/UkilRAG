# Slide-by-slide speaking guide

Seven slides; aim for about 5–6 minutes. Offer the walkthrough and adjust depth to the interviewer’s interest.

## 1. My understanding of the role

About 35 seconds. “I understand the role as learning how lawyers make decisions and representing approved reasoning as explicit rules. The system then prepares a consistent draft and explains its choices. AI can support review, but legal strategy and applicability remain with lawyers.” This is based on the supplied posting, not access to the internal system. Public context: https://docitalis.com/.

## 2. Earlier research contribution

About 40 seconds. “My role covered literature review, problem identification and initial design. I helped explore section-level organisation and parent Act metadata so retrieved passages could be traced to their sources. I later moved to an LLM inference project while a sub-team continued the legal work.” Do not claim implementation of the final research pipeline. A lawyer discussion motivated the Bangladesh/India confusion concern. Act names alone cannot settle jurisdiction; verified source, jurisdiction and version metadata are needed. The recent demo is a separate implementation; explain assistance and personal work accurately when discussing ownership.

## 3. Cells 1 and 2: ingredients and instructions

About 45 seconds. “Cell 1 creates the Legal Sources Matrix. Cell 2 defines seven prepared document blocks and their rules in version 1.2.0. The source ID connects each paragraph to the legal records it references.” Example: M5 requires records and selected M3, and links to C167. Show these are definitions, not a completed draft. The source texts are summaries rather than verified full provisions. Two judgment notes are simulated. Versions and dates are manually assigned. The legacy limitation_defense flag is a supplied request for the procedural example, not a calculation of a breached legal deadline. Exclusive routes are teaching configuration, not universal legal rules.

## 4. Cell 3: deterministic assembly

About 45 seconds. “The sample requests the procedural route, has records and requests relief. The engine validates fields, checks conditions and prerequisites, records every inclusion or skip, checks active conflicts and fills selected templates in order.” The sample selects M1, M2, M3, M5 and M7. M4 and M6 are skipped because their flags default to False. Defaulting unknown facts to False would need careful agreement in a real workflow. The returned trace includes rules, missing dependencies, source links, version and fingerprints. Hashes help compare outputs; they do not make them legally correct. No LLM invents the wording.

## 5. Cell 4: retrieval and review

About 50 seconds. “Retrieval uses TF-IDF word matching and cosine similarity with an uncalibrated 0.80 gate. If direct retrieval accepts nothing, explicit separators can split the query. The controlled two-source text example retrieves C54 and P420 after splitting.” That is not proof of paraphrase accuracy. “Separately, the review derives required citations from module definitions, checks markers in the actual text and compares stored judgment-note dates.” The unchanged draft has three newer-note warnings: M3-C54, M3-C167 and M5-C167. It has no missing-citation alerts. The ordinary case summary and both split parts accept no sources. Explicit source-link warnings do not depend on search success. No new judgments are discovered automatically, no generative reviewer runs, and marker presence does not establish semantic citation support.

## 6. Cell 5: regression tests

About 45 seconds. “These checks target the prototype’s promises: repeatable outputs, expected module order and citations, conflict rejection and recorded update alerts. All four groups pass.” Twenty-five repetitions were specified for the demo and are not a mathematically special number. Expected fixture lists are written separately. The conflict test passes when the intended error is raised. The update test removes notes, inserts a new simulated C167 note and checks M3 and M5; it also deliberately damages citations and checks retrieval paths. These are not approved real historical cases. A reviewed legal change may intentionally change expected outputs, so failures require investigation rather than blindly forcing old results.

## 7. Keeping a real system reliable

About 40 seconds. “The demo uses summaries, fictional cases and simple checks. With your team, I would start from one approved workflow and reviewed reference set, implement a bounded task, then inspect results with lawyers and engineers.” Production work needs jurisdiction/version/source metadata, approved test cases, access controls and technical review. Evaluate thresholds on labeled queries rather than assume 0.80 transfers to another corpus. Assess claim-to-source support rather than just marker presence. The prototype lacks production storage, a generative legal reviewer and an appeals workflow. Keep these as development scope, not completed features. Close with the slide’s question. Ask about technical supervision and legal approval if not covered.
