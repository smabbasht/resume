---
name: review-resume
description: Compile, audit, and enforce an exactly one-page A4 LaTeX resume. Check ATS text extraction, readability, and factual accuracy. Use after resume tailoring or when reviewing a resume.
---

# Review Resume

## Inputs

- `abbas_taqvi_resume.tex`
- `master_cv.tex` for factual verification
- `job_description.md` when available for relevance ranking

## Procedure

### 1. Compile

Compile the resume using `pdflatex` with nonstop interaction and halt-on-error enabled.

Use an isolated build directory. Run additional passes if references require them.

If compilation fails, fix the LaTeX error and retry.

### 2. Verify PDF

Use `pdfinfo` to verify:

- Exactly 1 page
- A4 dimensions, approximately 595 × 842 points

Use `pdftotext -layout` to inspect extracted content.

Check for missing text, broken Unicode, unusual reading order, duplicated content, and extraction failures.

Inspect the rendered page for clipping, overlaps, excessive whitespace, and readability when rendering tools are available.

### 3. Enforce one page

If the PDF exceeds one page, edit `abbas_taqvi_resume.tex` using this priority:

1. Remove redundant or irrelevant bullets.
2. Shorten verbose descriptions.
3. Remove less relevant projects or coursework.
4. Consolidate skills and repetitive information.
5. Make modest spacing adjustments.

Use `job_description.md` to decide what to retain when available.

Preserve strong, relevant achievements.

Do not use tiny fonts, extreme margins, or unreadable compression.

Recompile and verify after each revision.

Limit automatic revision to five iterations. If a readable one-page resume remains impossible, report the trade-off and request guidance.

### 4. Factual audit

Compare factual claims with `master_cv.tex` and any user-confirmed information available in the session.

Flag unsupported skills, inflated responsibilities, invented metrics, or misleading statements.

Do not remove a user-confirmed skill solely because it is absent from the master CV.

### 5. ATS audit

Check:

- Standard, recognizable section headings
- Relevant keywords used accurately
- Readable and extractable text
- Clear experience chronology
- No hidden keywords or keyword stuffing
- No misleading qualifications

Do not invent numerical ATS compatibility scores.

## Completion

Report:

- Compilation: PASS/FAIL
- Pages: actual count
- Paper size: A4 PASS/FAIL
- Text extraction: PASS/FAIL
- Factual audit: PASS/FAIL or needs confirmation
- Final PDF path
- Any unresolved issues

Never claim success without verifying the generated PDF.
