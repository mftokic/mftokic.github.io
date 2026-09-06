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
9. For `rewrite` mode, identify two or three same-mode published posts before editing. Write down the target's voice anchors: the narrator's point of view, the concrete human or Finance stakes, one recurring rhetorical move, and the appropriate level of certainty.
10. Separate fact correction from prose revision. First identify claims that need qualification or replacement. Then rewrite each correction in the author's natural register; do not let a needed caveat turn into detached, product-documentation prose.
11. Run the Voice Fidelity Gate before finalizing the rewrite. Every substantive section must answer yes to all of these questions:
	- Does it retain a real first-person viewpoint when the topic is based on the author's work or judgment?
	- Does it name a concrete person, workflow, or business consequence rather than only describing a capability?
	- Does it explain why the author built, changed, or cares about something, not only what the software does?
	- Are technical terms used to clarify a point rather than acting as a substitute for the author's voice?
	- Has factual caution preserved the author's conviction and directness?
12. If a section fails the gate, rewrite it around a concrete tension or consequence. Do not solve the problem by adding generic personality, hype, a fabricated anecdote, or copied catchphrases.
13. State whether the saved profile was used or refreshed, plus its corpus size and latest post date, in the final answer.

## Voice Constraints

- Favor clear, conversational first-person prose rooted in firsthand professional experience or a concrete example.
- Make the argument early, then develop it through practical consequences, examples, and honest tradeoffs.
- Use plain language to explain technical concepts; define jargon only when it helps the reader think or act.
- Allow direct opinions, occasional dry humor, and an informal edge when earned by the subject. Do not manufacture a joke, a hot take, profanity, or a personal anecdote.
- Let sections be uneven when the argument needs it. Do not force a formulaic hook, three symmetric points, or a tidy motivational ending.
- Prefer a firm, specific ending that gives the reader a judgment, caution, or next move over a generic recap or engagement prompt.
- Preserve intellectual humility: distinguish what is observed, inferred, speculative, and known. Do not turn cautious predictions into certainty.

## Fidelity Guardrails

- A factual correction changes the claim, not the author's identity on the page. Preserve the author's stance, concrete stakes, and natural degree of force whenever the facts allow it.
- Prefer a first-person build story, a Finance workflow, or a practical consequence over abstract feature descriptions.
- Treat neutral phrases such as "orchestration layer," "workflow," "capability," "candidate," "artifact," or "operationalize" as a warning sign when they replace plain language. They may be necessary technically, but they should not become the paragraph's voice.
- Do not turn every section into an evenly structured explainer. Keep the argument's natural unevenness: a short judgment can sit beside a fuller practical explanation.
- A rewrite should sound like the author explaining work he knows firsthand to a smart colleague, not a package website describing its features.

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