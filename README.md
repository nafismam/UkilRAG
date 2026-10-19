# Legal Knowledge Assistant

A small Python project that turns case details into a draft legal document and checks the legal references used in it.

## What problem does it solve?

Preparing a legal document involves repeated work: writing the facts, choosing the right sections, putting arguments in order, and checking references. This project shows how some of that work can follow clear, repeatable rules.

## A simple example

Imagine a person wants to question an arrest and has custody records available.

1. The program reads those case details.
2. It selects prepared paragraphs about the facts, arrest procedure, supporting records, and requested relief.
3. It puts those paragraphs in a fixed order and explains why each was selected.
4. It checks the legal references and warns if a reference is missing or has a newer judgment recorded against it.

The result is a draft and a checklist for a person to review.

## What is included?

- Eight sample legal section summaries.
- Six reusable document blocks.
- A rule-based document builder with a record of its decisions.
- A local search tool that finds related legal sections.
- Checks for missing references and recorded legal updates.
- Four automated tests, all passing in the tested environment.

The examples are fictional. The section summaries are not complete official law. Judgment updates and historical case fixtures are simulated; no lawyer approval is claimed. The output needs professional review before any real use.

## How to run it

1. Open Google Colab.
2. Upload `Legal_Knowledge_RAG_Engine.ipynb`.
3. Select **Runtime → Run all**.
4. Read the sample draft, decision table, review warnings, and test results.

No API key, paid service, GPU, or model download is required. It uses Python, NumPy, and scikit-learn, which are available in a standard Colab runtime. All processing runs inside that runtime without calling an external AI service.

## Is this a RAG pipeline?

It implements the search and review parts of a RAG-style system, but it is **not a full RAG pipeline**.

RAG means retrieval-augmented generation: first retrieve relevant information, then give it to a language model to generate an answer. This project retrieves information, but it builds the legal draft using fixed rules and prepared paragraphs. There is no language model generating answers from the retrieved material.

A clear interview description is: “I built a rule-based legal document assistant with local legal search, citation checks, and a trace explaining its decisions.”

## What do the tests show?

| Check | Result |
| --- | --- |
| Same case run 20 times | Identical output every time |
| Four fictional reference cases | Expected paragraphs and references matched |
| Two conflicting document routes requested | A clear error was raised |
| A simulated legal update was added | Affected document blocks were flagged |

These results demonstrate software behavior on sample data. They do not measure legal accuracy or performance on real cases.

## What would come next?

Replace the sample summaries with verified complete legal sections, add genuine judgment records, and have lawyers review the document rules and test cases. Search quality also needs testing on realistic questions. A language model could later be added to explain retrieved sources, with clear citations and human review.

## Project provenance

This demonstration was generated with AI assistance in response to a user-defined specification. It is a separate educational prototype, not the implementation of a published research system. Its presence in this repository does not establish that the repository owner personally wrote or validated every component. Personal contributions should be described separately and accurately. Technical inspiration is acknowledged in the notebook’s source note.
