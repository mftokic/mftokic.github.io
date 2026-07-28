---
name: author-voice
description: 'Analyze and recalibrate Mike Tokic\'s writing voice from published Quarto posts. Use when writing, editing, outlining, reviewing, or adapting content that should sound like the author; when a voice brief is needed; or when checking whether a draft has become generic, overly polished, or unlike the author.'
argument-hint: '[draft-path-or-topic] [mode: calibrate|brief|review|rewrite]'
---

# Author Voice Calibration

## Purpose

Build an evidence-based, current understanding of Mike Tokic's writing voice from the published post corpus. Use that understanding to guide a draft, edit, outline, review, or social adaptation without mechanically copying favorite phrases or preserving accidental errors.

## When to Use

- Before drafting a post, article outline, newsletter, or social adaptation in the author's voice.
- Before substantially editing a post when preserving voice matters.
- When asked to assess whether writing sounds like the author.
- When a previous voice brief may be stale because new posts have been published.

## Source of Truth

- Treat `posts/**/index.qmd` as the primary corpus.
- Exclude generated `docs/` output, `_drafts/`, and `posts/_metadata.yml` unless the user specifically asks to compare a draft to published work.
- Read the corpus across its full date range. Do not infer a permanent voice from one post, one series, or only recent work.
- Distinguish intentional style from typos, stale claims, unsupported assertions, and formatting inconsistencies. Preserve the former; correct the latter when editing.
- Treat [VOICE.md](./VOICE.md) as the persisted, shared calibration for other skills and workspace writing conversations.

## Procedure

1. Read [VOICE.md](./VOICE.md) first for the current shared calibration.
2. For `brief`, `review`, or `rewrite` mode, use the saved profile unless the user asks to recalibrate or a new published post may have changed the profile.
3. For `calibrate` mode, inventory `posts/**/index.qmd` and confirm the number of published posts and date range.
4. Read every published post. Keep lightweight notes by date, topic, and mode; do not rely on titles, excerpts, or generated HTML alone.
5. Separate recurring characteristics from topic-specific modes. At minimum, compare practical finance/AI posts, technical time-series teaching posts, personal or career essays, and short recurring formats such as weekend reads.
6. Extract brief, representative examples for recurring rhetorical moves. Quote only what is necessary and identify each source path.
7. Update [VOICE.md](./VOICE.md) with the current evidence-backed profile, coverage metadata, representative sources, and refresh date. Use [voice brief template](./assets/voice-brief-template.md) as the completeness check.
8. For `review` mode, compare the target draft to the saved profile. Identify only material mismatches, explain why they clash, and offer a concrete revision in the author's natural register.
9. For `rewrite` mode, retain the draft's factual meaning, structure, and technical precision unless asked to change them. Revise selected passages, then briefly self-check against the saved profile.
10. State whether the saved profile was used or refreshed, plus its corpus size and latest post date, in the final answer.

## Voice Constraints

- Favor clear, conversational first-person prose rooted in firsthand professional experience or a concrete example.
- Make the argument early, then develop it through practical consequences, examples, and honest tradeoffs.
- Use plain language to explain technical concepts; define jargon only when it helps the reader think or act.
- Allow direct opinions, occasional dry humor, and an informal edge when earned by the subject. Do not manufacture a joke, a hot take, profanity, or a personal anecdote.
- Let sections be uneven when the argument needs it. Do not force a formulaic hook, three symmetric points, or a tidy motivational ending.
- Prefer a firm, specific ending that gives the reader a judgment, caution, or next move over a generic recap or engagement prompt.
- Preserve intellectual humility: distinguish what is observed, inferred, speculative, and known. Do not turn cautious predictions into certainty.

## Anti-Patterns

- Generic creator, management-consulting, or corporate-marketing language.
- Empty superlatives, AI hype, forced contrarian framing, and clickbait hooks.
- Polished but impersonal transitions that remove the author's point of view.
- Invented personal experience, fabricated examples, or claims stronger than the evidence.
- Copying surface quirks, grammar mistakes, or repeated catchphrases as a substitute for voice.

## Output Contract

- Report corpus coverage: number of posts, date range, and post modes represented.
- Provide a compact evidence-backed voice brief or a focused draft comparison, depending on the requested mode.
- Cite representative source paths and keep quotations short.
- Give actionable writing rules: what to preserve, what to avoid, and at least two concrete revision examples when reviewing or rewriting.