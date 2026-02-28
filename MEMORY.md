# MEMORY.md - Long-term Memory

Capture what matters. Decisions, context, things to remember. Skip the secrets unless asked to keep them.

## Key Setup (as of 2026-02-27)
- Three-CSV ledger in expenses directory:
  - expense_tracker.csv (Master ledger)
  - expense_tracker_weekly.csv (Weekly totals)
  - expense_tracker_monthly.csv (Monthly totals)
- Cadence and delivery:
  - Daily reports from expense_tracker.csv at 22:30 Shanghai time
  - Weekly reports on Sunday 22:30 Shanghai time
  - Monthly reports on 1st of month 10:00 Shanghai time for the previous month
  - Reports delivered via Orchestrator relay to WhatsApp using:
    openclaw agent --agent main --message '<report>' --deliver
- Data layout decisions:
  - Currency columns: RMB, EUR, USD
  - Master ledger vs. summaries approach: Master ledger + derived weekly/monthly summaries
- Memory anchors to persist:
  - File paths: /Users/enterwizard/.openclaw/workspace-banker/expenses/expense_tracker.csv
  - Weekly: /Users/enterwird/.openclaw/workspace-banker/expenses/expense_tracker_weekly.csv
  - Monthly: /Users/enterwizard/.openclaw/workspace-banker/expenses/expense_tracker_monthly.csv
- Cron job names and purposes:
  - EXPENSE_DAILY (daily report)
  - EXPENSE_WEEKLY (weekly report)
  - EXPENSE_MONTHLY (monthly report)
- Relay pattern: Orchestrator via WhatsApp as the delivery channel

If you want more detail or other anchors added (e.g., sample memory entries), I can append them.