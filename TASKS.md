# TASKS — iris-ui

Open work only. Per `~/.claude/CLAUDE.md` rules : UI-only items
here ; done items removed (use `git tag -l` for history).

Recreated 2026-04-28 to capture the **Iris rebrand** in flight.

---

## 🌀 IRIS REBRAND (in flight 2026-04-28)

Coordinated rename Iris → Iris. See full context + phases in
[Java TASKS.md](https://gitlab.com/iris-7/iris-service-java/-/blob/main/TASKS.md#-iris-rebrand-in-flight-2026-04-28).

UI-side scope :

- **Code-level** : 138 files, 789 refs to "iris". Affects :
  - Angular routes (`/iris/*` if any → `/iris/*`)
  - Feature module names + component class names with "Iris" prefix
  - `ApiService` env URLs (`iris7.duckdns.org` → `iris1.duckdns.org`)
  - Component copydeck text ("Iris watchtower" → "Iris — 7 FACETS")
  - RBAC role mappings if they include "iris"
  - GitLab CI variables references
- **Banner illustration** : if the UI renders a Iris banner
  in-app (about page, splash), update to the new Iris visual
  `02o-iris-final.svg`.
- **README narrative** : Iris → Iris in user-facing copy + new
  framing "observability-first showcase d'un projet moderne complet
  (cloud · sécurité · IA · stack tech à jour)".
- **Phase 4 (code rename)** : 🔴 dedicated session (138 files,
  cross-cutting Angular structure changes).

### ✅ Decisions verrouillées

- **Name** : `Iris`
- **7 axes ROYGBIV** : OBSERVE · INFRA·CLOUD · SECURITY · CI·CD · ARCH · AI·ML · QUALITY
- **Visual** : `02o-iris-final.svg` — robot diaphragm + transparence + HUD overlay
- **Tagline** : `7 FACETS`
- **Color mapping** : RED=OBSERVE · ORANGE=INFRA·CLOUD · YELLOW=SECURITY · GREEN=CI·CD · CYAN=ARCHITECTURE · BLUE=AI·ML · VIOLET=QUALITY

These 7 colors should also be available as CSS custom properties
in `src/styles.scss` (if not already) for any future components
that need to surface the axis indication.

---

## 🟡 Stability-check ATTENTION items (2026-04-28)

From `iris-service-java/docs/audit/stability-2026-04-28-0447.md` :

- 🟢 **GitHub mirror sync** : confirmed in sync 2026-04-28 (4 commits
  pushed in this session).
- 🟢 **README dead doc-links** : ✅ resolved 2026-04-28 ([!176](https://gitlab.com/iris-7/iris-ui/-/merge_requests/176))
  — broken links to gitignored `docs/{compodoc,typedoc}/` replaced
  with descriptive text.
- 🟢 **Lefthook hooks** : ✅ installed 2026-04-28 (was missing
  pre-commit/pre-push wiring after path migration).

---

## 🎨 Long-term UI items (low priority)

- 🟢 **Dashboard.component.ts split** (1 022 LOC) : per file-length
  hygiene, split into 1 widget = 1 file. Deferred to a fresh
  session (~4 h, the only remaining > 1000 LOC offender in UI per
  the 2026-04-22 wave summary).
- 🟢 **customers.component.ts split** (813 LOC) : partial extraction
  landed 2026-04-22 ; full split by concern (list / CRUD / detail
  tabs) is higher risk because of shared signal state. Deferred.
