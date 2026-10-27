# Speaking guide

Five slides, about 3–4 minutes. Ask whether a short walkthrough would be useful before presenting.

## 1. My understanding of the role

About 35–40 seconds. “I understand this internship as turning lawyers’ knowledge into explicit software rules. I would start by learning the workflow, recording the conditions and exceptions, then helping build and test the approved process. Rules control document assembly; AI supports review, while legal decisions remain with lawyers.” The brief names Docitalis and services connected with Aprigliano. This slide does not claim to describe their existing architecture. Public context: https://docitalis.com/.

## 2. My previous experience

About 40–45 seconds. “In the earlier research, my contribution was literature review, problem identification and initial design. A practical concern was confusing Bangladeshi and Indian legal provisions. I helped explore section-level organisation and retaining parent Act metadata so evidence could be traced to its source. We also considered passages related to a question but insufficient to answer it fully. I then moved to LLM inference work while a sub-team continued the legal project.” Distinguish personally completed work from group work. Do not imply ownership of the complete published pipeline. Act names alone are not sufficient jurisdiction metadata; full official sources and versions also matter.

## 3. The project implementation

About 45 seconds. “I prepared this recent demonstration to explore requirements from the role. The fictional case requests the procedural route and has records. The engine validates input, checks conditions and prerequisites, rejects conflicting selections, fills prepared paragraphs and returns a decision record.” For this case it selects jurisdiction, facts, procedural defense, records and relief. M5 needs both records and selected M3. Same inputs and rule version give the same output. The prototype is not the original research system. Describe implementation assistance and your own review/testing accurately when explaining who built each part. The legacy limitation_defense flag requests a procedural example; it does not establish a legal deadline violation.

## 4. What is checked

About 45 seconds. “The review checks required citation markers and manually recorded judgment notes. A newer note flags selected modules linked to that source. It does not discover judgments online or assess legal applicability.” The four test groups check 25-run reproducibility, expected module order and citations on four fictional cases, rejection of configured conflicting routes, and warnings after an injected simulated judgment. Citation and retrieval assertions also run. All groups passed. This checks agreed software behaviour, not universal legal correctness. The source search uses TF-IDF with an uncalibrated 0.80 gate; exact-text examples demonstrate the mechanism, not paraphrase accuracy. There is no generative review model in this notebook.

## 5. A first contribution

About 30–40 seconds. “With the team, I would start from one approved workflow, clarify its rules and exceptions, agree on examples, then build a small pilot and inspect the results with reviewers. I would learn the existing system before choosing new tools.” The demo uses summaries and fictional cases, not real lawyer-approved histories. It is not a production backend, SQL database or implemented appeals workflow. For a broader RAG discussion, LearnRAG is a separate demo with actual MiniLM/Qwen outputs and documented limits. Close with the question on the slide and listen. Ask about supervision, code review and legal approval if these have not been discussed. No percentage improvement is promised without a baseline.
