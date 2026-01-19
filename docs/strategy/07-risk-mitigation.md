# Risk Mitigation Playbook

*Strategic Document 7 of 8 | Last Updated: January 2026*

---

## Executive Summary

This playbook converts identified risks into **actionable response plans** with specific triggers, immediate actions, and escalation paths. The goal is to detect problems early and respond systematically rather than reactively.

**Top 3 existential risks**:
1. Low free-to-paid conversion (<2%)
2. User abandonment during onboarding (<40% completion)
3. Liability from bad advice causing user harm

---

## 1. Risk Registry

### Complete Risk Inventory

| ID | Risk | Likelihood | Impact | Category | Owner |
|----|------|------------|--------|----------|-------|
| R01 | Low free-to-paid conversion | Medium | High | Revenue | Product |
| R02 | User abandons during profile setup | High | High | Retention | Product |
| R03 | Content gaps frustrate users | Medium | High | Product | Content |
| R04 | Bad advice causes damage/injury | Low | Critical | Legal | Legal/Product |
| R05 | Service provider network too thin | Medium | Medium | Revenue | BD |
| R06 | Paid CAC exceeds LTV | Medium | High | Growth | Marketing |
| R07 | Competitor launches similar feature | Medium | Medium | Competitive | Product |
| R08 | App Store rejection | Low | Medium | Technical | Engineering |
| R09 | Label scanning doesn't work well | Medium | Medium | Technical | Engineering |
| R10 | Low D30 retention (<5%) | Medium | High | Retention | Product |
| R11 | Providers won't pay $35/lead | Medium | Medium | Revenue | BD |
| R12 | Legal liability unclear | Medium | High | Legal | Legal |
| R13 | Poor App Store ratings (<4.0) | Medium | High | Growth | Product |
| R14 | Team burnout / solo founder risk | Medium | High | Operational | Founder |
| R15 | Funding runs out before PMF | Medium | Critical | Financial | Founder |

### Risk Matrix

```
         │ Low Impact │ Medium Impact │ High Impact │ Critical │
─────────┼────────────┼───────────────┼─────────────┼──────────┤
High     │            │ R02           │             │          │
Likelihood            │               │             │          │
─────────┼────────────┼───────────────┼─────────────┼──────────┤
Medium   │            │ R05, R09, R11 │ R01, R06,   │ R04, R15 │
Likelihood            │               │ R07, R10,   │          │
         │            │               │ R12, R13    │          │
─────────┼────────────┼───────────────┼─────────────┼──────────┤
Low      │            │ R08           │ R14         │          │
Likelihood            │               │             │          │
```

---

## 2. Detailed Mitigation Plans

### R01: Low Free-to-Paid Conversion

**Risk**: Conversion rate falls below 2%, making business unviable.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Conversion rate | <3% | Month 3-4 |
| Red alert | Conversion rate | <2% | Month 4-5 |

**Immediate Response (Yellow)**:
1. Analyze funnel: Where are users dropping off?
2. A/B test paywall positioning (earlier vs later)
3. Test alternative price points ($19.99/yr, $39.99/yr)
4. Add 7-day free trial of Premium
5. Survey churned users: "What would make you pay?"

**Escalation Response (Red)**:
1. Consider switching to ad-supported model
2. Explore B2B pivot (property management, insurance)
3. Test lifetime purchase option more aggressively
4. Evaluate acquisition by competitor with distribution

**Prevention**:
- Validate willingness to pay in pre-launch interviews
- Ensure clear value differentiation between free and premium
- Build habit-forming features before paywall

---

### R02: User Abandons During Profile Setup

**Risk**: Less than 40% of users complete profile, crippling personalization value.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Profile completion | <50% | Week 2-3 |
| Red alert | Profile completion | <40% | Week 4+ |

**Immediate Response (Yellow)**:
1. Reduce required fields (try 3 instead of 5)
2. Add progress indicator with time estimate
3. Show immediate value after each field ("Great! Now we know your HVAC filter size")
4. Add "skip for now" option with prompts later
5. Test gamification (completion badge, streak)

**Escalation Response (Red)**:
1. Implement zero-profile fallback experience
2. Use location-based defaults (well water common in your area)
3. Partner with real estate data providers for pre-population
4. Consider label scan as primary entry (vs manual fields)

**Prevention**:
- Test onboarding flow with 10 users before launch
- Benchmark against HomeZada's auto-population feature
- Design for mobile thumb-zone comfort

---

### R03: Content Gaps Frustrate Users

**Risk**: User searches for problem we don't cover, gets no help, churns.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | "No match" rate | >15% | Month 1-2 |
| Red alert | "No match" rate | >25% | Month 2-3 |

**Immediate Response (Yellow)**:
1. Analyze top unmatched queries
2. Prioritize content creation for top 5 gaps
3. Add graceful fallback: "We don't have this yet, but here's general guidance"
4. Link to YouTube videos for unmatched queries
5. Add "request this topic" feature

**Escalation Response (Red)**:
1. Pause new user acquisition until content gaps filled
2. Hire contract content writers to accelerate coverage
3. License content from RepairClinic or iFixit
4. Implement AI-assisted general answers (with disclaimers)

**Prevention**:
- Validate top 25 scenarios cover 80%+ of real queries
- Launch with 40 scenarios instead of 25
- Build query logging from day 1

---

### R04: Bad Advice Causes Damage/Injury

**Risk**: User follows app advice, causes property damage or personal injury.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Complaint received | 1 incident | Any time |
| Red alert | Legal action threatened | Any threat | Any time |

**Immediate Response (Yellow)**:
1. Document incident fully (user account, steps taken, outcome)
2. Review the specific content for accuracy
3. Consult with expert reviewer on content
4. Update content if error found
5. Consider goodwill gesture (refund, apology)

**Escalation Response (Red)**:
1. Engage attorney immediately
2. Preserve all records (user data, app version, content version)
3. Review and strengthen all electrical/gas safety warnings
4. Consider temporary removal of high-risk content
5. Activate insurance policy if applicable

**Prevention**:
- Expert review all content before launch
- Add explicit safety warnings for electrical, gas, water main issues
- Require user acknowledgment before high-risk procedures
- Include "when in doubt, call a pro" guidance
- Carry errors & omissions insurance

---

### R05: Service Provider Network Too Thin

**Risk**: Users click "find a pro" but no providers available in their area.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Provider coverage | <80% of Austin ZIP codes | Launch |
| Red alert | "No provider" rate | >20% of referral requests | Month 2+ |

**Immediate Response (Yellow)**:
1. Focus recruitment on underserved ZIP codes
2. Expand radius for provider matching (20 miles → 30 miles)
3. Show "providers coming soon" instead of empty state
4. Collect user email to notify when provider available

**Escalation Response (Red)**:
1. Partner with Thumbtack/Angi as fallback
2. Shift to directory model (show providers without vetting)
3. Offer "we'll find someone" concierge service
4. Temporarily remove referral feature from affected areas

**Prevention**:
- Seed 15+ providers before launch (5 per major category)
- Start with single metro, don't expand until density achieved
- Offer free leads for first 6 months to build supply

---

### R06: Paid CAC Exceeds LTV

**Risk**: Paid acquisition costs more than users are worth, accelerating cash burn.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Paid CAC | >$6 | Any paid campaign |
| Red alert | Paid CAC | >$8 | Any paid campaign |

**Immediate Response (Yellow)**:
1. Pause lowest-performing channels
2. Narrow targeting (more specific audiences)
3. Test new creative variants
4. Shift budget to higher-converting channels

**Escalation Response (Red)**:
1. Pause all paid acquisition immediately
2. Focus 100% on organic channels
3. Invest in referral program instead
4. Don't resume paid until LTV improves

**Prevention**:
- Don't launch paid acquisition until organic proves model
- Set strict CAC caps in ad platforms
- Start with small budgets, scale only winners

---

### R07: Competitor Launches Similar Feature

**Risk**: Dib, HomeZada, or new entrant launches troubleshooting before we achieve scale.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Competitor announcement | Feature announced | Any time |
| Red alert | Competitor launch | Feature live | Any time |

**Immediate Response (Yellow)**:
1. Assess competitor's approach and quality
2. Accelerate feature development timeline
3. Double down on unique differentiators
4. Increase marketing spend to establish position

**Escalation Response (Red)**:
1. Rapid competitive analysis: what do they do better/worse?
2. Identify and amplify our unique strengths
3. Consider partnership or acquisition discussions
4. Pivot to underserved niche (landlords, specific appliance types)

**Prevention**:
- Move fast: shorter development timeline
- Build community and brand before competitors can
- Establish "first mover" positioning in Austin market

---

### R10: Low D30 Retention

**Risk**: Users try the app but don't return, indicating weak value proposition.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | D30 retention | <8% | Month 2-3 |
| Red alert | D30 retention | <5% | Month 3-4 |

**Immediate Response (Yellow)**:
1. Analyze user behavior: what do retained users do differently?
2. Implement re-engagement push notifications
3. Add weekly maintenance tip emails
4. Create "saved $X" dashboard to reinforce value
5. Test weekly/monthly challenges

**Escalation Response (Red)**:
1. Major product pivot may be needed
2. Interview churned users to understand why
3. Consider switching to higher-frequency use case (daily tips)
4. Explore integration with smart home for passive value

**Prevention**:
- Design for recurring engagement (maintenance schedule, seasonal tips)
- Build notification strategy that provides ongoing value
- Create content calendar to drive return visits

---

### R13: Poor App Store Ratings

**Risk**: Rating falls below 4.0, hurting discoverability and social proof.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | App Store rating | <4.2 | Month 1-2 |
| Red alert | App Store rating | <4.0 | Month 2+ |

**Immediate Response (Yellow)**:
1. Respond to every negative review
2. Analyze review themes: what are common complaints?
3. Prioritize fixing top complaint issues
4. Implement "rate us" prompt for happy users (post-success moment)
5. Reach out to positive reviewers for detailed reviews

**Escalation Response (Red)**:
1. Emergency bug fix release if technical issues
2. Consider "soft relaunch" with major update
3. Incentivize reviews from satisfied users
4. Personal outreach to negative reviewers to resolve issues

**Prevention**:
- Don't prompt for ratings until user has had success
- Thorough QA before launch
- Beta test with harsh critics to find issues early

---

### R15: Funding Runs Out Before PMF

**Risk**: Cash exhausted before achieving product-market fit, forcing shutdown.

| Trigger | Metric | Threshold | Timeframe |
|---------|--------|-----------|-----------|
| Yellow alert | Runway | <6 months | Any time |
| Red alert | Runway | <3 months | Any time |

**Immediate Response (Yellow)**:
1. Cut non-essential expenses immediately
2. Accelerate path to revenue (earlier paywall, higher prices)
3. Begin fundraising conversations
4. Explore revenue alternatives (consulting, contracting)

**Escalation Response (Red)**:
1. Radical cost cutting (pause development, reduce team)
2. Seek bridge funding from angels/friends
3. Explore acquisition conversations
4. Plan for graceful shutdown if necessary

**Prevention**:
- Validate before building (this plan)
- Build with minimal viable scope
- Maintain 20% contingency buffer
- Track burn rate weekly, not monthly

---

## 3. Monitoring Dashboard

### Key Metrics to Track Daily (Week 1-4)

| Metric | Source | Alert Threshold |
|--------|--------|-----------------|
| New installs | App Store Connect | <10/day |
| Profile completion rate | Analytics | <50% |
| Onboarding drop-off step | Analytics | Any step >30% drop |
| Crash rate | Crashlytics | >1% |
| App Store rating | App Store | <4.0 |

### Key Metrics to Track Weekly (Month 1-3)

| Metric | Source | Alert Threshold |
|--------|--------|-----------------|
| D1 retention | Analytics | <20% |
| D7 retention | Analytics | <12% |
| Troubleshooting sessions/user | Analytics | <1.5/week |
| "No match" rate | Analytics | >15% |
| Support tickets | Support inbox | >5/week |

### Key Metrics to Track Monthly (Month 1-12)

| Metric | Source | Alert Threshold |
|--------|--------|-----------------|
| D30 retention | Analytics | <8% |
| Free-to-paid conversion | Analytics | <3% |
| MRR | Stripe/RevenueCat | Off projection by >20% |
| CAC (organic) | Analytics + ad spend | >$3 |
| Provider referral rate | Analytics | <3% of sessions |
| NPS score | Survey | <30 |

### Review Cadence

| Frequency | Meeting | Attendees | Focus |
|-----------|---------|-----------|-------|
| Daily | Standup | Founder | Installs, crashes, urgent issues |
| Weekly | Metrics review | Founder + advisors | Retention, conversion trends |
| Bi-weekly | Risk review | Founder | Risk registry updates |
| Monthly | Board/advisor update | All stakeholders | Overall health, strategic decisions |

---

## 4. Escalation Matrix

### Decision Authority

| Decision Type | Founder Can Decide | Requires Advisor Input | Requires Board/Investor |
|---------------|-------------------|------------------------|-------------------------|
| Feature priority change | ✅ | | |
| Marketing budget reallocation (<$1K) | ✅ | | |
| Marketing budget reallocation (>$1K) | | ✅ | |
| Pricing change | | ✅ | |
| Major pivot | | | ✅ |
| Additional funding request | | | ✅ |
| Shutdown decision | | | ✅ |
| Legal response | | ✅ | |
| Partnership agreement | | ✅ | |

### Communication Templates

**Yellow Alert Email** (to advisors):
> Subject: [YELLOW] {Risk Name} - {Metric} at {Value}
>
> Current status: {metric} is at {value}, below our threshold of {threshold}.
> Immediate actions being taken: {list actions}
> Decision needed: {if any}
> Next update: {date}

**Red Alert Email** (to all stakeholders):
> Subject: [RED ALERT] {Risk Name} - Immediate Attention Required
>
> Situation: {brief description}
> Impact: {what this means for the business}
> Actions taken: {list}
> Actions proposed: {list}
> Decision required by: {date}
> Call scheduled: {date/time}

---

## 5. Post-Mortem Template

When a risk materializes, document learnings:

### Risk Post-Mortem: [Risk Name]

**Date of incident**:
**Severity**: Yellow / Red
**Duration**:

**What happened**:
{Factual description}

**Root cause**:
{Why did this happen?}

**Detection**:
- When was it detected?
- How was it detected?
- Could we have detected it earlier?

**Response**:
- What actions were taken?
- How long did response take?
- What worked? What didn't?

**Impact**:
- Users affected:
- Revenue impact:
- Reputation impact:

**Lessons learned**:
1.
2.
3.

**Action items to prevent recurrence**:
| Action | Owner | Due Date |
|--------|-------|----------|
| | | |

---

*Document 7 of 8 | Next: Legal Checklist →*
