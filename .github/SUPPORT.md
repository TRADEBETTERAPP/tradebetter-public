# Support & FAQ

If you need help with TradeBetter, start here before opening an issue.

---

## Quick Links

| Resource | URL |
|----------|-----|
| TradeBetter App | [https://sndbx.tradebetter.app](https://sndbx.tradebetter.app) |
| Report a Bug | [Open Bug Report](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=bug_report.yml) |
| Request a Feature | [Open Feature Request](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=feature_request.yml) |
| Ask a Question | [Open Help Request](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=help.yml) |
| Security Issues | [Security Policy](https://github.com/TRADEBETTERAPP/tradebetter-public/blob/main/SECURITY.md) |

---

## Frequently Asked Questions

### Accounts & Authentication

**Q: How do I sign in to TradeBetter?**
A: TradeBetter uses wallet-based authentication via Privy. Connect your wallet (MetaMask, Phantom, Coinbase Wallet, or use the Privy embedded wallet) and sign the authentication message. A $BETTER token balance may be required depending on the current gate tier.

**Q: I connected my wallet but got a "gate" error. What does that mean?**
A: TradeBetter uses a token gate that requires a minimum $BETTER token balance. Check the current tier requirements at [https://sndbx.tradebetter.app](https://sndbx.tradebetter.app). Your token balance is re-checked every 10 minutes.

**Q: My session expired. How do I refresh?**
A: Sessions refresh automatically every 10 minutes. If you're logged out, simply reconnect your wallet and sign in again.

---

### Deposits & Withdrawals

**Q: How do I deposit funds?**
A: Navigate to the WALLET view or open the TRADE tab in the signal inspector. Click [DEPOSIT] to get your Unified Deposit Address (UDA). You can deposit USDC or USDT on Base or Ethereum — funds are automatically bridged to Polygon USDC.e for trading.

**Q: My deposit isn't showing up. What should I do?**
A: 
1. Verify the transaction was confirmed on-chain using a block explorer (Basescan, Etherscan).
2. Deposits are detected in real-time but may take 1–5 minutes for cross-chain bridging.
3. Check that you sent a supported asset (USDC or USDT) on a supported chain (Base or Ethereum).
4. If the deposit still doesn't appear after 15 minutes, open a [Help request](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=help.yml) with the transaction hash.

**Q: How do I withdraw funds?**
A: From the WALLET view, click [WITHDRAW]. Select a destination chain (Base, Ethereum, or Arbitrum), enter the amount and recipient address. Withdrawals use the Polymarket Bridge for cross-chain delivery.

**Q: Why can't I withdraw to a specific chain?**
A: Supported withdrawal destinations are Base (8453), Ethereum (1), and Arbitrum (42161). Other chains are not currently supported.

---

### Trading

**Q: How does live trading work?**
A: TradeBetter uses Dome-deployed Safe wallets for order execution on Polymarket. When you initialize trading, a Safe wallet is created and linked to Dome's order router. Orders are placed gaslessly through Polymarket's infrastructure.

**Q: What does "Initialize Trading" do?**
A: It creates your trading wallet (Safe), links it to the Dome order router, deploys the Safe contract, and sets up the necessary token allowances for USDC.e and conditional tokens.

**Q: My trade init failed at a specific step. What now?**
A: The response includes a `step_reached` field telling you which step failed (e.g., `dome_link_prepare`, `dome_set_allowances`). Check the diagnostics panel (WALLET view → [DIAG]) for details. If the issue persists, open a bug report with the step name and any error messages.

**Q: What order types are supported?**
A: Fill-or-Kill (FOK), Fill-and-Kill (FAK), and Good-Till-Cancelled (GTC). These are explained in the order type dropdown in the TRADE tab.

---

### Signals

**Q: What are signal confidence scores?**
A: Confidence is a composite score (0.30–0.98) based on five factors: Position Sizing (25%), Wallet Track Record (30%), Market Conditions (15%), Signal Corroboration (15%), and Timing (15%). Higher scores indicate stronger signals.

**Q: Why are some signals dimmed?**
A: Signals older than 30 minutes are displayed at 50% opacity, and signals older than 60 minutes at 30% opacity. This helps you focus on fresh, actionable signals.

**Q: What does the cluster badge mean?**
A: When multiple tracked wallets take the same side on a market within a 30-minute window, a cluster badge appears (e.g., "[3 wallets]"). This indicates corroborated activity.

---

### Common Error Patterns

| Error | Likely Cause | Fix |
|-------|-------------|-----|
| "Gate check failed" | Insufficient $BETTER balance | Acquire more $BETTER tokens |
| "Failed to fetch balance" | RPC node timeout | Wait 30 seconds and retry; check your network connection |
| "Trade init failed at dome_link" | Dome API temporarily unavailable | Retry in a few minutes; check [DIAG] panel |
| "Deposit address not found" | UDA not yet created | Click [DEPOSIT] to generate your deposit address |
| "Withdrawal failed" | Insufficient Safe balance | Verify your Safe balance in the WALLET view |
| Connection banner (red) | Backend unreachable | Check your internet; click [RECONNECT] in the banner |

---

## Still Need Help?

If your question isn't answered above, [open a Help request](https://github.com/TRADEBETTERAPP/tradebetter-public/issues/new?template=help.yml) with as much detail as possible.
