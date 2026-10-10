---
name: weekly-study-notes
description: >-
  Formats raw lecture notes, class notes, or study materials into structured weekly study notes.
  Use when the user asks for "study notes", "weekly notes", "class notes synthesis", or requests to
  format their raw notes. Do NOT use for general summarization, email drafting, or unrelated academic queries.
---

# Weekly Study Notes AI Skill

Transforms raw, messy lecture and class notes into high-yield, structured weekly study notes optimized for retention and active recall.

## Output Structure

Always structure the generated notes according to the following layout:

```markdown
# [Course / Subject]: [Weekly Topic Title]
*(Optional: Date / Lecture info if present in raw notes)*

## [Topic 1 Heading]
[Concise conceptual explanation synthesized from the notes]

### Key Terms
- **[Term 1]**: [Short 1-2 sentence definition or context].
- **[Term 2]**: [Short 1-2 sentence definition or context].

## [Topic 2 Heading]
...

## Active Recall & Review Questions
1. [Conceptual Question 1]
2. [Mechanism / Relationship Question 2]
3. [Application / Synthesis Question 3]
```

---

## Detailed Formatting Rules

### 1. Topic Headings
- Group related points into distinct `## Topic Heading` sections.
- When notes cover multiple days or disparate topics, organize them logically by theme rather than raw chronological fragments.

### 2. Key Terms List
- Under each major topic, include a dedicated key-terms list.
- Every key term must be **bolded**, followed by a colon and a concise definition/function.
- Highlight technical vocabulary, formulas, and laws mentioned in the notes.

### 3. Review Questions (Strict Constraint)
- Always end with `## Active Recall & Review Questions`.
- Provide **EXACTLY THREE (3)** high-yield conceptual questions to test retention.
- **Do not include answers** in the initial response; keep them blank so the student can practice retrieval. If the user asks for answers, provide them in a subsequent response.

---

## Edge Case Handling

1. **Messy / Incomplete Fragments**:
   - Synthesize fragments into coherent sentences without inventing facts or introducing external concepts not covered in the input.
2. **Mathematical Equations & Code**:
   - Preserve all formulas using proper LaTeX (`$E = mc^2$` or `$$...$$`).
   - Preserve all code snippets within appropriate fenced syntax blocks (e.g., ````python ... ````).
3. **No Fluff or Preamble**:
   - Begin immediately with the top-level Markdown title. Do not output conversational preambles like *"Here are your formatted study notes:"*.
