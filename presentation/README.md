# Final interview presentation

Seven plain-language slides. Each implementation slide explains what goes in, what the cell does and what comes out. No code screenshots. Suggested length: about 5–6 minutes; adjust depth to the interviewer’s interest.

- [Download PowerPoint](Nafis_Ismam_Docitalis_Final.pptx?raw=true)
- [View PDF](Nafis_Ismam_Docitalis_Final.pdf)
- [Read the slide-by-slide speaking guide](speaker_notes.md)

For Google Slides, download the PPTX, upload it to Drive and open with Google Slides. Check layout after importing.

## Flow

1. **My understanding of the role:** learn lawyers’ reasoning, record approved rules and check results.
2. **Previous experience:** literature review, problem identification and early design for Bangladeshi legal question answering.
3. **Cells 1 + 2:** prepare source records, paragraph templates and rules; link them through source IDs.
4. **Cell 3:** validate facts, check conditions and conflicts, assemble prepared text and return a decision trace.
5. **Cell 4:** retrieve source summaries; check citation markers and recorded judgment dates. Show the actual sample warnings and unresolved search.
6. **Cell 5:** explain the four regression groups and their passing results on synthetic examples.
7. **Keeping it reliable:** use approved sources/examples, review and version changes, then evaluate retrieval and citation support before expanding.

## Slide previews

![Overview](previews/overview.png)

### 1. My understanding of the role

![Slide 1](previews/slide-1.png)

### 2. Previous experience

![Slide 2](previews/slide-2.png)

### 3. Cells 1 + 2: sources and paragraph rules

![Slide 3](previews/slide-3.png)

### 4. Cell 3: assembly and decision trace

![Slide 4](previews/slide-4.png)

### 5. Cell 4: retrieval and review output

![Slide 5](previews/slide-5.png)

### 6. Cell 5: regression tests

![Slide 6](previews/slide-6.png)

### 7. Keeping it reliable in real use

![Slide 7](previews/slide-7.png)

## Sources and scope

- The original internship posting supplied by the candidate describes work with lawyers, explicit rules, versioned assembly, historical-case regression testing, assistive RAG review and an appeals extension. The deck explains that brief, not Docitalis's existing internal software.
- [Docitalis](https://docitalis.com/) provides the public company context. The supplied posting states the connection with services for Aprigliano International Law Firm; the deck does not infer corporate ownership.
- Earlier research responsibilities are based on the candidate's account. They are separate from this recent demonstration and from implementation of the full published research pipeline.
- [The executed notebook](../Legal_Knowledge_and_RAG_Prototype.ipynb) provides the demonstration and test evidence. It uses sample summaries and fictional cases/judgments, not complete verified official text or genuinely lawyer-approved historical cases. Passing tests does not establish legal accuracy. Its review checks markers and recorded dates; it does not assess legal applicability or run a generative review model. Technical inspiration is credited in the notebook.

The previous two decks have been removed from the current repository version. They remain recoverable through normal Git history.
