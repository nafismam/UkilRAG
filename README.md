# Legal Knowledge and RAG Prototype

## Overview

This compact Python notebook connects section-wise legal retrieval with rule-based document assembly. It follows the owner’s reported statutory RAG design work at North South University; this is a separate demonstration.

Fictional case details select prepared paragraphs with explicit explanations. Separate retrieval and review flag relevant sections, missing citations and simulated judgment updates.

## Architecture

- **Deterministic assembly and traceability:** seven blocks follow explicit conditions, prerequisites and ordering, with versioned rules and output hashes.
- **Section-wise retrieval and source review:** ten section summaries retain Act metadata. TF-IDF search uses a threshold and simple issue splitting. No language model generates answers, so this is not complete generative RAG.
- **Regression testing:** four synthetic reference cases check expected blocks and citations; further tests check 25-run reproducibility, conflicts and update warnings. They are not lawyer-approved historical records.

## Run

View saved outputs in [the notebook](Legal_Knowledge_and_RAG_Prototype.ipynb), or [open Colab](https://colab.research.google.com/github/nafismam/UkilRAG/blob/main/Legal_Knowledge_and_RAG_Prototype.ipynb) and run all cells. Locally, use an existing Jupyter installation with `pip install -r requirements.txt`.

No keys or GPU are required. Legal summaries, judgments and cases need replacement with verified material before real use. The illustrative 0.80 threshold is uncalibrated.
