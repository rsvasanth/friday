# BookPondy.com — Core Features & Functions Checklist

This document provides a consolidated list of the **Functional** and **Technical** features for the BookPondy enterprise application.

---

## 1. Functional Features (User-Centric)

### 1.1 Guest-Facing (Discovery & Booking)
- [ ] **Bespoke Itinerary Builder**: Modular journey designer allowing guests to mix and match experiences, stays, and transport.
- [ ] **Experience Catalog**: Searchable/filterable digital storefront for guided tours, workshops, and cultural immersions.
- [ ] **Stay Collection**: Curated villa and heritage property listings with real-time availability.
- [ ] **Dynamic Pricing**: Automatic application of seasonal multipliers and weekend rates.
- [ ] **Digital Checkout**: Secure payment processing with transparent GST and community fund breakdowns.
- [ ] **Guest Portal (PWA)**: Mobile-optimized dashboard for managing vouchers, viewing itineraries, and chat.
- [ ] **Digital Waivers**: In-app signing of liability waivers for high-risk activities (e-bikes, etc.).

### 1.2 Partner & Storyteller Management
- [ ] **Earnings Tracker**: Transparent display of commissions and session-based payouts.
- [ ] **Vendor KYB Onboarding**: Automated onboarding flow for partners (Document uploads, verification).

### 1.3 B2B & Travel Agents
- [ ] **Agent Booking Portal**: Specialized interface for travel agents to book journeys for their clients.
- [ ] **Commission Automation**: Real-time calculation and tracking of 3rd-party agent commissions.
- [ ] **B2B Quotation Workflow**: Logic for handling bulk or white-label inquiries.

### 1.4 Operations & Admin
- [ ] **Central Dispatch**: Command center for managing e-bike/vehicle mobility fleet assignments.
- [ ] **Concierge Dashboard**: Unified view for managing leads, itineraries, and real-time guest requests.
- [ ] **Incident Management**: Real-time logging and resolution tracking for breakdowns or complaints. (P2)
- [ ] **Emergency 'Concierge-Now'**: Safety/support trigger in the PWA for real-time assistance. (P0)
- [ ] **Dead-Man Switch Protocol**: Automated Duty of Care monitoring (Storyteller check-in alerts). (P0)

### 1.5 Regenerative Experience (PM Driven)
- [ ] **Impact Visualization**: Dynamic display of specific social/ecological impact per booking (e.g., "This booking funds 2 saplings in the Green Belt").
- [ ] **Sustainability Scorecard**: Real-time "Regenerativity Score" displayed in the Itinerary Builder based on choices.
- [ ] **Storyteller's Journal**: Post-experience digital mementos (photos, notes, resources) uploaded by the guide to the guest portal.
- [ ] **Interactive Bioregion Map**: Proximity-aware discovery tool to optimize travel routes and reduce carbon footprint.
- [ ] **Narrative Gift Boxes**: Themed gift vouchers (e.g., "The Sacred Geographer") with digital storytelling for recipients.
- [ ] **Impact Credit Governance**: Guest-led fund allocation (spend impact credits on specific local projects).
- [ ] **Impact Pulse Reporting**: Automated post-trip updates on the actual progress of funded projects.

---

## 2. Technical Features (System-Centric)

### 2.1 Backend & Architecture
- [ ] **Frappe/ERPNext Integration**: Deep linkage to Accounts, CRM, HR, Assets, and Payroll modules.
- [ ] **Regenerative Ledger**: Automated GL entries for the Community Impact Fund (3-5% accrual).
- [ ] **Permissions Matrix**: Enterprise-grade RBAC across all 15+ custom DocTypes.
- [ ] **State Machine Workflows**: Defined transitions for Bookings (Draft -> Confirmed) and Assignments.

### 2.2 Integrations
- [ ] **Razorpay (Payments)**: Webhook-driven payment reconciliation and automated Sales Invoice generation.
- [ ] **WhatsApp Cloud API**: Automated confirmations, reminders, and check-in alerts to guests.
- [ ] **Google Calendar Sync**: Two-way availability synchronization for villas and host calendars.
- [ ] **Channel Manager API**: Integration with professional inventory networks (Staah, Cloudbeds). (P1)
- [ ] **PDF Generation**: Auto-generation of branded itineraries, GST invoices, and vouchers.

### 2.3 Operations & Maintenance
- [ ] **Fleet Status Tracking**: Real-time status management (Parking, In Use, Maintenance) for assets.
- [ ] **Audit Logs**: Comprehensive tracking of all changes to bookings and financial records.
- [ ] **Scalable REST API**: Standardized JSON endpoints for Guest, Partner, and Agent frontends.
- [ ] **Programmatic SEO Engine**: Schema-optimized landing pages for Storytellers and Categories. (P1)

---

## 3. Implementation Priorities

| Feature | Category | Priority | Phase |
|---------|----------|----------|-------|
| Itinerary Engine | Functional | P0 | MVP |
| Community Fund Logic| Technical | P0 | MVP |
| Impact Visualization | Functional | P0 | MVP |
| Concierge-Now / Duty of Care| Functional | P0 | MVP |
| Storyteller Workflow| Functional | P1 | Phase 2 |
| Agent Portal | Functional | P1 | Phase 2 |
| Channel Manager Bridge| Technical | P1 | Phase 2 |
| Impact Governance | Functional | P1 | Phase 2 |
| Programmatic SEO | Technical | P1 | Phase 2 |
| Incident Management | Technical | P2 | Phase 2 |
