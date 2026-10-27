# Slide-by-slide speaking guide

Eight slides. Offer a short walkthrough, then adjust depth to the interviewer’s interest.

## 1. Role understanding

About 35 seconds. “I understand the role as learning how lawyers make decisions and representing approved reasoning as explicit rules. The system then prepares a consistent draft and explains its choices. AI can support review, but legal strategy and applicability remain with lawyers.” This is based on the supplied posting, not access to the internal system. Public context: https://docitalis.com/.

## 2. Previous experience

About 40 seconds. “My role covered literature review, problem identification and initial design. I helped explore section-level organisation and parent Act metadata so retrieved passages could be traced to their sources. I later moved to an LLM inference project while a sub-team continued the legal work.” Do not claim implementation of the final research pipeline. A lawyer discussion motivated the Bangladesh/India confusion concern. Act names alone cannot settle jurisdiction; verified source, jurisdiction and version metadata are needed. The recent demo is a separate implementation; explain assistance and personal work accurately when discussing ownership.

## 3. Source records and paragraph rules

About 50 seconds. Cell 1 creates a catalogue with source IDs, Act names, section numbers, prepared summaries, status and judgment notes. Cell 2 creates reusable paragraph definitions: conditions, prerequisites, configured exclusions, order, source links and prepared text. The shared ID C167 connects source and paragraph. M5 needs records AND selected M3, has order 50, and cites C167. Ten records and seven modules are definitions, not a draft. Version 1.2.0 and its snapshot date are manually assigned. Summaries and judgment notes are illustrative, not verified full official law. Legal time limits are not calculated by the legacy limitation_defense flag.

## 4. Assembly and actual decisions

About 55 seconds. These are the sample facts and actual decisions. Missing optional flags default to False. Every block must satisfy its own required facts AND have every prerequisite included. Conditions select M1, M2, M3, M5 and M7; M4 and M6 are skipped. Both configured exclusive routes would raise an error before text is returned. The selected prepared templates are filled with the name, case ID and summary, then joined in order. The trace records both inclusion and skipping with expected/actual facts, prerequisites, source IDs and version fingerprints. Same facts and rule snapshot produce the same result. It is not LLM drafting or automated legal fact verification.

## 5. Retrieval, decomposition and review

About 60 seconds. The two-part exact-source query first has a best score of 0.787877, below the uncalibrated 0.80 threshold, so nothing is accepted. The method splits on the semicolon, searches each exact source text, and accepts C54 and P420 at approximately 1.0. It interleaves ranked groups and removes duplicate IDs. No model performs this split: it uses explicit text separators. Ordinary case-summary retrieval and both split parts accept no sources, and are returned as unresolved. Retrieval does not determine strategy. Separately, review derives required citations from module definitions and reads markers from actual text. The sample has no missing markers but newer recorded notes produce three module-source warnings. Notes are manually entered and simulated; the program does not discover judgments or determine legal applicability. TF-IDF matching is word-based and the threshold is not an accuracy percentage.

## 6. Regression inputs and expectations

About 50 seconds. Reproducibility compares document and full-output fingerprints across 25 runs. Reference parity compares four synthetic cases against independently written module sequences, citation lists and actual text markers. The conflict test expects an exception when both teaching routes are requested, and checks consistent messages. The update test begins with no notes, adds a simulated C167 note and expects M3 and M5 warnings. Additional checks remove C54, add unknown C999 and exercise retrieval paths. All four groups pass. These checks were specified for this role-focused demonstration, not taken as an evaluation suite from the research paper. Twenty-five is a demonstration count, not a statistical guarantee. Synthetic fixtures are not genuinely lawyer-approved historical cases. Passing checks software expectations, not legal correctness.

## 7. Design choices and trade-offs

About 60 seconds. This slide replaces a challenge story with the actual implementation choices. First, 0.80 was adopted from the reference approach to demonstrate gating, not derived from experiments on this TF-IDF index. It is not 80% confidence, correctness or coverage. Calibrate thresholds with reviewed legal questions and expected sources. Second, lists and dictionaries serve different roles: a list holds multiple records, while each dictionary names fields; source["act_name"] is clearer than remembering positional indexes. The by_id dictionary also supports lookup by source ID and rejects duplicates. Third, sorted JSON plus SHA-256 produces compact fingerprints for comparing knowledge-base content and outputs. Direct equality comparisons are another option. Hashes do not themselves create determinism, establish semantic correctness, or make this an approval/signature system. Fourth, scikit-learn supplies TF-IDF and cosine similarity for a small local retrieval baseline. It needs no embedding-model download or API key. It may miss paraphrases and its score is lexical similarity, not applicability. A dense embedding model or hybrid retrieval could be evaluated later. An LLM is a separate generator/reviewer, not a direct alternative to the TF-IDF retrieval component. The current notebook uses rule-based checks rather than an LLM review layer.

## 8. Real-use reliability

About 40 seconds. “The demo uses summaries, fictional cases and simple checks. With your team, I would start from one approved workflow and reviewed reference set, implement a bounded task, then inspect results with lawyers and engineers.” Production work needs jurisdiction/version/source metadata, approved test cases, access controls and technical review. Evaluate thresholds on labeled queries rather than assume 0.80 transfers to another corpus. Assess claim-to-source support rather than just marker presence. The prototype lacks production storage, a generative legal reviewer and an appeals workflow. Keep these as development scope, not completed features. Close with the slide’s question. Ask about technical supervision and legal approval if not covered.
