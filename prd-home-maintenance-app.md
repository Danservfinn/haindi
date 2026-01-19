# PRD: Home Maintenance & Troubleshooting App

*Updated with strategic context | January 2026*

---

## Executive Summary

A mobile app that provides **context-aware troubleshooting** for homeowners, using their home's specific details (appliances, infrastructure, utilities) to deliver personalized diagnostic guidance. Unlike generic Google/YouTube results, we know your home and give answers that fit your setup.

**Market Opportunity**: Centriq's January 2025 shutdown left a gap in the home maintenance app market. Existing competitors (HomeZada, Dib) focus on inventory/documentation, not active problem-solving.

**Business Model**: Freemium subscription ($30/year premium) + service provider referrals ($35/lead).

**Launch Strategy**: iOS-first, single metro market (Austin, TX), 25 troubleshooting scenarios at launch.

---

## Problem & Motivation

Homeowners and landlords face a recurring challenge: when something goes wrong with an appliance or home system, they often don't know whether it's a simple fix or requires professional help. This uncertainty leads to:

- **Expensive unnecessary service calls** for issues that could be self-resolved
- **Deferred maintenance** because owners forget or don't know when to service equipment
- **Misdiagnosis** from generic internet searches that don't account for the specific home setup
- **Wasted time** researching appliance specs, filter sizes, and maintenance schedules

**The core insight**: Most troubleshooting advice fails because it's generic. Knowing that a home has copper pipes, well water, and a 15-year-old HVAC system fundamentally changes the diagnostic path.

### Competitive Gap

| Competitor | What They Do | What They Don't Do |
|------------|--------------|-------------------|
| HomeZada | Home inventory, value tracking | No troubleshooting |
| Dib | AI-powered document storage | No diagnostics |
| YouTube | Generic DIY videos | No personalization |
| Centriq (defunct) | Manual storage, recall alerts | No problem-solving |

**Our differentiation**: We're the only app that combines home context with active troubleshooting.

---

## Target Users

### Primary: Individual Homeowners
- First-time homeowners unfamiliar with maintenance responsibilities
- Experienced homeowners who want organized maintenance tracking
- DIY-oriented individuals who prefer self-service before calling professionals

**Acquisition channels**: ASO, content SEO, influencer partnerships, real estate agent closing gifts

### Secondary: Landlords
- Small-scale landlords managing 1-5 rental properties
- Need to track maintenance across multiple units
- Want to empower tenants with self-service troubleshooting for minor issues

**Note**: Multi-property management deferred to v2; serve individual homes well first.

---

## End State Vision

A homeowner opens the app when their bathroom faucet produces orange water. Instead of a generic Google result, the app knows:
- Their home has copper pipes
- They're on well water (not municipal)
- The water heater is 8 years old
- The last water softener service was 6 months ago

With this context, it provides a targeted diagnosis: "Orange water with copper pipes on well water typically indicates sediment buildup or corroding anode rod in your water heater. Given your heater is 8 years old, check the anode rod first. Here's how..."

The app also proactively reminds them: "Your HVAC filter (20x25x1) should be replaced next week based on your 90-day schedule."

---

## Scope

### In Scope (MVP)

#### Home Profile Setup
- Manual entry of home details:
  - Utility configuration (gas, electric, solar, well/municipal water)
  - Room inventory (kitchen, bathrooms, bedrooms, garage, etc.)
  - Infrastructure details (pipe material, shutoff locations)
- Appliance inventory:
  - Brand, model, age
  - Location within home
  - Label scanning for quick data capture
  - Manual entry fallback

#### Minimum Viable Profile (5 Required Fields)

Users must complete before first use:

| Field | Why Required | Collection Method |
|-------|--------------|-------------------|
| Home type | Affects infrastructure assumptions | Single select |
| Approximate year built | Determines pipe materials, wiring standards | Decade picker |
| Water source | Well vs municipal changes diagnostics | Toggle |
| Heating type | Gas vs electric vs heat pump | Single select |
| At least 1 major appliance | Unlocks maintenance scheduling | Manual or scan |

**Time to value**: Under 2 minutes from download to personalized dashboard

#### Maintenance Scheduling
- Auto-generated maintenance schedules based on appliance type and age
- Push notifications for upcoming maintenance
- Maintenance history tracking
- Consumable specifications (filter sizes, bulb types, etc.)

#### Troubleshooting Engine (25 Launch Scenarios)

| Category | Scenarios | Examples |
|----------|-----------|----------|
| HVAC | 8 | AC not cooling, heater not heating, strange noises |
| Plumbing | 7 | Clogged drain, running toilet, discolored water |
| Electrical | 5 | Outlet not working, breaker tripping |
| Appliances | 5 | Refrigerator not cooling, dishwasher not draining |

Each scenario includes: symptom description, quick checks, context-aware diagnostics, step-by-step solutions, safety warnings, and "when to call a pro" triggers.

#### Service Provider Connection
- Partner directory of vetted service providers (10-15 at launch in Austin)
- Category-based search (plumber, electrician, HVAC)
- Basic contact information and service areas
- Referral tracking for partnership revenue

### Out of Scope (v1)

| Feature | Rationale |
|---------|-----------|
| Parts ordering | Adds e-commerce complexity; users can search suggested parts |
| Service booking | Requires deep provider integration; v1 focuses on connection only |
| IoT/smart home integration | Significant technical scope; validate core value first |
| Multi-unit property management | Different UX needs; serve individual homes first |
| Android app | iOS-first to optimize development efficiency; Android in v2 |

---

## Technical Approach

### Platform Strategy: iOS-First

**Decision**: Launch on iOS exclusively, expand to Android after product-market fit.

| Factor | iOS | Android |
|--------|-----|---------|
| Target demographic | Higher income homeowners | Broader but lower ARPU |
| Development efficiency | Single form factor | Device fragmentation |
| Market share (US) | 59.4% | 40.6% |
| Willingness to pay | Higher | Lower |

**Android expansion criteria**:
- 10,000+ iOS MAU
- D30 retention >15%
- At least one revenue stream validated

### Data Architecture
```
Home
├── Profile (utilities, infrastructure)
├── Rooms[]
│   └── Appliances[]
│       ├── Specs (brand, model, age, location)
│       ├── MaintenanceSchedule[]
│       └── MaintenanceHistory[]
└── TroubleshootingHistory[]
```

### Troubleshooting Engine
- Decision tree architecture for symptom → diagnosis → solution paths
- Context injection from home profile at decision points
- Confidence scoring to determine when to recommend professional help
- Content authored by domain experts (licensed contractors, appliance technicians)
- AI-assisted first drafts with expert review (~$50-100/hour consultant)

---

## Business Model

### Revenue Streams

| Stream | Model | Target |
|--------|-------|--------|
| **Premium subscription** | $4.99/month or $29.99/year | 4% conversion |
| **Service provider referrals** | $35 per qualified lead | 4% of troubleshooting sessions |
| **Lifetime purchase** | $99.99 one-time | 10% of paid users |

### Free vs Premium Features

| Feature | Free | Premium |
|---------|------|---------|
| Home profile | ✅ | ✅ |
| Appliances | 3 max | Unlimited |
| Troubleshooting | 5/month | Unlimited |
| Maintenance reminders | Manual | Push notifications |
| Priority support | ❌ | ✅ |

### Unit Economics

| Metric | Value |
|--------|-------|
| Free user LTV | $6.30 |
| Premium user LTV | $138 |
| Blended LTV (4% conversion) | $11.57 |
| Target CAC | $3.86 |
| LTV:CAC target | 3:1 |

### Financial Projections (Base Case)

| Month | MAU | Premium Users | MRR | Total Revenue |
|-------|-----|---------------|-----|---------------|
| 6 | 5,000 | 200 | $1,000 | $2,050 |
| 12 | 15,000 | 600 | $3,000 | $6,150 |
| 24 | 50,000 | 2,000 | $10,000 | $20,500 |

**Break-even**: ~5,000 MAU (Month 6)

---

## Go-to-Market Summary

### Launch Market: Austin, TX

**Why Austin**:
- Tech-savvy population (early adopters)
- High homeownership growth
- Manageable market size for provider network
- Active home improvement culture

### Acquisition Strategy

| Channel | Priority | CAC | Phase |
|---------|----------|-----|-------|
| ASO (organic) | P0 | $0.50-1.50 | Launch |
| Content SEO | P0 | $0.30-1.00 | Launch |
| Referral program | P1 | $2-5 | Month 2 |
| Micro-influencers | P1 | $1-4 | Month 3 |
| Real estate partnerships | P1 | $1-3 | Month 4 |
| Paid acquisition | P3 | $5-10 | Post-PMF |

### Service Provider Strategy

**Phase 1 (Pre-launch)**: Seed 10-15 providers in Austin with free leads
**Phase 2 (Month 6+)**: Transition to paid leads ($35/lead)
**Phase 3 (Month 9+)**: Expand categories beyond HVAC/plumbing/electrical

### Geographic Expansion

| Phase | Markets | Timing |
|-------|---------|--------|
| Launch | Austin, TX | Month 0 |
| Wave 1 | Dallas, Houston | Month 6-9 |
| Wave 2 | Denver, Phoenix | Month 9-12 |
| Wave 3 | National | Month 12+ |

---

## Key Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| Bad advice causes damage/injury | High | Safety disclaimers, conservative recommendations, clear "call a pro" triggers, expert content review |
| User abandons during setup | High | 5-field minimum viable profile, show value with partial data, progressive disclosure |
| Appliance database incomplete | Medium | Focus on top 15 appliance categories; graceful handling of unknown models |
| Low conversion to premium | High | Clear free/paid feature differentiation; paywall at value moments |
| Service provider network too thin | Medium | Start with one metro; validate before expanding |
| Paid CAC unsustainable | Medium | Prioritize organic channels; only scale paid after proving unit economics |

---

## Success Metrics

### North Star Metric
**Problems solved without a service call** - captures user value, product quality, and engagement.

### Phase Targets

| Phase | Metric | Target |
|-------|--------|--------|
| **Month 1-3** | Total installs | 2,500 |
| | Profile completion | >60% |
| | D7 retention | >20% |
| | App Store rating | >4.0 |
| **Month 4-6** | MAU | 5,000 |
| | D30 retention | >10% |
| | Free-to-paid conversion | >3% |
| | Provider referral clicks | >5% of sessions |
| **Month 7-12** | MAU | 15,000 |
| | MRR | $5,000 |
| | LTV:CAC | >3:1 |
| | NPS | >40 |

---

## Open Questions (Resolved)

| Question | Resolution |
|----------|------------|
| ~~Content sourcing~~ | AI-assisted drafts + expert review (~$5-10K investment) |
| ~~Monetization timing~~ | Freemium from launch; premium features clear from start |
| ~~Platform strategy~~ | iOS-first; Android after 10K MAU and PMF signals |
| ~~Regional variations~~ | Start single market (Austin); address regional patterns as we expand |

### Remaining Open Questions

1. **Liability**: What legal disclaimers are needed for DIY advice? Consult attorney for launch.
2. **Appliance age estimation**: If users don't know exact age, can we estimate from model numbers? Research manufacturer date codes.

---

## Dependencies

- **OCR service** for label scanning (Apple Vision recommended for iOS)
- **Push notification infrastructure** (Firebase Cloud Messaging)
- **Service provider partnerships** (10-15 seed providers in Austin)
- **Content creation** (~150 hours for 25 scenarios)
- **Expert review** ($5-10K for licensed contractor consultation)

---

## Budget Summary

| Category | Amount |
|----------|--------|
| Development (iOS + backend) | $55-110K |
| Content creation | $5-10K |
| Design | $5-15K |
| Pre-launch marketing | $15K |
| Year 1 marketing | $25K |
| Infrastructure (Year 1) | $3-6K |
| **Total to launch + Year 1** | **$108-181K** |

---

## Milestones

### M1: Foundation (Weeks 1-6)
- Home profile creation (manual entry)
- Basic appliance inventory
- Minimum viable profile flow
- Simple maintenance scheduling

### M2: Intelligence (Weeks 7-12)
- Label scanning
- Troubleshooting engine (25 scenarios)
- Context-aware diagnostics
- Push notifications

### M3: Connection (Weeks 13-16)
- Service provider directory (Austin)
- Referral tracking
- Premium subscription integration
- User feedback loop

### M4: Launch (Week 17+)
- App Store submission
- Press/PR push
- Public launch

**Total timeline**: ~4-5 months to launch

---

## Related Documents

- [MVP Scope Details](docs/strategy/01-mvp-scope.md)
- [Business Model](docs/strategy/02-business-model.md)
- [Competitive Analysis](docs/strategy/03-competitive-analysis.md)
- [Go-to-Market Strategy](docs/strategy/04-go-to-market.md)

---

*PRD v2.0 | Updated with strategic context from business model, competitive analysis, and GTM planning*
