---
name: tailor-role
description: Create or update an authentic, reusable one-page LaTeX resume for a job family using master_cv.tex. Use on role/* branches.
---

# Tailor Role Resume

## Inputs

- `master_cv.tex` — factual source
- `abbas_taqvi_resume.tex` — output and existing template, if present
- Current `role/*` branch — target job family

## Procedure

1. Identify the target role from the branch name.
2. Read the master CV and identify the most relevant professional experience, projects, education, and technical skills.
3. Create or update `abbas_taqvi_resume.tex` using the existing LaTeX style.
4. Prioritize authentic accomplishments, technical depth, and a coherent professional narrative.
5. Use natural, recruiter-friendly wording. Avoid keyword stuffing, generic AI-sounding phrases, and exaggerated claims.
6. Prefer concrete technical contributions over vague responsibilities.
7. Preserve verified facts and metrics. Never invent missing information.
8. Select content to fit one A4 page without sacrificing readability.
9. Run the `review-resume` skill to compile, inspect, and enforce the one-page requirement.

## Rules

- Do not require a job description.
- Do not modify `master_cv.tex`.
- Do not exaggerate professional experience or proficiency.
- Do not sacrifice authenticity for ATS keyword coverage.
- Ask only when essential factual information is missing.

## Output

- Updated `abbas_taqvi_resume.tex`
- Validated one-page PDF
- Brief summary of selected and omitted content
