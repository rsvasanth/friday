# CTO Review Report: System Design Architecture

**To:** System Design Architect  
**From:** CTO, BookPondy.com  
**Date:** February 2, 2026  
**Subject:** Review of System Design & Missing Business Components

## 1. Executive Summary

I have reviewed the `system_design_architecture.md` against the `company_business_brief.md` and `cto_briefing.md`. 
The proposed architecture correctly identifies the **Frappe + ERPNext + React (Doppio/shadcn)** stack as the critical foundation. This alignment saves significant development time and meets our requirement for audit-ready financials.

However, there are specific **business logic gaps** where the "Regenerative" and "Bespoke" nature of our unique business model is not fully captured in the data schema. We need to bridge these gaps to ensure we deliver on our core value propositions of "Radical Transparency" and "Regenerative Impact."

## 2. Gap Analysis & Missing Business Components

### 2.1 Missing "Regenerative Finance" Logic (Critical)
**Business Requirement:** The brief explicitly states that "Every booking funds community development... ₹300-500 [per ₹10k] to Green Belt projects." It also mentions "Radical Transparency" where guests know exactly where their money goes.
**System Design Gap:** 
- The `Itinerary` DocType calculates `subtotal`, `service_fee`, and `gst_amount`, but **omits** the `community_fund_contribution`.
- There is no mechanism described to accrue these funds into a specific Account or Cost Center in ERPNext.
**Recommendation:**
- **Add Field:** `Itinerary.community_fund_amount` (Currency, calculated based on logic).
- **Add Accounting Logic:** Ensure `Sales Invoice` posting credits a "Community Impact Fund" Liability/Equity account, distinct from Revenue.

### 2.2 Incomplete Seasonality & Pricing Rules
**Business Requirement:** "Seasonal rates, but no algorithmic manipulation." "Rack rates updated annually."
**System Design Gap:**
- `Experience` DocType has `price_base` and `price_premium`.
- `Stay Property` has `price_per_night_weekend`.
- **Missing:** A **Pricing Rule Engine**. How does the system know *which* dates are "Premium" for an experience? Or what defines a "Weekend" (Fri-Sat vs Sat-Sun)? Or specific "Peak Season" date ranges (Dec-Jan)? Hardcoding this logic is brittle.
**Recommendation:**
- **New DocType:** `Operation Season` (Start Date, End Date, Type: Peak/Off-Peak).
- **Logic:** `get_experience_price(date)` should check `Operation Season` to apply `price_premium`.

### 2.3 Gap in "Discovery" & Curated Workflow
**Business Requirement:** The flow is "Guest Inquiry -> Discovery Call -> Quotation". This implies a high-touch sales process.
**System Design Gap:**
- The design jumps straight to `Itinerary` (Draft) or `Quotation`.
- It misses the **Inquiry/Discovery Phase**. A `Lead` in ERPNext is generic. We need to capture "Travel Intent", "Vibe Preference" (Quiet vs. Active), and "Group Dynamics" before an Itinerary is even created.
**Recommendation:**
- **New DocType:** `Travel Inquiry` (Extends Lead). Captures structured preferences *before* an Itinerary exists.
- **Workflow:** `Travel Inquiry` -> **Convert** -> `Itinerary`.

### 2.4 Missing Operational Incident Management
**Business Requirement:** "Real-time Support". Mobility partners have "E-bike fleets".
**System Design Gap:**
- `Mobility Asset` exists, but what happens when a bike breaks down mid-tour? Or a guest is unhappy with a Villa cleanliness?
- `Guest Feedback` is post-facto. We need *Real-time* incident logging.
**Recommendation:**
- **New DocType:** `Operations Incident`. Linked to `Booking`, `Asset`, or `Experience Slot`.
- **Fields:** `severity`, `resolution_status`, `refund_issued` (Link to Credit Note).

## 3. Detailed "Missing Components" List

Based on the review, the following components must be added to the scope:

| Component | Type | Priority | Purpose |
|-----------|------|----------|---------|
| **Community Fund Ledger** | Logic/Account | **P0** | Tracks the 3-5% impact fund contribution per transaction. |
| **Pricing Rule Engine** | Logic | **P1** | Determines when `price_premium` applies (Seasons, Holidays). |
| **Travel Inquiry** | DocType | **P1** | Captures "Discovery Call" data before Itinerary creation. |
| **Operations Incident** | DocType | **P2** | Tracks real-time issues (breakdowns, complaints) during execution. |
| **Storyteller Check-in/out** | Feature | **P2** | Explicit mobile workflow for "Start Experience" / "End Experience" to calculating duration accuracy (for payroll). |
| **Waiver Management** | DocType | **P1** | Liability waivers for active experiences (E-bikes, Forest walks). |

## 4. Conclusion & Approval

The architecture is **Approved with Conditions**. 
Please update the System Design to include the **Regenerative Finance** and **Pricing Rule** components immediately, as these affect the core data model. The Incident Management can be slated for Phase 2 if necessary, but the financial transparency model must be built into the MVP.

**Signed,**  
**CTO**
