---
name: tailor-application
description: Aggressively tailor a LaTeX resume to job_description.md for ATS relevance while preserving factual accuracy. Use on application/* branches.
---

# Tailor Application Resume

## Inputs

- `job_description.md` — target vacancy
- `abbas_taqvi_resume.tex` — primary reference and output
- `master_cv.tex` — secondary factual reference

## Phase 1: Analyze and ask once

Read all three files.

Extract the JD's required and preferred skills, technologies, qualifications, and responsibilities.

In a single pass, identify relevant skills not documented in either resume source.

Present one numbered list, ordered by JD importance:

1. dbt
2. Snowflake
3. Terraform

Ask: **"Which of these have you used? Reply with numbers (e.g. 1,3), or 'none'."**

Stop and wait.

Treat selected skills as user-confirmed. Never include unselected skills as possessed qualifications. Ask for details only if necessary to make a specific experience claim.

Do not repeat the questionnaire during the same tailoring task.

## Phase 2: Tailor aggressively

After confirmation:

1. Match JD terminology wherever genuinely applicable.
2. Prioritize the most relevant experience, projects, technologies, and accomplishments.
3. Reorder bullets and sections for maximum job relevance.
4. Incorporate confirmed skills naturally.
5. Use `master_cv.tex` to recover relevant factual details absent from the role resume.
6. Rewrite bullets to communicate impact, ownership, and technical contributions accurately.
7. Remove low-value content to maintain one-page length.
8. Preserve the existing LaTeX template.

Optimize strongly for ATS matching, but never invent experience, metrics, proficiency, job titles, or qualifications.

Related technologies do not establish experience with the exact JD technology.

## Phase 3: Validate

Run `review-resume`, passing the job description as relevance context.

Do not declare completion until the resulting PDF passes its checks.

## Output

- Updated `abbas_taqvi_resume.tex`
- Validated one-page PDF
- Concise summary of important JD matches
- Remaining genuine skill gaps

Never modify `master_cv.tex`, create commits, or submit applications automatically.
