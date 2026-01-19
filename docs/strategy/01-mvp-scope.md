# Refined MVP Scope: Home Maintenance & Troubleshooting App

*Strategic Document 1 of 4 | Last Updated: January 2026*

---

## Executive Summary

This document makes the hard tradeoffs the product requirements avoid: **iOS-first development**, a **10-field minimum viable profile**, and **25 launch troubleshooting scenarios**. These decisions optimize for speed-to-market and learning velocity over feature completeness.

**Key Market Opportunity**: Centriq, a major competitor, shut down in January 2025. Their user base is actively seeking alternatives. This creates a window to capture orphaned users with a focused, well-executed product.

---

## 1. Platform Decision

### Recommendation: iOS-First

Launch on iOS exclusively for the first 6-9 months, then expand to Android after validating product-market fit.

### Rationale

| Factor | iOS | Android | Winner |
|--------|-----|---------|--------|
| **Target demographic alignment** | Homeowners skew higher income; iOS users 48% more likely to earn $125K+ | Broader reach but lower average income | iOS |
| **Willingness to pay** | Higher app store spending ($101/mo avg on tech) | Lower ARPU globally | iOS |
| **Development efficiency** | Single device form factor, predictable OS behavior | Device fragmentation, testing complexity | iOS |
| **Home improvement app presence** | HomeZada, Centriq (defunct) launched iOS-first | Secondary platform for most | iOS |
| **Market share (US)** | 59.4% US market share | 40.6% US | iOS |

### Development Cost Comparison

| Approach | Estimated Cost | Time to MVP |
|----------|---------------|-------------|
| iOS-first (Swift/SwiftUI) | $40K-80K | 3-4 months |
| Android-first (Kotlin) | $45K-90K | 4-5 months |
| Cross-platform (Flutter/React Native) | $50K-100K | 4-6 months |
| Both native simultaneously | $80K-160K | 5-7 months |

**Recommendation**: Native iOS (Swift/SwiftUI) for quality and performance. Cross-platform introduces bugs, slower performance, and platform-specific workarounds that delay launch.

### Android Expansion Criteria

Expand to Android when:
1. iOS reaches 10,000 active users
2. Retention at 30 days exceeds 25%
3. At least one revenue stream is validated (referrals or subscriptions)
4. Core troubleshooting content library reaches 50+ scenarios

### Risk Mitigation

- **Risk**: Missing Android-only users
- **Mitigation**: Build email waitlist for Android users; creates demand signal and launch audience
- **Risk**: Rebuilding for Android later
- **Mitigation**: Design backend API-first; Android app consumes same APIs

---

## 2. Minimum Viable Profile (MVP Profile)

### Core Insight

The app's value depends on context-aware troubleshooting. But requiring extensive profile setup creates abandonment. The MVP Profile defines the **smallest data set that enables meaningful personalization**.

### Required Fields (Must Complete Before First Use)

| Field | Why Required | Collection Method |
|-------|--------------|-------------------|
| 1. Home type | Affects infrastructure assumptions | Single select |
| 2. Approximate year built | Determines pipe materials, wiring standards | Decade picker |
| 3. Water source | Well vs municipal changes diagnostics significantly | Toggle |
| 4. Heating type | Gas vs electric vs heat pump | Single select |
| 5. At least 1 major appliance | Unlocks maintenance scheduling | Manual or scan |

**5 fields = ~90 seconds to complete**

### Enhanced Fields (Prompted After First Value Delivery)

| Field | Unlocks | Prompt Trigger |
|-------|---------|----------------|
| 6. Number of bathrooms | Plumbing-related diagnostics | After first plumbing query |
| 7. Pipe material (copper/PEX/galvanized) | Water quality diagnostics | After water-related query |
| 8. HVAC brand/model | Specific filter sizes, maintenance schedules | After HVAC-related query |
| 9. Water heater age | Anode rod, sediment warnings | After hot water query |
| 10. Electrical panel amperage | Circuit load calculations | After electrical query |

### Progressive Disclosure Strategy

**Onboarding Flow**:
```
Welcome → Home Type → Year Built → Water Source → Heating Type → Add First Appliance → Dashboard
```

**Time to value**: Under 2 minutes from download to personalized dashboard

**Post-onboarding prompts**: After each troubleshooting session, prompt for 1-2 related fields:
- *"You asked about your water heater. Adding its age helps us give better maintenance alerts. Add it now?"*

### Zero-Profile Fallback

If user skips all profile setup, provide generic troubleshooting with clear callouts:
- *"Without knowing your water source, here are general causes of orange water..."*
- *"Adding your home details gives you personalized answers. [Complete Profile]"*

This ensures **no dead ends** while incentivizing profile completion.

---

## 3. Content Scope for Launch

### Launch Troubleshooting Scenarios (25 Total)

Based on frequency of homeowner queries and ability to provide DIY resolution.

#### HVAC (8 scenarios)
| # | Scenario | DIY Potential | Priority |
|---|----------|---------------|----------|
| 1 | AC not cooling | High (filter, thermostat) | Must-have |
| 2 | Heater not heating | High (filter, pilot, thermostat) | Must-have |
| 3 | Strange HVAC noises | Medium (loose parts) | Must-have |
| 4 | HVAC short cycling | Medium (filter, coil) | Must-have |
| 5 | Musty smell from vents | High (mold, filter) | Must-have |
| 6 | Uneven heating/cooling | Medium (vents, ductwork) | Should-have |
| 7 | Thermostat not responding | High (batteries, wiring) | Should-have |
| 8 | High energy bills | Medium (diagnostics checklist) | Should-have |

#### Plumbing (7 scenarios)
| # | Scenario | DIY Potential | Priority |
|---|----------|---------------|----------|
| 9 | Clogged drain | High (plunger, snake) | Must-have |
| 10 | Running toilet | High (flapper, fill valve) | Must-have |
| 11 | Low water pressure | Medium (aerator, valve) | Must-have |
| 12 | Discolored water | Medium (diagnostics) | Must-have |
| 13 | Leaky faucet | High (washer, cartridge) | Should-have |
| 14 | Water heater no hot water | Medium (pilot, element) | Should-have |
| 15 | Garbage disposal jammed | High (reset, hex key) | Should-have |

#### Electrical (5 scenarios)
| # | Scenario | DIY Potential | Priority |
|---|----------|---------------|----------|
| 16 | Outlet not working | High (breaker, GFCI reset) | Must-have |
| 17 | Breaker keeps tripping | Medium (load identification) | Must-have |
| 18 | Flickering lights | Low (diagnostics only) | Should-have |
| 19 | Dead outlet after storm | Medium (surge, GFCI) | Should-have |
| 20 | Smoke detector beeping | High (battery, replacement) | Should-have |

#### Major Appliances (5 scenarios)
| # | Scenario | DIY Potential | Priority |
|---|----------|---------------|----------|
| 21 | Refrigerator not cooling | Medium (coils, thermostat) | Must-have |
| 22 | Dishwasher not draining | High (filter, hose) | Must-have |
| 23 | Washing machine won't spin | Medium (lid switch, belt) | Should-have |
| 24 | Dryer not heating | Medium (lint, element) | Should-have |
| 25 | Oven not heating | Medium (element, igniter) | Should-have |

### Content Structure Per Scenario

Each troubleshooting scenario includes:

```
1. Symptom Description
   - User-friendly description
   - Common variations

2. Quick Checks (30 seconds)
   - Immediate things to verify
   - "Is it plugged in?" equivalents

3. Context-Aware Diagnostics
   - Questions that narrow down cause
   - Profile-informed suggestions

4. Step-by-Step Solutions
   - Numbered instructions with images
   - Skill level indicators (Easy/Moderate/Advanced)
   - Safety warnings (electrical, gas)

5. Parts/Tools Needed
   - Generic descriptions (not affiliate links for v1)
   - Where to find (Home Depot, Lowe's, Amazon)

6. When to Call a Pro
   - Clear escalation triggers
   - What to tell the service provider

7. Prevention Tips
   - Maintenance tasks to avoid recurrence
   - Links to maintenance schedule
```

**Estimated creation time**: 4-6 hours per scenario (research, writing, review)
**Total content investment**: 100-150 hours for 25 scenarios

### Content Sourcing Strategy

| Option | Pros | Cons | Recommendation |
|--------|------|------|----------------|
| In-house creation | Full control, custom to app | Time-intensive | **Primary approach** |
| Licensed content (RepairClinic, iFixit) | Fast, comprehensive | Cost, generic | Evaluate for v2 |
| Expert contributors | Credibility, depth | Coordination overhead | For specialized topics |
| AI-assisted drafting | Speed | Requires expert review | Use for first drafts |

**Recommended approach**: AI-assisted first drafts reviewed and edited by licensed contractor (HVAC tech or master plumber as paid consultant, ~$50-100/hour).

### Appliance Coverage for Launch

Focus on **top 15 appliance categories** by household penetration:

| Category | US Household Penetration | Launch Priority |
|----------|-------------------------|-----------------|
| Refrigerator | 99% | Yes |
| Stove/Oven | 98% | Yes |
| Microwave | 97% | No (rare issues) |
| Washing Machine | 85% | Yes |
| Dryer | 80% | Yes |
| Dishwasher | 75% | Yes |
| Central AC | 75% | Yes |
| Water Heater | 90% | Yes |
| Furnace/Heat Pump | 85% | Yes |
| Garbage Disposal | 50% | Yes |
| Smoke Detectors | 96% | Yes |
| Thermostat | 85% | Yes |

**Brand coverage**: Generic guidance for all; specific model data for top 5 brands per category (based on market share).

---

## 4. Feature Prioritization

### Must-Have for Launch (MVP)

| Feature | Why Critical |
|---------|--------------|
| Home profile creation | Enables personalization |
| Appliance inventory (manual + scan) | Core data asset |
| 25 troubleshooting scenarios | Primary value proposition |
| Maintenance schedule generation | Recurring engagement driver |
| Push notifications for maintenance | Retention mechanism |
| Service provider directory (static list) | Revenue foundation |

### Fast-Follow (30-60 Days Post-Launch)

| Feature | Why Deferred |
|---------|--------------|
| Additional 25 troubleshooting scenarios | Content creation time |
| User feedback on solutions (thumbs up/down) | Learn what's working |
| Maintenance task completion tracking | Engagement data |
| Share home profile (for landlords/tenants) | Complexity |

### Deferred to v2 (6+ Months)

| Feature | Why v2 |
|---------|--------|
| Service provider booking | Two-sided marketplace complexity |
| Parts ordering integration | E-commerce scope |
| Warranty tracking | Nice-to-have, not core |
| Multi-property management | Different user segment |
| Smart home / IoT integration | Hardware dependencies |

---

## 5. Resource & Timeline Estimates

### Development Estimate

| Component | Effort | Notes |
|-----------|--------|-------|
| iOS app (profile, inventory, scheduling) | 6-8 weeks | Core screens and flows |
| Backend API | 4-6 weeks | Can parallel with iOS |
| Troubleshooting engine | 3-4 weeks | Decision tree + content delivery |
| Push notifications | 1-2 weeks | Firebase or APNs |
| Admin panel (content management) | 2-3 weeks | For updating scenarios |
| Testing & polish | 2-3 weeks | Beta feedback integration |
| **Total development** | **12-16 weeks** | With 1-2 developers |

### Content Creation Estimate

| Task | Effort | Notes |
|------|--------|-------|
| 25 troubleshooting scenarios | 100-150 hours | AI-assisted + expert review |
| Appliance database (top 15 categories) | 40-60 hours | Brand/model data |
| Maintenance schedule templates | 20-30 hours | By appliance type |
| **Total content** | **160-240 hours** | ~4-6 weeks at 40 hrs/week |

### Budget Summary (Solo Founder)

| Item | Low Estimate | High Estimate |
|------|--------------|---------------|
| iOS development (contract) | $40,000 | $80,000 |
| Backend development | $15,000 | $30,000 |
| Content creation (expert review) | $5,000 | $10,000 |
| Design (UI/UX) | $5,000 | $15,000 |
| Infrastructure (Year 1) | $2,400 | $6,000 |
| App Store fees | $99 | $99 |
| **Total to MVP** | **$67,500** | **$141,000** |

### Timeline to Launch

| Phase | Duration | Milestone |
|-------|----------|-----------|
| Design & architecture | 2-3 weeks | Figma mockups, API spec |
| Development sprint 1 | 4 weeks | Profile + inventory working |
| Development sprint 2 | 4 weeks | Troubleshooting + scheduling |
| Content creation (parallel) | 6 weeks | 25 scenarios complete |
| Closed beta | 2 weeks | 20-50 testers |
| App Store review | 1-2 weeks | Approval buffer |
| **Total** | **14-18 weeks** | ~3.5-4.5 months |

---

## 6. Key Assumptions to Validate

| Assumption | How to Validate | Risk if Wrong |
|------------|-----------------|---------------|
| Users will complete profile setup | Measure onboarding completion rate; target >60% | Core value prop fails |
| 25 scenarios cover majority of queries | Track "no match found" rate; target <20% | User frustration, churn |
| Context improves troubleshooting quality | A/B test personalized vs generic answers | Differentiation erodes |
| iOS-first doesn't miss key audience | Monitor Android waitlist size | Slower growth |
| Label scanning accuracy sufficient | Test with 100+ appliance photos | Manual entry fallback |

---

## 7. Success Criteria for Launch

| Metric | Target | Rationale |
|--------|--------|-----------|
| Onboarding completion | >60% | Profile is essential |
| Troubleshooting sessions (Month 1) | >3 per user | Validates core utility |
| Day 7 retention | >30% | Industry benchmark |
| Day 30 retention | >15% | Healthy for utility app |
| NPS score | >30 | Willing to recommend |
| "Call a pro" referral clicks | >5% of sessions | Revenue potential signal |

---

## Appendix: Competitive Gap Created by Centriq Shutdown

Centriq's January 2025 shutdown creates immediate opportunity:

**What Centriq Did Well**:
- Appliance cataloging via serial number photos
- Automatic manual lookup
- Recall alerts
- Parts ordering links

**What Centriq Lacked** (our differentiation):
- Context-aware troubleshooting (just stored manuals, didn't diagnose)
- Proactive maintenance scheduling
- Home infrastructure context (water source, pipe type, etc.)
- Service provider connection

**Migration Opportunity**:
- Target Centriq users in marketing (they're actively searching for alternatives)
- Offer "import from Centriq" if data export format is accessible
- Emphasize troubleshooting as key differentiator vs just manual storage

---

*Document 1 of 4 | Next: Business Model →*
