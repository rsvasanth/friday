# BookPondy.com — Master Implementation Prompt [SENIOR VERSION]
## Digital Transformation: From Collective to Regenerative Ecosystem

### 1. Project Overview & Vision
BookPondy.com is a vertically integrated marketplace for bespoke travel in the Auroville-Puducherry bioregion. It transforms fragmented travel coordination into a seamless, regenerative experience.

**Senior Objective**: Transition from a "Booking Agency" to an **"Interpretive Gateway"** with high emotional retention and operational scalability.

---

### 2. The Technical Stack (Non-Negotiable)
- **Backend**: Frappe Framework (v15+) + ERPNext (v15+).
- **Frontend**: React SPA (via Doppio) + **shadcn/ui** + Tailwind CSS.
- **Database**: MariaDB + Redis.
- **Integrations**: Razorpay (Payments), WhatsApp Cloud API, Channel Manager (iCal/API).

---

### 3. Core Data Model & Custom DocTypes
Extend ERPNext (Accounts, CRM, HR, Assets) with the following:

#### 3.1 Experience & Stay Management
- `Experience`: Catalog with base/premium pricing, linked to ERPNext Items.
- `Experience Slot`: Instances with capacity and Storyteller assignment.
- `Stay Property`: Villa metadata with **Channel Manager ID** and iCal sync.
- `Storyteller Profile`: Extends ERPNext `Employee` with expertise, canonical URLs, and ratings.

#### 3.2 Transactional & Discovery
- `Travel Inquiry`: Discovery phase capturing "Travel Intent" and "Vibe".
- `Itinerary`: Master record linking Stays, Experiences, and Mobility. Calculates **Community Fund**, **Impact Credits**, and **Service Fees**.
- `Operation Season`: Logic for peak/off-peak date multipliers.

#### 3.3 Operations & Support
- `Mobility Dispatch`: Real-time booking for transport assets.
- `Operations Incident`: Real-time logging of issues.
- `Duty of Care Monitor`: Automated "Dead-Man Switch" for Storyteller check-ins.

---

### 4. Senior PM Logic: Regenerative & Scale
- **Communit Fund Ledger**: On Sales Invoice submission, accrue 3-5% of net revenue to a "Community Impact Fund".
- **Impact Credit Governance**: Guests earn credits to *choose* which local project receives their booking's fund.
- **Impact Pulse Reporting**: Automated notifications 30/90 days post-trip showing progress of funded projects.
- **Channel Manager Bridge**: Implement robust sync to prevent overbooking across OTA platforms.

---

### 5. Advanced UX & UI (shadcn/ui Focus)
- **Aesthetic**: Premium, terracotta (#C2410C) and deep teal (#0D9488).
- **Storyteller's Journal**: Post-trip digital mementos interface.
- **Concierge-Now**: Real-time support trigger in PWA.
- **Programmatic Landing Pages**: SEO-optimized pages for every Storyteller and Experience Category.

---

### 6. Implementation Priorities

| Phase | Focus | Key Deliverables |
|-------|-------|------------------|
| **Phase 1: MVP** | Revenue & Safety | Experience Catalog, Razorpay, **Duty of Care Monitor**, Impact Visualization. |
| **Phase 2: Growth**| Retention & Scale | Itinerary Builder, **Impact Credit Governance**, **Channel Manager Bridge**, SEO Engine. |
| **Phase 3: Scale** | Optimization | AI Recommendation, **Impact Pulse Reporting**, Partner PWA, Multi-language. |

---

### 7. Governance & Compliance
- **Vendor KYB**: Automated onboarding with document verification.
- **GDPR Compliance**: Data portability and "Right to be Forgotten" for international guests.
- **Revenue Attribution**: Tracking LTV and Social ROI per Storyteller.

---

**Authorized by the Founder, CTO & Senior PM, February 2026**
