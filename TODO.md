# TODO: Remove console.logs and use centralized logger

**Progress: 2/7 steps complete**

1. [ ] Checkout branch: `git checkout -b blackboxai/remove-console-logs-centralized-logger`
2. [ ] ✅ Create TODO.md (this file)
3. [✅] Edit batch 1 files (network-graph/route.ts, useChartExport.ts, alerts/page.tsx, chart-export.ts)
4. [ ] Edit batch 2 files (KeyboardShortcutsContext.tsx, WebSocketErrorBoundary.tsx, OnChainVerification.tsx, analytics-api.ts)
5. [ ] Edit batch 3 files (keyboard-shortcuts/registry.ts, ChartErrorBoundary.tsx, EnhancedNotificationCenter/useEnhancedNotificationCenter.ts, ChartExportButton.tsx)
6. [ ] Edit remaining files + run `pnpm test` + commit
7. [ ] Create PR: `gh pr create --title "Remove console logs: use centralized logger" --body "Replaces 33 console.* with logger (error/warn/info/debug). Prod-safe, redacts sensitive data. Tests pass." --base main`

**Notes:**
- 33 console matches in 15+ frontend/src files.
- logger.ts: dev-only verbose, always error + tracking, redacts keys/addresses.
- No perf/security issues.
- Update this file after each step.

