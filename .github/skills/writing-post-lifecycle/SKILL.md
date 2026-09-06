---
name: writing-post-lifecycle
description: 'Move Quarto blog posts from _drafts to posts, enforce that each YYYY-MM-DD post folder matches the publication date in index.qmd, render a browser-review build, and prepare an approved post for official site release. Use when promoting, reviewing, publishing, or scheduling a blog post.'
argument-hint: '[draft-or-post-path] [phase: review|publish]'
user-invocable: true
---

# Quarto Post Lifecycle

## Purpose

Use this skill to move a Quarto article through its actual lifecycle without
creating a mismatch between its URL, frontmatter, rendered page, and publication
state.

## Source Of Truth

The `date` field in the post's `index.qmd` frontmatter is the publication date.
Every post folder must use this exact format:

```
posts/YYYY-MM-DD-slug/index.qmd
```

The `YYYY-MM-DD` directory prefix must exactly match the frontmatter date. Do
not infer a date from an old draft directory. If the author says to publish
today, set the frontmatter date to today's ISO date first, then derive the post
directory from it. If the date is scheduled, preserve the scheduled date.

## Quarto Rendering Rules

This is a Quarto website project whose `_quarto.yml` sets `output-dir: docs`.
From the repository root, render a post by targeting its directory:

```powershell
quarto render "posts/<date>-<slug>/"
```

This follows Quarto's documented [project rendering](https://quarto.org/docs/projects/quarto-projects.html): rendering a project subdirectory incrementally applies the root project configuration and writes the browser output under `docs/`.

The source post directory contains authored material only: `index.qmd` and any
deliberately added images, data, or supporting source files. Never create,
keep, or commit generated document artifacts in that directory, including
`index.html`, `index_files/`, or `*_files/`. The rendered review page belongs
at `docs/posts/<date>-<slug>/index.html`.

Posts inherit `freeze: true` from `posts/_metadata.yml`. Per Quarto's
[execution guidance](https://quarto.org/docs/projects/code-execution.html), a
directory-scoped incremental render still executes its documents. For a
computational post, render in the intended environment and treat an execution
failure as a review blocker rather than assuming frozen output will hide it.

## Phase 1: Draft To Browser Review

1. Read the full draft and its frontmatter. Confirm `title`, `description`,
   `date`, `categories`, and `draft` are present and that `date` is an ISO date.
2. Use the frontmatter date and the existing slug to derive the destination:
   `posts/<date>-<slug>/`. Check that the destination does not already exist.
3. Remove any generated source artifacts such as `index.html`, `index_files/`,
   or `*_files/`. Move `index.qmd` and authored assets together; do not leave
   legitimate images, data, or supporting source files behind in `_drafts/`.
4. Keep `draft: true` during review. This repository uses Quarto
   `draft-mode: unlinked`, so the post can render under `docs/` without being
   added to the public listing.
5. From the repository root, run this date-path check directly in PowerShell.
   It must pass before rendering:

   ```powershell
   $postPath = "posts/<date>-<slug>"
   $folderDate = (Split-Path -Path $postPath -Leaf).Substring(0, 10)
   $dateMatch = Select-String -LiteralPath "$postPath/index.qmd" -Pattern '^date:\s*"?(\d{4}-\d{2}-\d{2})"?\s*$' | Select-Object -First 1
   $frontMatterDate = $dateMatch.Matches[0].Groups[1].Value
   if ([string]::IsNullOrWhiteSpace($frontMatterDate) -or $folderDate -ne $frontMatterDate) {
       throw "Folder date '$folderDate' does not match frontmatter date '$frontMatterDate'."
   }
   Write-Output "PASS: $postPath"
   ```

6. From the repository root, incrementally render only the moved post folder:

   ```powershell
   quarto render "posts/<date>-<slug>/"
   ```

7. Confirm that Quarto created this exact browser-review file:

   ```text
   docs/posts/<date>-<slug>/index.html
   ```

8. Start a local browser-review server on an unused port and report the exact
   URL to the author:

   ```powershell
   $port = if (Get-NetTCPConnection -State Listen -LocalPort 4200 -ErrorAction SilentlyContinue) { 4201 } else { 4200 }
   quarto preview "posts/<date>-<slug>/" --no-browser --port $port
   ```

9. Inspect the review page before calling it ready. Verify the title, metadata,
   headings, links, images, and any code or notebook output. A frontmatter
   `image` must resolve to a real post asset before final publication.

## Phase 2: Approved Post To Official Release

Run this phase only after the author explicitly approves the browser draft.

1. Recheck that the folder prefix and frontmatter `date` still match. If the
   publication date changes, rename the folder, update the date, and remove any
   stale generated page at the old `docs/posts/` route.
2. Run the same direct PowerShell date-path check again. Treat any failure as a
   publication blocker.
3. Run the `writing-publish-prep` skill for final claim checks and social copy.
4. Change `draft: true` to `draft: false` or remove the field. Do not make this
   change during browser draft review.
5. Render the whole Quarto site so navigation, listings, RSS, sitemap, and the
   article page are regenerated together:

   ```powershell
   quarto render
   ```

6. Review the final page in a browser at
   `/posts/<date>-<slug>/index.html`, check the site listing and feed as
   applicable, and report any missing asset or build error as a publication
   blocker.
7. Show the resulting Git status. Commit and push only when the author asks for
   that deployment step explicitly.

## Guardrails

- Never overwrite an existing destination post directory.
- Never silently choose or rewrite a publication date.
- Never publish a `draft: true` post.
- Do not call a page ready for official release when its declared hero image or
  linked local asset is missing.
- Keep the draft-review render scoped to the individual post directory; use a
   full-site render only for the approved release phase.
- Never use document-level output options or retain generated `index.html`,
   `index_files/`, or `*_files/` artifacts in a source post directory.

## Output Contract

Report the source path, destination path, frontmatter date, folder date,
rendered output path, browser URL, and whether the post is `review-ready` or
`publication-ready`. State any blockers separately from non-blocking notes.