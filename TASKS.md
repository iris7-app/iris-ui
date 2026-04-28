# TASKS — iris-ui

Open work only. Per `~/.claude/CLAUDE.md` rules : UI-only items
here ; done items removed (use `git tag -l` for history).

---

## 🎨 Long-term UI items (low priority)

- **Dashboard.component.ts split** (1 022 LOC) : per file-length
  hygiene, split into 1 widget = 1 file. Deferred to a fresh
  session (~4 h, the only remaining > 1000 LOC offender in UI).
- **customers.component.ts split** (813 LOC) : partial extraction
  landed 2026-04-22 ; full split by concern (list / CRUD / detail
  tabs) is higher risk because of shared signal state. Deferred.
