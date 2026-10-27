# Slide-by-slide speaking guide

Eight slides. Full walkthrough: about 6–7 minutes. For a shorter introduction, offer to skip detail slides and discuss them only if useful.

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

## 7. Design challenges and limits

About 45 seconds. Present this as design reasoning rather than invented project history. “The demo makes three concerns visible. A compound query can fail the gate, so the controlled example tries explicit decomposition. Conflicting module choices must not silently coexist, so assembly raises an error. Citation metadata may claim a source is required even when the text omits it, so the review checks actual markers.” These are chosen failure modes and scripted checks, not evidence of a real customer incident or measured business improvement. The search is not validated on natural legal queries, legal exclusions require domain approval, and marker checks do not assess semantic support. Do not claim an optimal threshold or a fully solved legal retrieval problem.

## 8. Real-use reliability

About 40 seconds. “The demo uses summaries, fictional cases and simple checks. With your team, I would start from one approved workflow and reviewed reference set, implement a bounded task, then inspect results with lawyers and engineers.” Production work needs jurisdiction/version/source metadata, approved test cases, access controls and technical review. Evaluate thresholds on labeled queries rather than assume 0.80 transfers to another corpus. Assess claim-to-source support rather than just marker presence. The prototype lacks production storage, a generative legal reviewer and an appeals workflow. Keep these as development scope, not completed features. Close with the slide’s question. Ask about technical supervision and legal approval if not covered.
