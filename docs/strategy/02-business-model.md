# Business Model: Home Maintenance & Troubleshooting App

*Strategic Document 2 of 4 | Last Updated: January 2026*

---

## Executive Summary

This document defines how the app generates revenue, at what scale it becomes viable, and the path to profitability. The recommended model is a **freemium subscription with service provider referral revenue**, targeting **$30/year premium pricing** with a **3-5% conversion rate**. Break-even requires approximately **15,000 monthly active users**.

---

## 1. Revenue Model

### Primary Revenue: Freemium Subscription

#### Pricing Structure

| Tier | Price | Features |
|------|-------|----------|
| **Free** | $0 | Home profile, 3 appliances, basic troubleshooting (5/month), manual maintenance reminders |
| **Premium** | $4.99/month or $29.99/year | Unlimited appliances, unlimited troubleshooting, smart scheduling, push notifications, priority support, maintenance history |
| **Lifetime** | $99.99 (one-time) | All Premium features forever, early access to new features |

#### Rationale for Pricing

- **$29.99/year** aligns with HomeZada's $59/year (positioned as more affordable) and consumer subscription app median
- **Annual discount** (50% vs monthly) encourages commitment and improves retention
- **Lifetime option** captures price-sensitive users while generating upfront cash

#### Conversion Assumptions

| Metric | Conservative | Base | Optimistic |
|--------|-------------|------|------------|
| Free-to-paid conversion | 2% | 4% | 7% |
| Monthly vs annual split | 30%/70% | 25%/75% | 20%/80% |
| Lifetime purchases | 5% of paid | 10% of paid | 15% of paid |

Based on industry benchmarks:
- Freemium consumer apps typically convert 2-5%
- Utility apps at the lower end (~2-3%)
- Apps with clear value demonstration reach 5-8%

---

### Secondary Revenue: Service Provider Referrals

#### Model

When a troubleshooting session concludes with "call a professional," users can request connections to vetted local providers. Revenue generated per successful referral.

#### Commission Structure Options

| Model | Revenue/Referral | Pros | Cons |
|-------|------------------|------|------|
| **Flat fee per lead** | $25-50 | Simple, predictable | Lower revenue potential |
| **Percentage of first job** | 10-15% | Higher revenue on big jobs | Complex tracking |
| **Pay-per-call** | $30-75 | Industry standard | Requires call tracking |

**Recommendation**: Start with **flat fee per qualified lead ($35)** for simplicity. Transition to percentage model after establishing provider relationships.

#### Referral Funnel Assumptions

| Stage | Conversion Rate | Notes |
|-------|-----------------|-------|
| Troubleshooting session | 100% | Starting point |
| Escalates to "call a pro" | 15-20% | Most issues DIY-resolved |
| Clicks "find a provider" | 40-50% | Of those needing pro |
| Submits contact request | 60-70% | Of those who click |
| Provider accepts lead | 80-90% | Depends on lead quality |
| **Net referral rate** | **3-6%** | Of all troubleshooting sessions |

#### Revenue Per User Calculation

| Assumption | Value |
|------------|-------|
| Troubleshooting sessions/user/month | 1.5 |
| Net referral rate | 4% |
| Revenue per referral | $35 |
| **Monthly referral revenue/user** | **$2.10** |

---

### Future Revenue (Not Modeled for v1)

| Stream | Potential | Why Deferred |
|--------|-----------|--------------|
| **Affiliate parts sales** | 5-10% of purchase | E-commerce complexity |
| **Service booking fees** | $10-25/booking | Marketplace complexity |
| **B2B licensing (landlords)** | $99-299/year/property | Different segment |
| **Data insights (anonymized)** | $50K-200K/year | Requires scale |
| **Sponsored provider placement** | $100-500/month | Conflicts with trust |

---

## 2. Cost Structure

### Fixed Costs (Monthly)

| Item | Low | Medium | High | Notes |
|------|-----|--------|------|-------|
| Cloud hosting (AWS/GCP) | $200 | $500 | $1,500 | Scales with users |
| Push notification service | $50 | $100 | $300 | Firebase/OneSignal |
| Database (managed) | $100 | $250 | $500 | PostgreSQL/MongoDB |
| Error monitoring | $50 | $100 | $200 | Sentry/Bugsnag |
| Analytics | $0 | $100 | $300 | Mixpanel/Amplitude |
| Email service | $50 | $100 | $200 | Transactional emails |
| App Store fees | $8 | $8 | $8 | $99/year ÷ 12 |
| **Total Fixed** | **$458** | **$1,158** | **$3,008** | |

### Variable Costs (Per User/Month)

| Item | Cost | Notes |
|------|------|-------|
| Hosting (incremental) | $0.05-0.15 | Per MAU |
| Support (ticket handling) | $0.10-0.30 | Assuming low touch |
| Payment processing | 2.9% + $0.30 | On subscription revenue |
| App Store commission | 15-30% | On subscription revenue |
| **Total Variable** | **$0.15-0.50** | Per MAU |

### Content Maintenance Costs

| Item | Annual Cost | Notes |
|------|-------------|-------|
| Content updates/review | $5,000-10,000 | Quarterly expert review |
| New scenario creation | $3,000-6,000 | 10-20 new scenarios/year |
| Bug fixes/maintenance | $10,000-20,000 | Part-time developer |
| **Total Content/Maintenance** | **$18,000-36,000/year** | |

---

## 3. Unit Economics

### Customer Lifetime Value (LTV)

#### Free User LTV

| Component | Value | Calculation |
|-----------|-------|-------------|
| Referral revenue/month | $2.10 | 1.5 sessions × 4% × $35 |
| Average lifespan | 3 months | Low retention |
| **Free User LTV** | **$6.30** | |

#### Premium User LTV

| Component | Conservative | Base | Optimistic |
|-----------|-------------|------|------------|
| Annual subscription | $29.99 | $29.99 | $29.99 |
| Average tenure | 1.5 years | 2.5 years | 4 years |
| Referral revenue/year | $25 | $25 | $25 |
| Gross subscription LTV | $45 | $75 | $120 |
| Referral LTV | $37 | $63 | $100 |
| **Total Premium LTV** | **$82** | **$138** | **$220** |

#### Blended LTV (Assuming 4% Conversion)

| User Type | % of Users | LTV | Weighted LTV |
|-----------|------------|-----|--------------|
| Free | 96% | $6.30 | $6.05 |
| Premium | 4% | $138 | $5.52 |
| **Blended LTV** | 100% | | **$11.57** |

---

### Customer Acquisition Cost (CAC) Targets

Based on LTV, target CAC for sustainable growth:

| Metric | Target | Rationale |
|--------|--------|-----------|
| Blended LTV | $11.57 | Calculated above |
| Target LTV:CAC ratio | 3:1 | Industry standard |
| **Target CAC** | **$3.86** | Maximum sustainable |
| Stretch target (5:1) | $2.31 | For profitability |

#### CAC Reality Check by Channel

| Channel | Typical CAC | Viable? |
|---------|-------------|---------|
| Organic (ASO, content) | $0.50-2.00 | Yes |
| Referral program | $1-5 | Yes |
| Facebook/Instagram ads | $3-8 | Marginal |
| Google UAC | $2-6 | Marginal |
| Influencer partnerships | $1-4 | Yes |
| PR/earned media | $0.10-0.50 | Yes |

**Implication**: Paid acquisition is challenging with current LTV. Must prioritize organic channels and viral growth.

---

### Payback Period

| Scenario | Premium LTV | CAC | Payback |
|----------|-------------|-----|---------|
| Conservative | $82 | $4 | 1.7 months |
| Base | $138 | $4 | 1.0 months |
| Optimistic | $220 | $4 | 0.6 months |

**Key insight**: Fast payback is possible IF users convert to premium. The challenge is the low conversion rate dragging down blended economics.

---

### Contribution Margin

| Line Item | Per User/Month | Notes |
|-----------|----------------|-------|
| **Revenue (blended)** | $1.16 | $11.57 LTV ÷ 10 mo avg lifespan |
| Variable costs | ($0.25) | Hosting, support |
| Payment processing | ($0.05) | 2.9% + $0.30 on subs |
| App Store take | ($0.15) | ~15% on subscriptions |
| **Contribution margin** | **$0.71** | **61%** |

---

## 4. Financial Scenarios

### Model Assumptions (Common)

| Input | Value |
|-------|-------|
| App Store commission | 15% (small business program) |
| Payment processing | 2.9% + $0.30 |
| Monthly churn (premium) | 5% |
| Annual renewal rate | 70% |

---

### Scenario 1: Conservative (Slow Growth)

| Month | MAU | Premium Users | MRR | Referral Rev | Total Revenue | Costs | Net |
|-------|-----|---------------|-----|--------------|---------------|-------|-----|
| 6 | 2,000 | 40 | $200 | $420 | $620 | $1,500 | -$880 |
| 12 | 5,000 | 100 | $500 | $1,050 | $1,550 | $2,000 | -$450 |
| 18 | 10,000 | 200 | $1,000 | $2,100 | $3,100 | $3,000 | +$100 |
| 24 | 15,000 | 300 | $1,500 | $3,150 | $4,650 | $4,000 | +$650 |

**Break-even**: ~15,000 MAU (Month 18-20)

---

### Scenario 2: Base Case (Moderate Growth)

| Month | MAU | Premium Users | MRR | Referral Rev | Total Revenue | Costs | Net |
|-------|-----|---------------|-----|--------------|---------------|-------|-----|
| 6 | 5,000 | 200 | $1,000 | $1,050 | $2,050 | $2,000 | +$50 |
| 12 | 15,000 | 600 | $3,000 | $3,150 | $6,150 | $4,000 | +$2,150 |
| 18 | 30,000 | 1,200 | $6,000 | $6,300 | $12,300 | $6,000 | +$6,300 |
| 24 | 50,000 | 2,000 | $10,000 | $10,500 | $20,500 | $8,000 | +$12,500 |

**Break-even**: ~5,000 MAU (Month 6)
**Year 2 revenue**: ~$200K ARR

---

### Scenario 3: Optimistic (Strong Product-Market Fit)

| Month | MAU | Premium Users | MRR | Referral Rev | Total Revenue | Costs | Net |
|-------|-----|---------------|-----|--------------|---------------|-------|-----|
| 6 | 10,000 | 700 | $3,500 | $2,100 | $5,600 | $3,000 | +$2,600 |
| 12 | 40,000 | 2,800 | $14,000 | $8,400 | $22,400 | $6,000 | +$16,400 |
| 18 | 80,000 | 5,600 | $28,000 | $16,800 | $44,800 | $10,000 | +$34,800 |
| 24 | 150,000 | 10,500 | $52,500 | $31,500 | $84,000 | $15,000 | +$69,000 |

**Year 2 revenue**: ~$750K ARR

---

## 5. Key Assumptions & Sensitivities

### What Must Be True

| Assumption | Base Value | If Wrong... |
|------------|------------|-------------|
| 4% free-to-paid conversion | 4% | At 2%, need 2x users for same revenue |
| $35 referral fee sustainable | $35 | At $20, referral revenue drops 43% |
| 70% annual renewal | 70% | At 50%, LTV drops 25% |
| 15% escalate to "call pro" | 15% | At 10%, referral revenue drops 33% |
| $4 blended CAC achievable | $4 | At $8, business unprofitable |

### Sensitivity Analysis

| Variable | -50% | Base | +50% | Revenue Impact |
|----------|------|------|------|----------------|
| Conversion rate | 2% | 4% | 6% | High |
| Referral rate | 2% | 4% | 6% | Medium |
| Premium price | $15 | $30 | $45 | Medium |
| User retention | 3 mo | 6 mo | 9 mo | High |
| Referral fee | $17 | $35 | $52 | Medium |

**Most sensitive**: Conversion rate and user retention. These are the levers to optimize.

---

## 6. Funding Implications

### Path 1: Bootstrappable

| Requirement | Value |
|-------------|-------|
| Initial investment | $70K-100K |
| Time to break-even | 12-18 months |
| Risk | High (solo founder) |
| Equity preserved | 100% |

**Strategy**: Keep day job, build nights/weekends, launch lean, iterate to product-market fit before scaling.

**Key milestones**:
1. MVP launch with 25 scenarios
2. 1,000 MAU with 3%+ conversion
3. First $1K MRR month
4. Positive unit economics validated

---

### Path 2: Seed Funding ($250K-500K)

| Requirement | Value |
|-------------|-------|
| Initial raise | $300K |
| Runway | 18-24 months |
| Equity given | 15-20% |
| Use of funds | Dev team, content, marketing |

**Milestones that unlock funding**:
1. Validated MVP with 5,000+ MAU
2. 3%+ conversion to paid
3. Positive referral partner feedback
4. Clear path to $100K ARR

**What investors want to see**:
- Large market (140M US homeowners)
- Clear differentiation (context-aware troubleshooting)
- Repeatable acquisition channel
- Path to $10M+ ARR

---

### Path 3: Strategic Partnership

Partner with an existing player (home warranty company, real estate platform, insurance company) for distribution and funding.

| Partner Type | Value Proposition | Revenue Share |
|--------------|-------------------|---------------|
| Home warranty (Choice, AHS) | Reduce claims via DIY | 50/50 on savings |
| Real estate (Zillow, Realtor.com) | Closing gift / new homeowner onboarding | License fee |
| Insurance (State Farm, Allstate) | Loss prevention | Subsidy for policyholders |

**Pros**: Fast distribution, credibility, funding
**Cons**: Loss of control, revenue share, slow decision cycles

---

## 7. Revenue Roadmap

### Year 1: Validate

| Quarter | Focus | Revenue Target |
|---------|-------|----------------|
| Q1 | Launch iOS, 25 scenarios | $0 (beta) |
| Q2 | Onboard first 5,000 users | $2K MRR |
| Q3 | Launch premium tier | $5K MRR |
| Q4 | Add referral program | $8K MRR |

**Year 1 total**: ~$50K revenue

### Year 2: Scale

| Quarter | Focus | Revenue Target |
|---------|-------|----------------|
| Q1 | Android launch | $12K MRR |
| Q2 | 50 scenarios, expand service providers | $18K MRR |
| Q3 | Partnership pilots | $25K MRR |
| Q4 | Geographic expansion | $35K MRR |

**Year 2 total**: ~$250K revenue

### Year 3: Expand

| Focus | Revenue Target |
|-------|----------------|
| B2B landlord tier | |
| Parts affiliate integration | |
| Premium provider placement | |
| **Year 3 total** | ~$750K-1M revenue |

---

## 8. Key Metrics Dashboard

### North Star Metric

**Troubleshooting sessions resolved without a service call**

This metric captures:
- User value delivered (money saved)
- Product quality (accurate diagnostics)
- Engagement (users returning with problems)

### Supporting Metrics

| Category | Metric | Target |
|----------|--------|--------|
| **Acquisition** | Weekly new users | 500+ |
| **Activation** | Profile completion rate | >60% |
| **Retention** | D7 retention | >20% |
| **Retention** | D30 retention | >10% |
| **Revenue** | Free-to-paid conversion | >4% |
| **Revenue** | Monthly referral clicks | >5% of sessions |
| **Engagement** | Sessions per user/week | >1.5 |

---

## Appendix: Competitive Pricing Reference

| App | Free Tier | Premium Price | Features |
|-----|-----------|---------------|----------|
| HomeZada | Limited | $59-189/year | Full home management, no troubleshooting |
| Centriq (defunct) | Yes | ~$32/year | Manual storage, recall alerts |
| HomeServe | App free | Service plans $25-75/mo | Emergency coverage, not DIY |
| **Our App** | Yes | $30/year | Context-aware troubleshooting + maintenance |

**Positioning**: More affordable than HomeZada, more useful than Centriq was, DIY-focused unlike HomeServe.

---

*Document 2 of 4 | Next: Competitive Analysis →*

---

**Sources**:
- [RevenueCat State of Subscription Apps 2025](https://www.revenuecat.com/state-of-subscription-apps-2025/)
- [First Page Sage SaaS Freemium Conversion Rates](https://firstpagesage.com/seo-blog/saas-freemium-conversion-rates/)
- [Growth-onomics Mobile App Retention Benchmarks 2025](https://growth-onomics.com/mobile-app-retention-benchmarks-by-industry-2025/)
- [Home Improvement Leads Cost 2025](https://agedleadstore.com/home-improvement-leads-cost-2025-guide-by-state-service-type/)
