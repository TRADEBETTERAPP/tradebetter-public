# Issue Guide

This guide helps you write issues that get resolved quickly.

---

## Good vs Bad Issues

### Bug Report — Good Example

> **Title:** [Bug]: Deposit modal shows 'undefined' for USDC balance when connected via MetaMask on Base
>
> **Summary:** When connected via MetaMask on Base, the deposit modal balance field displays "undefined" instead of the actual USDC balance.
>
> **Steps to Reproduce:**
> 1. Connect MetaMask wallet (Base network)
> 2. Navigate to WALLET view
> 3. Click [DEPOSIT]
> 4. Select Base chain and USDC token
> 5. Observe balance field
>
> **Expected:** Balance shows "42.50 USDC"
> **Actual:** Balance shows "undefined"
>
> **Environment:** macOS 15.1, Chrome 131, MetaMask 12.8.1, Base network

**Why it's good:** Specific title, numbered reproduction steps, exact values, full environment info.

### Bug Report — Bad Example

> **Title:** deposits broken
>
> **Summary:** can't deposit
>
> **Steps:** tried to deposit and it didn't work

**Why it's bad:** Vague title, no reproduction steps, no environment info, no expected/actual behaviour. The team can't act on this without asking follow-up questions, which delays resolution.

---

### Feature Request — Good Example

> **Title:** [Feature]: Wallet reputation indicator on signal cards
>
> **Problem:** When scanning the signal feed, I can't quickly tell which signals come from wallets that have historically been profitable to copy. I have to open each signal's PERFORMANCE tab individually.
>
> **Proposed Solution:** Add a small colored dot or badge on SignalCardCompact showing the source wallet's copy-trade ROE tier (green for >10%, yellow for 0-10%, red for negative). Data is already available from the wallet analytics cache.
>
> **Alternatives:** I could star wallets manually using the annotation feature, but that requires me to maintain the list and doesn't update automatically.
>
> **Impact:** High — I review 50+ signals per session and this would save significant time.

---

## How to Get Faster Responses

1. **Search first.** Check [existing issues](https://github.com/TRADEBETTERAPP/tradebetter-public/issues) — your problem may already be reported. Add a 👍 reaction to upvote it instead of opening a duplicate.

2. **Use the templates.** Fill out every required field. Skipping fields means the team has to ask follow-up questions, which adds days.

3. **Be specific.** "The app crashes" is not actionable. "Clicking [TRADE] on a 15m Up/Down signal with confidence 0.92 causes a white screen on Chrome 131" is.

4. **Include evidence.** Screenshots, screen recordings, browser console logs (`F12` → Console tab), and network traces (`F12` → Network tab) dramatically speed up diagnosis.

5. **One issue per report.** Don't combine multiple bugs or requests into a single issue. Each gets its own lifecycle and labels.

6. **Redact sensitive data.** Before posting screenshots or logs, remove wallet addresses (if you prefer privacy), API keys, tokens, and any personal information.

7. **Use reactions, not comments.** If you're experiencing the same bug as someone else, add a 👍 reaction. Commenting "+1" or "same" creates noise and doesn't help prioritization.

---

## What Happens Next

After you open an issue:

| Stage | Timeline | What to expect |
|-------|----------|----------------|
| `triage` | 1–3 business days | Team reviews and categorizes your issue |
| `accepted` | After triage | Issue is confirmed and prioritized |
| `in-progress` | Varies | A team member is working on it |
| `shipped` | After deployment | Fix is live; issue auto-closes via internal PR |

You'll receive GitHub notifications at each stage transition. If you don't hear back within a week, it's okay to leave a polite comment asking for an update.
