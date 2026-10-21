# Speaker notes

Suggested length: about five minutes. Treat this as an optional discussion aid.

## 1. Understanding the role

About 50 seconds. Docitalis publicly describes legal document translation for citizenship applications and an existing platform with human review. The internship brief extends into legal knowledge structuring and deterministic assembly. The brief supplies the Aprigliano connection; I am not asserting ownership or corporate affiliation. My aim is to understand the existing workflow before proposing changes. Source: https://docitalis.com/ and the supplied role description.

## 2. System boundaries

About 60 seconds. The deterministic engine uses case facts and an approved strategy. A module declares its required facts, prerequisites, conflicts, order and source links. A version and fingerprint identify the rule snapshot. The separate source matrix stores provenance, jurisdiction, dates and relationships between authorities and modules. Retrieval supplies review evidence and warnings, not a legal strategy. A lawyer assesses applicability. Relational tables are a reasonable starting point; a graph is a later choice only if relationship queries justify it. Sources: role description; https://docitalis.com/privacy-cookie-policy/ for document confidentiality context.

## 3. Daily work

About 60 seconds. I would join on-site discovery sessions, ask for a representative approved example and ask why each argument is included or excluded. I would record unknowns instead of guessing legal rules. Then I would translate one decision into explicit structured conditions, implement a narrow Python change and inspect the resulting trace with the domain expert. SQL can hold modules, conditions, prerequisites, citations and approvals. I would build proficiency in the team’s actual schema and formal methods. My current demos do not demonstrate SQL or Alloy implementation, so I would describe those as development areas rather than completed work.

## 4. Safe changes and appeals

About 65 seconds. Regression tests compare a changed knowledge base with approved reference cases. A changed answer may be a defect or an intended legal update; the difference must be explained and reviewed. Passing every agreed test is a software acceptance criterion, not a guarantee of universal legal accuracy. My demonstration uses synthetic cases and simulated judgments, not real lawyer-approved histories. A new judgment is not necessarily a statutory amendment or applicable to every case. For appeals I would structure findings, reasoning and authorities and link them to issues; legal professionals would decide viable grounds. Protect confidential documents and use authorized or de-identified examples for testing.

## 5. Evidence and first month

About 65 seconds. My earlier research contribution was literature review, problem identification and initial design. I later moved to an LLM inference project while a sub-team continued the legal work. These repositories are recent demonstrations, separate from the published implementation. UkilRAG demonstrates versioned modules, deterministic assembly and four passing synthetic regression groups; it is not a complete generative RAG system. LearnRAG has seven passing component tests and separately captured real MiniLM/Qwen outputs. It omits requested inline citations, and three chunks with top-k three do not establish retrieval quality at scale. I can explain those limitations. My first-month proposal is to map one workflow, agree on an authorized reference set, implement one bounded rule set and measure the result with reviewers. The team’s priorities determine the actual schedule. I would ask which workflow is the best first target.