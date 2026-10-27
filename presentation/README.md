# Final interview presentation

One five-slide deck combining role understanding, previous experience and a cell-by-cell UkilRAG walkthrough. Related cells share a slide; assembly has a slide of its own. Each implementation slide shows an idea and a small output, not code. Suggested length: about 4 minutes.

- [Download PowerPoint](Nafis_Ismam_Docitalis_Final.pptx?raw=true)
- [View PDF](Nafis_Ismam_Docitalis_Final.pdf)
- [Read the speaking guide](speaker_notes.md)

For Google Slides, download the PPTX, upload it to Drive, and open with Google Slides. Check the layout after importing.

## Flow

1. **My understanding of the role:** learn from lawyers, record approved rules and check changes.
2. **My previous experience:** literature review, problem identification and initial design.
3. **Cells 1 + 2 — sources and paragraph rules:** example source C167, and the rule linking it to the records paragraph.
4. **Cell 3 — deterministic assembly:** sample facts produce jurisdiction, facts, procedure, records and relief, with an inclusion explanation.
5. **Cells 4 + 5 — review and tests:** actual search/review observations, 25 matching runs, four reference cases, conflict rejection and source-update checks.

## Slide previews

![Overview](previews/overview.png)

### 1. My understanding of the role
![Slide 1](previews/slide-1.png)

### 2. My previous experience
![Slide 2](previews/slide-2.png)

### 3. Cells 1 + 2: sources and paragraph rules
![Slide 3](previews/slide-3.png)

### 4. Cell 3: assembly and decision record
![Slide 4](previews/slide-4.png)

### 5. Cells 4 + 5: review and test outputs
![Slide 5](previews/slide-5.png)

## Sources and scope

- The original internship posting supplied by the candidate describes work with lawyers, explicit rules, versioned assembly, historical-case regression testing, assistive RAG review and an appeals extension. The deck explains that brief, not Docitalis's existing internal software.
- [Docitalis](https://docitalis.com/) provides the public company context. The supplied posting states the connection with services for Aprigliano International Law Firm; the deck does not infer corporate ownership.
- Earlier research responsibilities are based on the candidate's account. They are separate from this recent demonstration and from implementation of the full published research pipeline.
- [The executed notebook](../Legal_Knowledge_and_RAG_Prototype.ipynb) provides the demonstration and test evidence. It uses sample summaries and fictional cases/judgments, not complete verified official text or genuinely lawyer-approved historical cases. Passing tests does not establish legal accuracy. Its review checks markers and recorded dates; it does not assess legal applicability or run a generative review model. Technical inspiration is credited in the notebook.

The previous two decks have been removed from the current repository version. They remain recoverable through normal Git history.
