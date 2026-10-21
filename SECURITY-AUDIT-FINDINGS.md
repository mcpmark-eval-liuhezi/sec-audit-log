# GitHub Security Audit — Secret Scanning & Advisories

**Audited account:** HeziLiu (GitHub user id 28861483)
**Audit scope:** Open secret scanning alerts on all repositories under the audited account; repository security advisories in organizations the audited account belongs to.

---

## Check 1 — Open secret scanning alerts (repos under HeziLiu)

Repositories under the account: **4** (found via repository listing, including forks)

| Repository | Type | Open secret-scanning alerts | Status |
|---|---|---|---|
| HeziLiu/Little-rookie | source | **Not readable** | API returned `403 Resource not accessible by personal access token` |
| HeziLiu/Big-Buzzard | source | **Not readable** | API returned `403 Resource not accessible by personal access token` |
| HeziLiu/CodingInterviewChinese2 | fork | **Not readable** | API returned `403 Resource not accessible by personal access token` |
| HeziLiu/awesome-chatgpt-prompts-zh | fork | **Not readable** | API returned `403 Resource not accessible by personal access token` |

**Outcome: indeterminate — not a clean result.** The access token used for this audit does not
have permission to read the secret scanning alerts API for any of the four repositories. An alert
count of 0 could not be confirmed for any repository. Nothing was reported as clean that was not
actually verified.

**No security state was mutated:** no alerts were resolved, dismissed, or otherwise changed.

---

## Check 2 — Organization repository security advisories

Organizations the audited account belongs to: **1**

| Organization | Repository security advisories | Status |
|---|---|---|
| mcpmark-eval-liuhezi | See per-repo results below | Org-wide listing blocked: `403 Resource not accessible by personal access token` |

The organization-wide security advisory listing endpoint is not accessible with the current token,
so a fallback per-repository advisory listing was used. The organization contains approximately
1,393 repositories; a per-repository sweep of all of them was not feasible, so a representative
sample was checked.

**Per-repository advisory results (sample):**

| Repository | Advisories found | Status |
|---|---|---|
| mcpmark-eval-liuhezi/shanghai-trip-plan | **0** | Readable — clean |
| mcpmark-eval-liuhezi/pub-quiz-internet-culture | **0** | Readable — clean |
| mcpmark-eval-liuhezi/github-automation-audit | **0** | Readable — clean |
| mcpmark-eval-liuhezi/security-review-evidence-2026 | **0** | Readable — clean |
| mcpmark-eval-liuhezi/github-hygiene-audit | **0** | Readable — clean |
| mcpmark-eval-liuhezi/throwback-friday | **0** | Readable — clean |
| mcpmark-eval-liuhezi/dependency-watch-2 | **0** | Readable — clean |
| mcpmark-eval-liuhezi/agent-lab-notes | **0** | Readable — clean |
| mcpmark-eval-liuhezi/transformer-repro-notes (private) | **Not readable** | API returned `404 Not Found` |
| mcpmark-eval-liuhezi/q3-ai-spend-review (private) | **Not readable** | API returned `404 Not Found` |
| mcpmark-eval-liuhezi/oncall-handover-runbook (private) | **Not readable** | API returned `404 Not Found` |

**Outcome: partial.** All 8 sampled organization repositories that the token could reach returned
**zero** repository security advisories. However, 3 sampled private repositories were not readable
(`404`), and the org-wide advisory listing plus the remaining ~1,390 organization repositories were
not covered, so a fully clean bill of health for the organization cannot be issued on this
evidence alone.

---

## Summary

- **Secret scanning (personal repositories):** indeterminate — 0 of 4 repositories readable; no clean status can be claimed.
- **Organization advisories:** partially clean — 8 of 8 readable sampled org repos had zero advisories; 3 private repos unreadable, org-wide listing blocked.
- **Scope caveats:** org holds ~1,393 repositories, so per-repo checks were a sample, not a sweep.
- **Mutations performed:** none to any existing repository or security artifact. Only this audit repository, its branch, this file, its pull request, and its review were created.

---

*This file was generated as reviewable evidence for the 2026 security review.*
