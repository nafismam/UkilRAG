# Speaker notes

Five slides; aim for 4–5 minutes. Offer the presentation as an optional discussion aid.

## 1. The goal

Opening, 35–45 seconds: “I understand this role as helping turn lawyer-approved expertise into repeatable software. I would first learn how your team works, rather than assume your process needs replacing.” Docitalis publicly describes document translation for Italian citizenship and human review. The role brief places this internship with Aprigliano legal teams and includes pleading assembly. I am distinguishing that brief from the public translation business. The legal team decides strategy; the software applies approved rules. Sources: https://docitalis.com/ and the supplied role description.

## 2. Challenges, not accusations

About 50 seconds: “These are challenges I infer from the job description, not problems I have observed inside your company.” First, an experienced lawyer may know when an argument applies but the exceptions may not yet be written as software rules. Second, changing a rule can unintentionally change other documents. Third, a new authority may warrant review of existing arguments. Ask which of these consumes most team time. Do not say their current drafts contain errors or their system lacks tests. Avoid quantifying costs or promising a reduction without a baseline.

## 3. Three corresponding actions

About 60 seconds. “For unwritten knowledge, I would work through an approved example with a lawyer and record the conditions and exceptions. For consistency, I would compare changed software against examples with agreed expected results. For source review, I would keep links between authorities and the paragraphs that rely on them.” In engineering terms these are modular rules, regression tests, and a maintained legal sources matrix. Retrieval can assist source discovery, and AI can suggest concerns, but legal applicability and strategy remain with lawyers. A source change triggers investigation, not automatic replacement of every document. Human review remains essential.

## 4. One worked example

About 60 seconds: “Suppose a new judgment is recorded. The first task is not to let AI rewrite the pleadings. It is to find the paragraphs linked to the relevant authority and ask a lawyer whether the judgment applies. If the lawyer approves a rule change, I would record a new version, rerun agreed examples and explain the differences.” It may be an interpretation rather than a statutory amendment. Regression means checking that a change did not break behavior we still expect. An intended legal update can legitimately change an expected result after review. Passing all agreed examples is not 100% legal accuracy. For the appeals extension, similar structured source links can help organise findings, reasoning and possible issues for lawyer assessment; they do not decide appeal grounds.

## 5. Evidence and a first step

About 55 seconds. “My earlier research contribution was literature review, problem identification and initial design. I later moved to an LLM inference project while a sub-team continued the legal work. These recent demos are separate exercises.” UkilRAG demonstrates explicit document rules, a decision trace and regression checks on synthetic cases. LearnRAG has saved actual model outputs and separate component tests, with limitations recorded. Do not claim that either repository proves historical implementation ownership or production readiness. Proposed starting point: understand one workflow, agree on authorized examples and expected outputs, build one small pilot and measure reviewer effort and rework. Ask: “Which workflow would be the most useful starting point for this internship?”