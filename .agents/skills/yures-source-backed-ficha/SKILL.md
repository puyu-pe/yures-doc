---
name: yures-source-backed-ficha
description: "Trigger: YURES ficha, source-backed ficha, document YURES behavior. Investigate YURES source and author or update evidence-backed fichas."
license: Apache-2.0
metadata:
  author: "Velnae"
  version: "1.0"
---

## Activation Contract

Use when investigating YURES behavior to create or revise a ficha in this repository.

## Hard Rules

- Resolve `YURES_SOURCE_DIR` before source work. Use CodeGraph before broad source searches.
- Cite concrete source evidence for every factual claim. Never invent buttons, permissions, validations, required steps, or business policy.
- Separate code-enforced behavior from safe operational advice. Mark unsupported conclusions as uncertainty or a human decision.
- Write technical artifacts in English; ficha content follows the repository's established Spanish language.

## Decision Gates

| Finding | Treatment |
| --- | --- |
| Directly traced or tested | Proven behavior |
| Depends on state, config, role, or branch | Conditional behavior |
| Safer operating practice, not enforced by code | Operational recommendation |
| Evidence missing or policy-dependent | Uncertainty or human decision |
| Same objective and operational flow | Update the existing ficha; do not create another |
| Partial overlap | Extend or cross-link existing content; do not duplicate it |
| Distinct objective and operational flow | Creation allowed |
| Ambiguous boundary | Stop and ask the user before writing |

## Execution Steps

1. Before creating a ficha, search relevant `docs/**/*.md`, `mkdocs.yml`, and `documentation/inventory.yml` using the proposed problem, task, expected outcome, and useful synonyms. Read the strongest matches and apply the similarity gate above.
2. Resolve `YURES_SOURCE_DIR`; inspect neighboring ficha(s). Use CodeGraph to trace UI/view to JS/event, route, controller, service/model, and tests. Search hints only: routes, views, POS JS, controllers, services/models, tests.
3. Inspect relevant non-indexed configuration directly when needed. Record file and symbol, route, test, or configuration evidence.
4. When writing, preserve adjacent ficha conventions. Update `mkdocs.yml` and `documentation/inventory.yml` only when the requested change requires it.
5. Run `.venv/bin/mkdocs build --strict --clean`.

## Output Contract

Return similar fichas inspected; create, update, or extend decision with rationale; evidence inspected; proven and conditional behavior; recommendations; uncertainties; changed files; and validation outcome.

## References

- `../../../AGENTS.md`
- `../../../mkdocs.yml`
- `../../../documentation/inventory.yml`
