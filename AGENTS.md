# Resume Repository

Maintain authentic, ATS-readable, single-page A4 LaTeX resumes.

## Branches

- `master`: Complete factual CV and shared instructions.
- `role/*`: Authentic, reusable role-specific resumes.
- `application/*`: Aggressively ATS-tailored resumes for individual jobs.

Application branches originate from the relevant role branch. If none exists, create the role branch from `master` first, with user approval.

## Files

- `master_cv.tex`: Factual source of truth; never modify during tailoring.
- `abbas_taqvi_resume.tex`: Tailored resume and editing target.
- `job_description.md`: Job description on application branches.

For applications, prioritize the role resume, using the master CV for additional verified evidence.

## Rules

- Never fabricate skills, experience, metrics, qualifications, or achievements.
- User-confirmed skills are valid even when absent from the master CV.
- Preserve factual meaning while freely improving wording, relevance, and ordering.
- Role resumes prioritize authenticity; application resumes prioritize ATS matching without misrepresentation.
- Preserve the existing LaTeX design and readable formatting.
- Every final resume must compile to **exactly one A4 page**, with readable PDF text extraction.
- Do not commit, push, submit, or modify Git branches/worktrees without permission.

## Skills

- `tailor-role`: Create an authentic role resume.
- `tailor-application`: Match a JD, batch-check missing skills, and tailor for ATS.
- `review-resume`: Compile, verify, and enforce one-page PDF output.

Use `review-resume` after every tailoring operation. Report validation failures rather than claiming success.
