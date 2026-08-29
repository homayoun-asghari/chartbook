# ChartBook — 179 MetaTrader screenshots, March–May 2024

Sixteen dates of screen captures taken while building the MetaTrader 5 Expert Advisors in [`mql5-expert-advisors`](https://github.com/homayoun-asghari/mql5-expert-advisors). Charts, Strategy Tester runs, optimisation tables and MetaEditor source windows.

**This is a development record, not a trading journal.** It is not two years of daily chart study, and it should not be read as one.

---

## Provenance

> Reconstructed in 2026 from a filesystem archive. **Commit dates are the real capture times**, taken from the macOS screenshot filenames (`Screenshot 2024-05-02 at 9.26.22 PM.png`) and confirmed against both file birth time and mtime. One commit is dated 2026: this README.
>
> Images were **downscaled to 1600px wide** in 2026 to keep the repository at a workable size; the originals are 3360×2100 and average 0.8 MB. Nothing was cropped, redacted or edited.
>
> One limit worth stating: a modification time is not an authorship time. Here the filename itself carries the capture timestamp, which is stronger evidence than an mtime — but it is still the filesystem's record, not independent proof.

## The shape of it

| Period | Dates | Captures |
|---|---|---|
| 13 March – 29 April 2024 | 14 dates | 25 |
| **1 May 2024** | one day | **63** |
| **2 May 2024** | one day, 13:32 → 21:53 | **91** |

Fourteen dates of a few captures each, then two consecutive days accounting for 154 of the 179. Those two days are one sustained EA calibration and optimisation session, not a habit.

## What is in them

MetaTrader 5 running over Microsoft Remote Desktop, on **demo accounts throughout** — Alpari MT5 demo, and FundedNext and GrowthNext prop-firm evaluation demos. Every window title reads `Demo Account`. No live capital appears anywhere in this repository, and the balances visible are practice funds.

Account numbers are visible in some window title bars. They are demo account identifiers with no password shown, and they are left in rather than redacted — an earlier attempt at automated redaction was verified and failed on 19 of 43 images, and a partial redaction is worse than an honest disclosure.

What recurs across the captures:

- **`MA(8)`, `MA(21)`, `MA(144)` and `ATR(13)`** in the Data Window — the indicator set of `U2_trail` onward in the EA lineage
- **Pivot levels drawn as horizontal rays** — red R1/R2, blue PP, green S1/S2 — computed in code by `ultimatetrendfollowing.mq5`
- **EarnForex's Position Sizer v3.06** (their URL visible in the panel), risk set to **0.12%**, size derived from stop distance — the logic later hand-written into `U3_lotsize.mq5`
- Fibonacci retracements (23.6 / 38.2 / 50 / 61.8 / 78.6)
- **Strategy Tester optimisation tables** for `U_calibration_V2`, maximising Profit Factor across XAUUSD, EURUSD, GBPUSD, NAS100, BRN, US500 and USDJPY
- **MetaEditor source windows** — a large share of the 1–2 May captures show code, not charts
- Instruments: XAUUSD, GBPUSD, UKOUSD (Brent), NDX100, mostly M15 and M30

## What was excluded

Thirteen files, none of them work:

- A MetaTrader **account-history report** (HTML and PNG) and two duplicate copies of each — six files carrying an account number and the account holder's name
- Two pages of a **Persian PDF containing a residential address**
- Three frames of a **third-party YouTube trading channel** and one frame of another trading video — someone else's content
- One frame of a **US immigration form** open in Preview

## Layout

```
charts/YYYY-MM-DD/YYYY-MM-DD_HHMMSS_NNN.png
```

One directory per capture date, filenames carrying the capture time, one commit per date.

## Related

- [`mql5-expert-advisors`](https://github.com/homayoun-asghari/mql5-expert-advisors) — the code being calibrated in these captures
- [`trading-methodology`](https://github.com/homayoun-asghari/trading-methodology) — the written rules being applied
- [`backtest-parameter-sweeps`](https://github.com/homayoun-asghari/backtest-parameter-sweeps) — the trade journal from the same period
