# Financial Scenarios: Stress-Testing Business Viability

*Strategic Document 5 of 8 | Last Updated: January 2026*

---

## Executive Summary

This document models conservative and pessimistic scenarios to stress-test the business model. **Key finding**: The business remains viable under conservative assumptions (2% conversion, 5% D30 retention) but requires longer runway and lower CAC. Under pessimistic assumptions, the model fails without significant changes.

**Critical insight**: The most sensitive variable is free-to-paid conversion rate. At 1%, the business is not viable with any realistic CAC.

---

## 1. Scenario Definitions

### Scenario Parameters

| Parameter | Base Case | Conservative | Pessimistic |
|-----------|-----------|--------------|-------------|
| Free-to-paid conversion | 4% | 2% | 1% |
| D7 retention | 20% | 12% | 8% |
| D30 retention | 10% | 5% | 3% |
| Free user lifespan (months) | 3 | 1.5 | 1 |
| Premium annual renewal | 70% | 55% | 40% |
| Referral rate (% of sessions) | 4% | 2% | 1% |
| Sessions per user/month | 1.5 | 1.0 | 0.5 |

### Rationale for Conservative Scenario

- **2% conversion**: Bottom of industry benchmark range for freemium consumer apps
- **5% D30 retention**: Slightly above utility app average (3.4% per industry data)
- **1.5-month free lifespan**: Accounts for users who try app once and churn quickly
- **55% renewal**: Accounts for users who forget to cancel or find less value over time

### Rationale for Pessimistic Scenario

- **1% conversion**: What happens if our value prop doesn't resonate
- **3% D30 retention**: Industry average for utility apps
- **1-month free lifespan**: Users try once and never return
- **40% renewal**: High churn due to infrequent use

---

## 2. Revised Unit Economics Per Scenario

### Free User LTV Calculation

| Component | Base | Conservative | Pessimistic |
|-----------|------|--------------|-------------|
| Sessions/month | 1.5 | 1.0 | 0.5 |
| Referral rate | 4% | 2% | 1% |
| Revenue/referral | $35 | $35 | $35 |
| Monthly referral revenue | $2.10 | $0.70 | $0.18 |
| Average lifespan (months) | 3 | 1.5 | 1 |
| **Free User LTV** | **$6.30** | **$1.05** | **$0.18** |

**Key insight**: Free user LTV drops 83% from base to conservative. This significantly impacts blended economics.

---

### Premium User LTV Calculation

| Component | Base | Conservative | Pessimistic |
|-----------|------|--------------|-------------|
| Annual subscription | $29.99 | $29.99 | $29.99 |
| Average tenure (years) | 2.5 | 1.8 | 1.2 |
| Gross subscription LTV | $75 | $54 | $36 |
| Annual referral revenue | $25 | $12 | $4 |
| Referral LTV | $63 | $22 | $5 |
| **Premium User LTV** | **$138** | **$76** | **$41** |

---

### Blended LTV Calculation

| Scenario | Free % | Free LTV | Premium % | Premium LTV | **Blended LTV** |
|----------|--------|----------|-----------|-------------|-----------------|
| Base | 96% | $6.30 | 4% | $138 | **$11.57** |
| Conservative | 98% | $1.05 | 2% | $76 | **$2.55** |
| Pessimistic | 99% | $0.18 | 1% | $41 | **$0.59** |

---

### Viable CAC Thresholds

| Scenario | Blended LTV | Target LTV:CAC (3:1) | **Max Viable CAC** |
|----------|-------------|---------------------|-------------------|
| Base | $11.57 | 3:1 | **$3.86** |
| Conservative | $2.55 | 3:1 | **$0.85** |
| Pessimistic | $0.59 | 3:1 | **$0.20** |

**Critical finding**:
- **Conservative**: Only organic acquisition with near-zero cost is viable ($0.85 CAC)
- **Pessimistic**: No viable acquisition path exists

---

## 3. Financial Projections (24-Month)

### Base Case Projection

| Month | MAU | Premium | MRR | Referral | Total Rev | Costs | Net |
|-------|-----|---------|-----|----------|-----------|-------|-----|
| 3 | 2,000 | 80 | $400 | $420 | $820 | $1,500 | -$680 |
| 6 | 5,000 | 200 | $1,000 | $1,050 | $2,050 | $2,000 | +$50 |
| 12 | 15,000 | 600 | $3,000 | $3,150 | $6,150 | $4,000 | +$2,150 |
| 18 | 30,000 | 1,200 | $6,000 | $6,300 | $12,300 | $6,000 | +$6,300 |
| 24 | 50,000 | 2,000 | $10,000 | $10,500 | $20,500 | $8,000 | +$12,500 |

**Break-even**: Month 6 (~5,000 MAU)
**Year 2 Net**: +$150K cumulative

---

### Conservative Case Projection

| Month | MAU | Premium | MRR | Referral | Total Rev | Costs | Net |
|-------|-----|---------|-----|----------|-----------|-------|-----|
| 3 | 1,500 | 30 | $150 | $105 | $255 | $1,500 | -$1,245 |
| 6 | 3,500 | 70 | $350 | $245 | $595 | $1,800 | -$1,205 |
| 12 | 8,000 | 160 | $800 | $560 | $1,360 | $2,500 | -$1,140 |
| 18 | 15,000 | 300 | $1,500 | $1,050 | $2,550 | $3,500 | -$950 |
| 24 | 25,000 | 500 | $2,500 | $1,750 | $4,250 | $4,500 | -$250 |

**Break-even**: Month 26-28 (~30,000 MAU)
**Year 2 Net**: -$25K cumulative (still burning)

**Implication**: Conservative scenario requires 18-24 months longer runway than base case.

---

### Pessimistic Case Projection

| Month | MAU | Premium | MRR | Referral | Total Rev | Costs | Net |
|-------|-----|---------|-----|----------|-----------|-------|-----|
| 3 | 1,000 | 10 | $50 | $18 | $68 | $1,500 | -$1,432 |
| 6 | 2,000 | 20 | $100 | $35 | $135 | $1,800 | -$1,665 |
| 12 | 4,000 | 40 | $200 | $70 | $270 | $2,200 | -$1,930 |
| 18 | 6,000 | 60 | $300 | $105 | $405 | $2,500 | -$2,095 |
| 24 | 8,000 | 80 | $400 | $140 | $540 | $2,800 | -$2,260 |

**Break-even**: Never (at current model)
**Year 2 Net**: -$45K cumulative (accelerating losses)

**Implication**: Pessimistic scenario is not viable. Would require fundamental model changes.

---

## 4. Runway Requirements

### Initial Investment Comparison

| Scenario | Months to Break-even | Monthly Burn (Avg) | **Runway Needed** |
|----------|---------------------|-------------------|------------------|
| Base | 6 | $1,000 | **$70-100K** |
| Conservative | 26-28 | $1,100 | **$150-180K** |
| Pessimistic | Never | $1,800 | **N/A (pivot)** |

### Recommended Starting Capital by Scenario

| Scenario | Dev + Launch | Runway Buffer | **Total Needed** |
|----------|--------------|---------------|------------------|
| Base | $100K | $20K (2 months) | **$120K** |
| Conservative | $100K | $80K (8 months) | **$180K** |
| Pessimistic | N/A | N/A | **Don't launch** |

---

## 5. Decision Triggers

### Kill Criteria (Stop and Pivot)

| Metric | Threshold | Timeframe | Action |
|--------|-----------|-----------|--------|
| D7 retention | <8% | Month 2-3 | Pause acquisition, fix onboarding |
| D30 retention | <3% | Month 3-4 | Major product pivot or kill |
| Free-to-paid conversion | <1% | Month 4-6 | Rethink value prop or monetization |
| Profile completion | <30% | Month 1-2 | Simplify onboarding |
| Blended CAC | >$5 organic | Month 3-4 | Cut marketing spend, focus on product |

### Go/No-Go: Android Expansion

| Criteria | Threshold | Status |
|----------|-----------|--------|
| iOS MAU | >10,000 | Required |
| D30 retention | >8% | Required |
| Free-to-paid conversion | >2.5% | Required |
| Referral revenue validated | >$500/month | Required |
| iOS profitable | Contribution margin >0 | Required |

**Decision rule**: ALL criteria must be met before investing in Android development.

### Go/No-Go: Paid Acquisition

| Criteria | Threshold | Status |
|----------|-----------|--------|
| Organic CAC | <$2 | Required |
| LTV:CAC ratio (organic) | >4:1 | Required |
| D30 retention | >10% | Required |
| Free-to-paid conversion | >3% | Required |
| Premium user payback | <3 months | Required |

**Decision rule**: ALL criteria must be met. If any fail, paid acquisition will accelerate losses.

---

## 6. Sensitivity Analysis

### Impact of Each Variable on Blended LTV

| Variable | -50% Change | Impact on Blended LTV |
|----------|-------------|----------------------|
| Conversion rate (4% → 2%) | -78% | **Most sensitive** |
| Free user lifespan (3 → 1.5 mo) | -42% | High |
| Sessions/user/month (1.5 → 0.75) | -35% | Medium-High |
| Referral rate (4% → 2%) | -30% | Medium |
| Premium renewal (70% → 35%) | -18% | Medium |
| Referral fee ($35 → $17.50) | -25% | Medium |

**Strategic implication**: Focus optimization efforts on conversion rate first, then retention.

---

### Conversion Rate Sensitivity Table

| Conversion Rate | Blended LTV | Max Viable CAC | Verdict |
|-----------------|-------------|----------------|---------|
| 5% | $14.25 | $4.75 | Healthy |
| 4% (base) | $11.57 | $3.86 | Viable |
| 3% | $8.89 | $2.96 | Tight margins |
| 2% (conservative) | $6.20 | $2.07 | Organic only |
| 1% (pessimistic) | $3.52 | $1.17 | Not viable |

---

## 7. Scenario-Based Strategic Adjustments

### If Landing in Conservative Scenario

| Problem | Adjustment |
|---------|------------|
| CAC too high | 100% organic focus; no paid until metrics improve |
| Low conversion | Test different paywall positions; add trial period |
| Low retention | Improve onboarding; add engagement features (reminders, tips) |
| Low referral revenue | Increase referral fee (if providers will pay) or deprioritize |

### If Landing in Pessimistic Scenario

| Problem | Pivot Option |
|---------|--------------|
| Fundamental value prop failure | Pivot to B2B (property management, landlords) |
| Wrong target audience | Reposition for DIY enthusiasts (higher engagement segment) |
| Can't compete with free alternatives | Partner with HomeZada/Dib instead of competing |
| Revenue model doesn't work | Explore content licensing, white-label to insurers |

---

## 8. Key Takeaways

### The Business Works If:
1. Free-to-paid conversion ≥2%
2. D30 retention ≥5%
3. Organic CAC ≤$2
4. Service providers will pay $35+/lead

### The Business Fails If:
1. Conversion <1.5% (no viable acquisition path)
2. D30 retention <3% (not enough engagement for referral revenue)
3. Organic CAC >$3 (even organic channels too expensive)
4. Providers won't pay for leads (removes 40%+ of revenue)

### Validation Priorities (Before Development)
1. **Test willingness to pay** - Landing page with price shown
2. **Validate provider interest** - 10 interviews, confirm $35 acceptable
3. **Test engagement hypothesis** - Prototype troubleshooting flow, measure completion
4. **Measure profile completion** - How simple must it be?

---

## Appendix: Detailed Monthly Projections

### Base Case - Full 24 Months

| Mo | New Users | Churn | MAU | Premium | MRR | Ref Rev | Total | Costs | Net | Cumulative |
|----|-----------|-------|-----|---------|-----|---------|-------|-------|-----|------------|
| 1 | 500 | 0 | 500 | 20 | $100 | $105 | $205 | $1,500 | -$1,295 | -$1,295 |
| 2 | 600 | 100 | 1,000 | 40 | $200 | $210 | $410 | $1,500 | -$1,090 | -$2,385 |
| 3 | 700 | 200 | 1,500 | 60 | $300 | $315 | $615 | $1,500 | -$885 | -$3,270 |
| 6 | 1,000 | 500 | 5,000 | 200 | $1,000 | $1,050 | $2,050 | $2,000 | +$50 | -$4,320 |
| 12 | 2,000 | 1,000 | 15,000 | 600 | $3,000 | $3,150 | $6,150 | $4,000 | +$2,150 | +$5,580 |
| 18 | 3,000 | 1,500 | 30,000 | 1,200 | $6,000 | $6,300 | $12,300 | $6,000 | +$6,300 | +$45,780 |
| 24 | 4,000 | 2,000 | 50,000 | 2,000 | $10,000 | $10,500 | $20,500 | $8,000 | +$12,500 | +$120,780 |

### Conservative Case - Full 24 Months

| Mo | New Users | Churn | MAU | Premium | MRR | Ref Rev | Total | Costs | Net | Cumulative |
|----|-----------|-------|-----|---------|-----|---------|-------|-------|-----|------------|
| 1 | 400 | 0 | 400 | 8 | $40 | $28 | $68 | $1,500 | -$1,432 | -$1,432 |
| 2 | 450 | 100 | 750 | 15 | $75 | $52 | $127 | $1,500 | -$1,373 | -$2,805 |
| 3 | 500 | 200 | 1,050 | 21 | $105 | $74 | $179 | $1,500 | -$1,321 | -$4,126 |
| 6 | 700 | 400 | 3,500 | 70 | $350 | $245 | $595 | $1,800 | -$1,205 | -$8,500 |
| 12 | 1,200 | 700 | 8,000 | 160 | $800 | $560 | $1,360 | $2,500 | -$1,140 | -$15,300 |
| 18 | 1,800 | 1,100 | 15,000 | 300 | $1,500 | $1,050 | $2,550 | $3,500 | -$950 | -$21,000 |
| 24 | 2,500 | 1,500 | 25,000 | 500 | $2,500 | $1,750 | $4,250 | $4,500 | -$250 | -$24,500 |

---

*Document 5 of 8 | Next: Validation Plan →*
