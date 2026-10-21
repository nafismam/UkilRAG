# Understanding the presentation in plain language

The whole idea: a lawyer supplies the approved instructions; software follows them, shows its work, and helps the lawyer notice what needs checking.

## Slide 1 — The goal

Imagine an experienced colleague who knows which paragraphs belong in each kind of document. Other people need to reuse that knowledge consistently. Your job is to help write down the instructions and turn them into software. You are not deciding what the law means.

Say: “I understand the role as making lawyer-approved reasoning easier to reuse and check.”

## Slide 2 — Three possible challenges

1. Someone knows a rule, but its exceptions are not written down clearly.
2. A person changes one rule and accidentally changes something else.
3. A new judgment means an old argument might need another look.

These are suggested by the job description. You have not inspected the company's internal process. Ask whether they are relevant rather than state they are existing failures.

## Slide 3 — Three matching actions

Write the instructions down with the expert. Keep some agreed examples and rerun them after changes. Keep a list of which sources support which paragraphs.

A rule might be: “Include paragraph B only if fact X is present and paragraph A is included.” This is a software illustration, not a legal rule. If the required facts are absent, the program should say why it left the paragraph out.

Say: “I would start with one approved example, record the conditions, and check the software's output with the lawyer.”

## Slide 4 — A change happens

A new judgment is added. Look up the paragraphs linked to it. Ask a lawyer whether it affects the relevant rule. If a change is approved, make a new version and check the agreed examples again. Review both intended and unexpected differences before release.

Regression testing is like changing an instruction in a recipe and checking that the dishes you still expect to work have not unexpectedly changed. An intended update may correctly change a result. The expert approves that new expectation; you do not blindly force the old result to pass.

Say: “A new judgment triggers review, not an automatic rewrite.”

## Slide 5 — Your contribution

Your earlier work covered literature review, problem identification and initial design. You later moved to an LLM inference project. The recent repositories are separate demonstrations; they are not the original published implementation.

Propose a small first task: understand one workflow, agree on examples, build a small pilot, and inspect its results with the team. Measure something useful, such as review effort or rework, before promising an improvement.

## Terms you should be able to explain

- **Module:** a reusable paragraph or document block.
- **Dependency:** something that must be present before another block can be used.
- **Exclusion:** two options configured not to appear together.
- **Deterministic:** the same facts, strategy and rule version produce the same output.
- **Version:** an identifiable edition of the rules; old outputs remain explainable.
- **Trace:** a record of why each block was included or skipped.
- **Legal sources matrix:** a structured catalogue of authorities and their links to rules or document blocks.
- **RAG:** retrieve relevant material, put it into a model prompt, and generate a response. Here it supports review; it does not choose legal strategy.
- **Regression test:** check that a software or knowledge change did not unexpectedly break agreed behavior.

## If asked about the demonstrations

UkilRAG: fixed rules select prepared paragraphs; the trace explains decisions; synthetic source changes trigger warnings. It does not generate answers with an LLM, and its cases are not genuinely lawyer-approved historical files.

LearnRAG: small text windows become vectors, the question retrieves close passages, and Qwen generates an answer using those passages. The real run abstained on one unsupported question but omitted requested inline citations. With three chunks and top-k three, every question gets the whole tiny collection; this is not a retrieval-quality benchmark.

Describe implementation assistance and your personal work accurately when asked. Knowing the limits is more credible than claiming perfect results.

## Possible coding discussion

The role explicitly involves Python, backend work and tests. A short coding exercise or code walkthrough is possible, but nothing supplied confirms the format. A laptop conversation alone does not establish a live-coding assessment.

Prepare to do the following without relying on generated code:

- Read a JSON case and validate its required fields and types.
- Filter a list of document blocks using Boolean conditions.
- Check that prerequisites are present and reject conflicting choices.
- Sort blocks consistently and explain the order.
- Write a small pytest assertion against an expected result.
- Explain a simple SQL relationship between modules, sources and case outputs.
- Explain what a Git diff shows and how a change could be reverted.

Understand the code in your repositories first. Then practise small variations: a missing fact, an absent prerequisite, a conflicting flag, a citation missing from text and a changed expected output.

To clarify interview logistics, ask: “Should I prepare for a live Python exercise, a walkthrough of my projects, or both?”
