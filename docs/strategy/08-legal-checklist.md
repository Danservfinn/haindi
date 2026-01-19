# Legal Checklist & Resolution Path

*Strategic Document 8 of 8 | Last Updated: January 2026*

---

## Executive Summary

This document identifies all legal questions requiring resolution before development and provides a framework for attorney consultation. **Do not launch without addressing liability, Terms of Service, and Privacy Policy**.

**Estimated legal budget**: $3,000-5,000
**Timeline**: 2-4 weeks for initial consultation and document drafting

---

## 1. Liability for DIY Advice

### The Core Question

**If a user follows our troubleshooting advice and causes property damage or personal injury, what is our liability exposure?**

### Risk Scenarios

| Scenario | Potential Harm | Liability Concern |
|----------|---------------|-------------------|
| User follows electrical advice, gets shocked | Personal injury | Negligence claim |
| User follows plumbing advice, causes flood | Property damage | Negligence, consequential damages |
| User follows gas appliance advice, causes fire | Personal injury, property damage | Gross negligence, failure to warn |
| User delays calling pro based on our advice, problem worsens | Increased repair cost | Negligent misrepresentation |
| User follows advice, voidsappliance warranty | Financial loss | Misrepresentation |

### Comparable Services Analysis

| Service | Content Type | Disclaimers Used |
|---------|--------------|------------------|
| **YouTube DIY videos** | User-generated | Varies; most have general disclaimers |
| **This Old House** | Professional editorial | General disclaimer, "consult professional" |
| **RepairClinic** | Commercial parts seller | "For informational purposes only" |
| **WikiHow** | User-generated | Extensive disclaimers, "not professional advice" |
| **Home Depot guides** | Retailer content | "Results may vary," product liability disclaimers |

### Questions for Attorney

1. What standard of care applies to DIY advice apps? Is it different from publishing?
2. Can we limit liability through Terms of Service disclaimers?
3. What specific warnings are legally required for:
   - Electrical work (shock, fire hazard)
   - Gas appliance work (carbon monoxide, explosion)
   - Plumbing work (water damage, mold)
4. Should we require user acknowledgment before high-risk content?
5. Does personalized advice (vs generic) increase our liability exposure?
6. What insurance should we carry (E&O, general liability)?

### Recommended Disclaimer Framework

**General Disclaimer** (visible at all times):
> Information provided by [App Name] is for educational purposes only and does not constitute professional advice. Always consult a licensed professional for electrical, gas, plumbing, or structural work. [App Name] is not liable for any damage or injury resulting from use of this information.

**High-Risk Content Warning** (before electrical/gas content):
> ⚠️ **Safety Warning**: This procedure involves [electrical/gas/water] systems that can cause serious injury or property damage if performed incorrectly. If you are not comfortable with any step, stop and contact a licensed professional. Proceeding is at your own risk.

**User Acknowledgment** (before accessing high-risk guides):
> [ ] I understand this information is for educational purposes only
> [ ] I accept responsibility for any outcomes from following these steps
> [ ] I will stop and contact a professional if I am uncertain at any point
>
> [Continue] [Cancel]

---

## 2. Terms of Service Requirements

### Key Clauses Needed

| Clause | Purpose | Priority |
|--------|---------|----------|
| **Limitation of liability** | Cap damages, exclude consequential damages | Critical |
| **Disclaimer of warranties** | No guarantee of accuracy or suitability | Critical |
| **Assumption of risk** | User accepts risk of DIY activities | Critical |
| **Arbitration clause** | Require disputes go to arbitration | High |
| **Class action waiver** | Prevent class action lawsuits | High |
| **Indemnification** | User indemnifies us for third-party claims | High |
| **Modification rights** | Right to change content without notice | Medium |
| **Account termination** | Right to terminate for any reason | Medium |
| **Intellectual property** | Ownership of content, user-generated content | Medium |
| **Geographic limitations** | US-only service initially | Medium |

### User Flow for ToS Acceptance

```
Download → First Launch → ToS Screen → Scroll to Bottom → Check "I Agree" → [Accept]
```

**Requirement**: User must affirmatively accept (not pre-checked box)

### Questions for Attorney

1. Are limitation of liability clauses enforceable for physical harm in [state]?
2. Is arbitration clause enforceable for consumer apps under current law?
3. Are there specific state laws (CA, TX) that affect our ToS?
4. How do we handle ToS updates for existing users?
5. Do we need separate Terms for service providers?

---

## 3. Privacy Policy Requirements

### Data We Collect

| Data Type | Collection Method | Purpose | Sensitivity |
|-----------|-------------------|---------|-------------|
| Email address | Registration | Account, marketing | Low |
| Home address | Profile setup | Service provider matching | Medium |
| Home characteristics | Profile setup | Personalization | Medium |
| Appliance inventory | User input, label scan | Troubleshooting, maintenance | Low |
| Usage data | Analytics | Product improvement | Low |
| Device identifiers | Automatic | Analytics, fraud prevention | Low |
| Location (approximate) | IP address | Service provider matching | Medium |
| Payment information | Stripe | Subscription billing | High (processed by Stripe) |

### Regulatory Requirements

| Regulation | Applies? | Requirements |
|------------|----------|--------------|
| **CCPA (California)** | Yes (if CA users) | Right to know, delete, opt-out of sale |
| **CPRA (California)** | Yes | Enhanced CCPA + sensitive data rules |
| **VCDPA (Virginia)** | Yes (if VA users) | Right to access, correct, delete |
| **CPA (Colorado)** | Yes (if CO users) | Similar to VCDPA |
| **CTDPA (Connecticut)** | Yes (if CT users) | Similar to VCDPA |
| **GDPR** | No (US only initially) | Not applicable unless EU users |

### Privacy Policy Sections Needed

1. **Information We Collect**
   - Categories of personal information
   - How we collect it (directly, automatically, third parties)

2. **How We Use Information**
   - Provide service
   - Improve product
   - Marketing (with opt-out)
   - Legal compliance

3. **How We Share Information**
   - Service providers (cloud hosting, analytics)
   - Business partners (service providers in referral network)
   - Legal requirements
   - Business transfers

4. **Your Rights**
   - Access your data
   - Correct your data
   - Delete your data
   - Opt-out of marketing
   - Do Not Sell (CCPA)

5. **Data Retention**
   - How long we keep data
   - Deletion upon request

6. **Security**
   - How we protect data
   - No guarantee of security

7. **Children's Privacy**
   - Not intended for under 18
   - COPPA compliance statement

8. **Changes to Policy**
   - How we notify of changes

### Questions for Attorney

1. Do we need a separate privacy policy for service providers?
2. What are our obligations if there's a data breach?
3. How do we handle data deletion requests for home profile data?
4. Does collecting home address require additional disclosures?
5. Are there specific requirements for storing appliance/serial number data?

---

## 4. Service Provider Agreements

### Agreement Type Needed

**Referral Partner Agreement** covering:

| Element | Description |
|---------|-------------|
| **Lead delivery** | How leads are sent (email, SMS, app) |
| **Lead fees** | $35/qualified lead, payment terms |
| **Lead definition** | What constitutes a "qualified lead" |
| **Quality standards** | Provider must be licensed, insured |
| **Dispute resolution** | Process for bad leads, refunds |
| **Exclusivity** | Non-exclusive; we can have multiple providers per area |
| **Termination** | Either party can terminate with notice |
| **Indemnification** | Provider indemnifies us for their work |
| **Non-solicitation** | Provider can't poach users directly |

### Provider Requirements

| Requirement | Verification Method |
|-------------|-------------------|
| Licensed (where required) | License number verification |
| Insured (general liability) | Certificate of insurance |
| Background check passed | Third-party service (future) |
| Good standing (no complaints) | BBB, state board check |

### Questions for Attorney

1. Is our referral fee structure considered a "kickback" in any state?
2. Do we have any liability for provider work quality?
3. What happens if a provider we refer causes damage?
4. Do we need different agreements for different service categories?
5. Are there state-specific contractor referral regulations?

---

## 5. Intellectual Property

### Our IP Assets

| Asset | Protection Method | Status |
|-------|-------------------|--------|
| App name/brand | Trademark | Need to file |
| Troubleshooting content | Copyright | Auto-protected at creation |
| App code | Copyright | Auto-protected at creation |
| User interface design | Trade dress, copyright | Document creation dates |
| Logo/visual assets | Trademark, copyright | Need to create and file |

### Third-Party IP Concerns

| Concern | Risk | Mitigation |
|---------|------|------------|
| Appliance manufacturer data | Using brand names, model numbers | Fair use for factual info |
| Repair guides based on manufacturer manuals | Potential copyright issue | Create original content |
| Photos of appliances | May include copyrighted elements | Use user photos or licensed stock |
| YouTube video embeds | YouTube ToS allows embedding | Properly embed, don't download |

### Trademark Search Needed

Before finalizing app name:
1. USPTO search for similar marks in class 9 (software) and class 42 (SaaS)
2. App Store search for similar app names
3. Domain availability check
4. Social media handle availability

### Questions for Attorney

1. Should we file a trademark application before launch?
2. Do we need permission to list appliance brands in our database?
3. How do we protect our troubleshooting content from copying?
4. What are the risks of using manufacturer repair information as a basis for our guides?

---

## 6. Insurance Requirements

### Recommended Coverage

| Type | Coverage | Estimated Cost |
|------|----------|---------------|
| **General Liability** | $1M per occurrence / $2M aggregate | $500-800/year |
| **Errors & Omissions (E&O)** | $1M | $1,000-2,000/year |
| **Cyber Liability** | $1M | $500-1,000/year |
| **Directors & Officers** | $1M (if incorporated) | $500-1,000/year |

### E&O Coverage Specifics

For a DIY advice app, E&O should cover:
- Claims arising from advice given
- Defense costs
- Settlements

**Important**: Review policy exclusions carefully. Some E&O policies exclude bodily injury claims.

### Questions for Insurance Broker

1. Does E&O cover bodily injury claims from following our advice?
2. Should we have a specific "content liability" rider?
3. What's the claims process if a user sues?
4. Do we need higher coverage limits given the nature of our content?

---

## 7. Action Items & Timeline

### Pre-Development (Weeks 1-2)

| Item | Action | Owner | Due |
|------|--------|-------|-----|
| Attorney selection | Research and select startup/tech attorney | Founder | Week 1 |
| Initial consultation | 1-hour call covering all topics | Founder + Attorney | Week 2 |
| Insurance quotes | Get quotes for GL, E&O, Cyber | Founder | Week 2 |

### During Development (Weeks 3-6)

| Item | Action | Owner | Due |
|------|--------|-------|-----|
| ToS drafting | Attorney drafts Terms of Service | Attorney | Week 4 |
| Privacy Policy drafting | Attorney drafts Privacy Policy | Attorney | Week 4 |
| Disclaimer language | Attorney reviews/approves disclaimers | Attorney | Week 4 |
| Provider agreement | Attorney drafts referral agreement | Attorney | Week 5 |
| Trademark search | Attorney conducts clearance search | Attorney | Week 5 |

### Pre-Launch (Weeks 7-8)

| Item | Action | Owner | Due |
|------|--------|-------|-----|
| Legal review | Attorney reviews final app for compliance | Attorney | Week 7 |
| Insurance binding | Bind coverage before launch | Founder | Week 7 |
| Document finalization | Final ToS, Privacy Policy, agreements | Attorney | Week 8 |
| Implementation | Add legal documents to app/website | Engineering | Week 8 |

---

## 8. Attorney Consultation Prep

### Questions Organized by Topic

**Liability (20 min)**
1. What's our liability exposure for DIY advice that causes harm?
2. How do we effectively limit liability through disclaimers?
3. What warnings are legally required for high-risk content?
4. Does personalized advice (based on home profile) increase exposure?
5. What insurance do you recommend for this type of app?

**Terms of Service (15 min)**
1. What are the most important protective clauses for our situation?
2. Is arbitration/class action waiver enforceable in our target states?
3. How do we handle ToS updates for existing users?
4. Are there consumer protection laws that limit our ToS provisions?

**Privacy (15 min)**
1. What are our CCPA/state privacy law obligations?
2. Any special requirements for home address and appliance data?
3. What's our breach notification obligation?
4. Do we need a separate policy for service providers?

**Provider Relationships (10 min)**
1. Any regulatory issues with contractor referral fees?
2. What happens if a referred provider causes harm?
3. Do we need provider agreements in place before we start referring?

**IP & Business (10 min)**
1. Should we file a trademark before launch?
2. Any concerns with using appliance brand names?
3. Recommended entity structure (LLC vs C-Corp)?

---

## 9. Budget Estimate

### Legal Costs

| Item | Estimated Cost |
|------|---------------|
| Attorney consultation (2-3 hours) | $600-900 |
| Terms of Service draft | $800-1,200 |
| Privacy Policy draft | $600-800 |
| Service Provider Agreement draft | $500-800 |
| Trademark search | $300-500 |
| Document review/revisions | $400-600 |
| **Total Legal** | **$3,200-4,800** |

### Insurance Costs (Annual)

| Coverage | Estimated Cost |
|----------|---------------|
| General Liability | $500-800 |
| Errors & Omissions | $1,000-2,000 |
| Cyber Liability | $500-1,000 |
| **Total Insurance** | **$2,000-3,800** |

### First Year Total: $5,200-8,600

---

## 10. Legal Document Checklist

### Required Before Launch

- [ ] Terms of Service (drafted and reviewed)
- [ ] Privacy Policy (drafted and reviewed)
- [ ] Disclaimer language (approved by attorney)
- [ ] Cookie policy (if using cookies)
- [ ] In-app acknowledgment flow (implemented)
- [ ] General liability insurance (bound)
- [ ] E&O insurance (bound)

### Required Before Provider Onboarding

- [ ] Service Provider Agreement (drafted)
- [ ] Provider verification process (documented)
- [ ] Lead dispute process (documented)

### Recommended Before Launch

- [ ] Trademark search complete
- [ ] Trademark application filed
- [ ] Domain and social handles secured
- [ ] Cyber liability insurance (bound)

### Can Be Deferred

- [ ] Full trademark registration (can file after launch)
- [ ] D&O insurance (needed if raising funding)
- [ ] Employment agreements (needed if hiring)

---

## Appendix: Sample Disclaimer Language

### General App Disclaimer

> **DISCLAIMER**: The information provided by [App Name] is for general educational and informational purposes only. It is not intended to be a substitute for professional advice from a licensed contractor, electrician, plumber, HVAC technician, or other qualified professional.
>
> [App Name] makes no representations or warranties of any kind, express or implied, about the completeness, accuracy, reliability, suitability, or availability of the information contained in this app for any purpose. Any reliance you place on such information is strictly at your own risk.
>
> In no event will [App Name] be liable for any loss or damage including without limitation, indirect or consequential loss or damage, or any loss or damage whatsoever arising from loss of data or profits arising out of, or in connection with, the use of this app.

### Pre-Electrical Content Warning

> ⚠️ **ELECTRICAL SAFETY WARNING**
>
> Working with electrical systems can result in serious injury or death from electric shock. Before proceeding:
>
> - Turn off power at the circuit breaker
> - Use a voltage tester to confirm power is off
> - If you are uncertain about any step, STOP and contact a licensed electrician
>
> By continuing, you acknowledge that you understand the risks and accept full responsibility for your actions.
>
> [ ] I understand and accept the risks
>
> [Continue] [Find an Electrician Instead]

### Pre-Gas Appliance Warning

> ⚠️ **GAS SAFETY WARNING**
>
> Working with gas appliances can result in fire, explosion, or carbon monoxide poisoning. Before proceeding:
>
> - Know where your gas shutoff valve is located
> - If you smell gas, leave immediately and call your gas company
> - Never use open flames to check for gas leaks
>
> Gas work often requires permits and licensed professionals. When in doubt, call a licensed professional.
>
> [ ] I understand and accept the risks
>
> [Continue] [Find a Professional Instead]

---

*Document 8 of 8 | Strategy Suite Complete*

---

## Related Documents

- [Financial Scenarios](05-financial-scenarios.md)
- [Validation Plan](06-validation-plan.md)
- [Risk Mitigation Playbook](07-risk-mitigation.md)
