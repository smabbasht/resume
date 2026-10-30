---
name: tailor-role
description: Create or update an authentic, reusable one-page LaTeX resume for a job family using master_cv.tex. Use on role/* branches.
---

# Tailor Role Resume

## Inputs

- `master_cv.tex` — factual source
- `abbas_taqvi_resume.tex` — output and existing template
- Current `role/*` branch — target job family

## Procedure

1. Identify the target role from the branch name.
2. Read the `abbas_taqvi_resume.tex` and `master_cv.tex` and identify the most relevant professional experience, projects, education, and technical skills.
3. Update `abbas_taqvi_resume.tex` using the existing LaTeX style.
4. Never restructure, add/remove or reorder the LaTeX resume sections, Keep it as it is.
5. Prioritize authentic accomplishments, technical depth, and a coherent professional narrative.
6. Use natural, recruiter-friendly wording. Avoid keyword stuffing, generic AI-sounding phrases, and exaggerated claims.
7. Prefer concrete technical contributions over vague responsibilities.
8. Preserve verified facts and metrics. Never invent missing information.
9. Select content to fit one A4 page without sacrificing readability.
10. Run the `review-resume` skill to compile, inspect, and enforce the one-page requirement.

## Rules

- Never remove Logiciel Services LLC and ImproData roles.
- Do not exaggerate professional experience or proficiency.
- Do not sacrifice authenticity for ATS keyword coverage.
- Ask only when essential factual information is missing.
- Do not modify `master_cv.tex`.

## Output

- Updated `abbas_taqvi_resume.tex`
- Validated one-page PDF
- Brief summary of selected and omitted content
