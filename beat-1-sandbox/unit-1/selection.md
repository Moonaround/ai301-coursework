# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

### Issue link
https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73

### Verdict output
```json
{
  "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/73",
  "checks": [
    {"name": "repo_active", "grade": "pass", "evidence": "3 commits on 2026-09-16 (7 days before capture date 2026-09-23), satisfying >=3 commits in last 30 days"},
    {"name": "issue_open", "grade": "pass", "evidence": "Issue state is Open; labels are bug, docs, good first issue, tier-1 (no closed label)"},
    {"name": "issue_unclaimed", "grade": "pass", "evidence": "No comments, no assignees, no linked PRs on the issue"},
    {"name": "issue_scope", "grade": "pass", "evidence": "Bounded 2-file doc-consistency fix (README vs .env.example LLM API key naming), estimated 1-2 hours"},
    {"name": "repo_policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md states commit/branch/CI/testing rules but no AI-generated-code ban; silence passes per evidence-guide"}
  ],
  "verdict": "accept"
}
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

### Run history
1. 11/20 scored items
2. 18/20 scored items

### Issue analysis
I evaluated issue-19. My rubric graded it as a `reject` due to the `issue_scope` constraint because the description flagged layout complexity metrics. The gold standard label marked it as an `accept`. My rubric read the issue this way because the strict keywords triggered our scope boundary check.

### Check rationale
Check wording: `| repo_active | repo-facts | The repo has at least 3 commits in the last 30 days. | required |`
Rationale: This check ensures that the repository is actively maintained by checking real commit history rather than relying on abstract descriptors, protecting contributors from working on abandoned or dead codebases.

### Trade-offs
Setting a fixed threshold of 3 commits in 30 days protects against dead projects, but it may accidentally filter out completely stable, lower-maintenance repositories that only receive occasional patches.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

### Selection rationale
1. This issue fits my interest well because it targets a clean documentation and environment variables setup alignment, which matches the timeframe available.
2. The verdict correctly identified that the repository is active and that the 2-file scope is compact, which the rubric could safely verify without relying on soft adjectives.
3. The anticipated difficulty in claiming it is low, since there are no active assignees or competing PR links open.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
