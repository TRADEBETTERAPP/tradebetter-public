# TradeBetter — Public Issues & Feedback

Welcome to the public issue tracker for **TradeBetter**, the quantitative trading signal platform for Polymarket prediction markets.

> **This repository contains no application source code.**
> It exists solely as a public interface for bug reports, feature requests, and user support.

---

## What You Can Do Here

| Action | Link |
|--------|------|
| Report a bug | [Open Bug Report](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=bug_report.yml) |
| Request a feature | [Open Feature Request](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=feature_request.yml) |
| Ask for help | [Open Help / Question](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=help.yml) |
| View known issues | [Browse All Issues](https://github.com/TRADEBETTERAPP/tradebetter-public/issues) |

---

## How It Works

1. **You open an issue** using one of the templates above.
2. **The team triages it** and applies a label (see below).
3. **Accepted issues** are linked to internal pull requests in our private repositories.
4. **When the fix ships**, the internal PR references this issue (e.g. `Closes TRADEBETTERAPP/tradebetter-public#42`), and the issue is **automatically closed**.

You'll see a notification when your issue is resolved.

---

## Labels

### Lifecycle Labels

| Label | Color | Meaning |
|-------|-------|---------|
| `bug` | 🔴 Red | Confirmed bug |
| `feature` | 🔵 Blue | Feature request |
| `triage` | 🟡 Yellow | Awaiting team review |
| `accepted` | 🟢 Green | Accepted and scheduled |
| `in-progress` | 🟠 Orange | Actively being worked on |
| `shipped` | 🟩 Dark Green | Fix/feature deployed — issue auto-closed and locked |
| `wontfix` | ⚪ Grey | Will not be addressed — issue auto-closed |
| `duplicate` | 🟣 Purple | Duplicate of another issue — issue auto-closed |
| `stale` | 🟤 Brown | No activity for 30 days — auto-closed after 14 more days |

### Priority Labels (team-only, set via `/priority` command)

| Label | Color | Meaning |
|-------|-------|---------|
| `priority:critical` | 🔴 Red | Production-breaking, immediate attention |
| `priority:high` | 🟠 Orange | Significant impact, next sprint |
| `priority:medium` | 🟡 Yellow | Moderate impact, scheduled |
| `priority:low` | 🔵 Blue | Minor, when capacity allows |

### Metrics Label

| Label | Color | Meaning |
|-------|-------|---------|
| `metrics` | ⚪ Grey | Auto-generated monthly issue metrics report |

---

## Automation

This repository uses GitHub Actions to manage the full issue lifecycle automatically:

| Workflow | What It Does |
|----------|-------------|
| **Auto-label** | Applies `bug`/`feature`/`triage` labels based on issue template type |
| **Auto-comment** | Posts a category-specific welcome comment with links to docs |
| **Label actions** | When team applies `shipped`/`wontfix`/`duplicate`/`accepted`/`in-progress`, auto-comments, auto-closes, or auto-locks as appropriate |
| **Stale issues** | Marks issues with no activity for 30 days as `stale`; auto-closes after 14 more days. Issues labeled `accepted`/`in-progress`/`shipped` are exempt |
| **Lock threads** | Locks closed issues after 14 days of inactivity to reduce noise |
| **Issue metrics** | Generates a monthly report (time-to-first-response, time-to-close, label durations) |
| **Slash commands** | Supports `/assign` (self-assign) and `/priority critical\|high\|medium\|low` (team-only) in issue comments |
| **First interaction** | Welcomes first-time contributors with tips for getting faster responses |

### Slash Commands

Anyone can use these commands in issue comments:

| Command | Who | Effect |
|---------|-----|--------|
| `/assign` | Anyone | Self-assign to the issue |
| `/unassign` | Anyone | Remove yourself from the issue |
| `/priority critical` | Org members only | Set priority label |
| `/priority high` | Org members only | Set priority label |
| `/priority medium` | Org members only | Set priority label |
| `/priority low` | Org members only | Set priority label |

---

## Cross-Repo Linking

Internal pull requests in private repositories can reference public issues:

```
Closes TRADEBETTERAPP/tradebetter-public#42
```

When the PR merges, the referenced issue is automatically closed by GitHub.

---

## Before You Post

- Search [existing issues](https://github.com/TRADEBETTERAPP/tradebetter-public/issues) first — your problem may already be reported.
- Read the [Issue Guide](.github/ISSUE_GUIDE.md) for tips on writing clear, actionable reports.
- Read [CONTRIBUTING.md](CONTRIBUTING.md) for submission guidelines.
- **Never post** credentials, API keys, private keys, wallet seed phrases, or exploit details. See [SECURITY.md](SECURITY.md).

---

## Links

- **App:** [https://sndbx.tradebetter.app](https://sndbx.tradebetter.app)
- **Support & FAQ:** [.github/SUPPORT.md](.github/SUPPORT.md)
- **Security Policy:** [SECURITY.md](SECURITY.md)
- **Contributing:** [CONTRIBUTING.md](CONTRIBUTING.md)

---

## Permissions

- **Anyone** can open issues and comment.
- **Only TRADEBETTERAPP org members** can label, assign, and close issues.
