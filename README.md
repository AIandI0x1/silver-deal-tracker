# Silver Deal Tracker

Automated monitoring system for underpriced physical silver listings on eBay.

## Overview

This repository tracks silver bullion deals (coins, bars, rounds) found on:
- **eBay.de** (German marketplace, EUR)
- **eBay.com** (US marketplace, converted to EUR)

Deals are identified when listings have **15%+ margin potential** compared to current spot price plus typical dealer premiums.

## Current Market Parameters

| Parameter | Value |
|-----------|-------|
| Spot Price | ~94 EUR/oz |
| USD/EUR Rate | 0.84 |
| Minimum Margin | 15% |

## Deal Thresholds (for 15%+ margin)

| Product | Max Price (EUR) | Fair Value (EUR) |
|---------|-----------------|------------------|
| 1 oz round/bar | < 80 EUR | ~100-110 EUR |
| 10 oz bar | < 800 EUR | ~1.000-1.100 EUR |
| 1 kg bar | < 2.570 EUR | ~3.200-3.400 EUR |

## Files

- `deals/deals.json` - Machine-readable JSON log of all deals
- `deals/HISTORY.md` - Human-readable deal history
- `scans/` - Individual scan results (optional)

## How It Works

1. Agent scans eBay.de and eBay.com every 2 hours
2. Extracts silver listings with prices
3. Calculates margin vs spot + dealer premiums
4. Logs deals with 15%+ margin to this repo
5. Sends email alert for immediate action

## Disclaimer

This is an automated tracking system. Always verify listings before purchasing:
- Confirm actual silver content (not copper/plated)
- Check seller reputation
- Factor in shipping and fees
- Verify authenticity

---
*Last updated: 2026-01-28T01:35:18.276Z*
