# Speaking guide

Five slides, about 4 minutes. Flow: role → experience → sources/rules → assembly → review/tests.

## 1. My understanding of the role

About 35–40 seconds. “I understand this internship as turning lawyers’ knowledge into explicit software rules. I would start by learning the workflow, recording the conditions and exceptions, then helping build and test the approved process. Rules control document assembly; AI supports review, while legal decisions remain with lawyers.” The brief names Docitalis and services connected with Aprigliano. This slide does not claim to describe their existing architecture. Public context: https://docitalis.com/.

## 2. My previous experience

About 40–45 seconds. “In the earlier research, my contribution was literature review, problem identification and initial design. A practical concern was confusing Bangladeshi and Indian legal provisions. I helped explore section-level organisation and retaining parent Act metadata so evidence could be traced to its source. We also considered passages related to a question but insufficient to answer it fully. I then moved to LLM inference work while a sub-team continued the legal project.” Distinguish personally completed work from group work. Do not imply ownership of the complete published pipeline. Act names alone are not sufficient jurisdiction metadata; full official sources and versions also matter.

## 3. Cells 1 and 2: sources and paragraph rules

About 45 seconds. “Cell 1 stores labelled source records: Act, section, text and any recorded judgment note. Cell 2 stores prepared paragraphs and the conditions for including them. The shared source ID connects the two.” For example, the records paragraph M5 requires available records AND selected procedural block M3; it links to C167. The output of these cells is a source table and a module-rule table, not an assembled document. There are ten educational source summaries and seven blocks in knowledge base 1.2.0. The date and version are manually assigned. Two simulated source updates exist for testing. The terms and exclusive routes are teaching examples, not verified legal instructions.

## 4. Cell 3: the assembly engine

About 50 seconds. “This is the main drafting step. The engine checks the case facts, evaluates paragraph conditions, checks prerequisites and rejects active configured conflicts. It fills the selected templates and returns both the draft and an explanation.” The sample output is M1 jurisdiction, M2 facts, M3 procedure, M5 records and M7 relief. M4 substantive and M6 bail are skipped because their flags default to False. M5 is included because has_records=True and M3 was included. The trace records expected/actual facts, missing prerequisites, decisions, version and fingerprints. The method returns the final document text, module IDs, required sources and trace. No LLM chooses paragraphs. The legacy limitation_defense flag is a supplied request for this procedural example, not an automated conclusion about a legal deadline.

## 5. Cells 4 and 5: review and regression tests

About 60 seconds. “Cell 4 retrieves source summaries and performs structured checks on the draft. The controlled two-part search finds C54 and P420 after decomposition. In the sample draft, newer recorded notes flag M3-C54, M3-C167 and M5-C167: three module-source links. There are no missing-citation warnings in this unmodified draft. Searching the ordinary case summary accepts no source at the 0.80 gate; both split parts remain unresolved.” The threshold is uncalibrated, TF-IDF is word-based, decomposition uses separators, and no generative reviewer runs. Judgment warnings compare manually entered dates; they do not assess applicability. “Cell 5 checks 25-run reproducibility, four synthetic reference cases, rejection of conflicting routes and warning propagation after a simulated source update. All four groups pass; additional assertions exercise citation and retrieval paths.” Expected examples are synthetic, not actual lawyer-approved files. Close: “With the team I would start from one approved workflow and agreed examples. Which would be the most useful starting point?”
