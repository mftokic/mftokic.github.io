---
name: writing-publish-prep
description: 'Prepare approved Quarto posts for official site release and social distribution. Use when a post needs publication-date and path checks, a full Quarto render, final browser review, a LinkedIn post, and modern X post-first distribution.'
argument-hint: '[post-path] [platform-focus] [cta]'
---

# Writing Publish Prep

## When to Use
- The article is close to done and needs final readiness checks.
- A browser-reviewed post is ready to move from `draft: true` to official site release.
- You need to confirm the date in a `posts/YYYY-MM-DD-slug/` folder matches `index.qmd` before publishing.
- You want platform-specific adaptations for LinkedIn and X.
- You need concise social copy that points back to the article.
- You want modern X formats used by top creators, with standalone posts first and optional follow-up posts.

## Inputs
- Final post path under `posts/`.
- Optional CTA, audience segment, and platform focus.

## Publication State

- Treat the frontmatter `date` in `index.qmd` as the publication-date source of truth.
- The parent directory must be `posts/YYYY-MM-DD-slug/`, with a prefix exactly equal to that date.
- Run this skill only after browser draft review and explicit author approval.
- Confirm that the post has `draft: false` or no `draft` field before the final full-site render.
- For a review-only rebuild, run `quarto render "posts/YYYY-MM-DD-slug/"` from the repository root. Quarto's [project documentation](https://quarto.org/docs/projects/quarto-projects.html) specifies directory-scoped rendering for an incremental project build.
- The source post directory holds authored inputs only. Rendered files belong under the configured `docs/` output directory, never beside `index.qmd` as `index.html`, `index_files/`, or `*_files/`.

## Voice Calibration
- Read the shared [author voice profile](../author-voice/VOICE.md) before adapting copy for LinkedIn or X so platform conventions do not flatten the author's point of view or tone.
- Use the [author voice skill](../author-voice/SKILL.md) to refresh the profile when a new corpus calibration is needed.
- Before approving a post for release, compare its opening, one representative middle section, and conclusion against same-mode published work. Treat a polished but impersonal product-documentation tone as a publication blocker when it displaces the author's viewpoint or practical stakes.

## Procedure
1. Read frontmatter and body for title, description, date, categories, and key takeaway.
2. Run the lifecycle date-path check directly in PowerShell, then verify that the `posts/YYYY-MM-DD-slug/` directory prefix exactly matches the frontmatter date. Treat a mismatch as a blocker until the folder is renamed or the intended date is corrected.

	```powershell
	$postPath = "<post-path>"
	$folderDate = (Split-Path -Path $postPath -Leaf).Substring(0, 10)
	$dateMatch = Select-String -LiteralPath "$postPath/index.qmd" -Pattern '^date:\s*"?(\d{4}-\d{2}-\d{2})"?\s*$' | Select-Object -First 1
	$frontMatterDate = $dateMatch.Matches[0].Groups[1].Value
	if ([string]::IsNullOrWhiteSpace($frontMatterDate) -or $folderDate -ne $frontMatterDate) {
		 throw "Folder date '$folderDate' does not match frontmatter date '$frontMatterDate'."
	}
	Write-Output "PASS: $postPath"
	```

3. Run a final readiness check: clarity, claim support, consistency, links, and local assets referenced by frontmatter.
4. Run the Voice Fidelity Gate: verify that the opening, a representative middle section, and conclusion retain the author's firsthand viewpoint, concrete stakes, and calibrated conviction. A factually correct but generic product-documentation rewrite fails this gate.
5. Confirm explicit author approval, then change `draft: true` to `draft: false` or remove the field.
6. From the repository root, run `quarto render` to regenerate the complete site, including listings, feeds, sitemap, and the final article page. Use this full-site command only after approval; use `quarto render "posts/YYYY-MM-DD-slug/"` for a review-only rebuild.
7. Review the final page in a browser at `docs/posts/YYYY-MM-DD-slug/index.html` or through `quarto preview`; report failures as publication blockers.
8. Draft LinkedIn copy using [linkedin template](./assets/linkedin-template.md).
9. Draft X copy using [x-template](./assets/x-template.md), defaulting to post-first distribution rather than long threads.
10. Create X variants in modern creator formats: one flagship standalone post, one short list-style post, and one contrarian or myth-vs-reality angle.
11. Add a lightweight continuation plan using optional reply follow-ups instead of a required full thread.
12. Provide optional variant hooks and CTA options.
13. Return a short publish checklist and any blocking issues. Do not commit or push unless explicitly requested.

## Output Contract
- Final readiness summary with blocking and non-blocking notes.
- Confirmation that the folder date, frontmatter date, draft status, final render, and browser route are ready for official posting.
- One LinkedIn post draft.
- One flagship standalone X post.
- Two optional X variant posts in different angles.
- Optional reply-based continuation plan (2 to 3 follow-ups) instead of a default long thread.
- Optional alternate openers and CTA variants.

## Guardrails
- Do not fabricate metrics, quotes, or source claims.
- Keep platform tone native and concise.
- Ensure social copy reflects the article faithfully.
- Do not use document-level output options or commit generated `index.html`, `index_files/`, or `*_files/` artifacts inside `posts/YYYY-MM-DD-slug/`.
- Do not approve a post merely because facts, links, and rendering pass. It must also pass the Voice Fidelity Gate.
