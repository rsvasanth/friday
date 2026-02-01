# BookPondi.com PRD: The Comprehensive Concierge

## 1. Vision & Mission
BookPondi.com is the digital evolution of the Payanam Collective, serving as an "interpretive gateway" to the Auroville-Puducherry bioregion. It synchronizes **Bespoke Itineraries**, **Premium Stays**, and **Integrated Mobility** under a model of **Regenerative Tourism**.

## 2. Core Pillars (The Three-Dimensional Marketplace)
The system must manage three primary verticals with high customizability:

### A. The Experience Engine (Bespoke Itineraries)
- Modular itinerary builder where guests design a "narrative" rather than just booking a tour.
- Categories: Urban Heritage, Auroville Immersion, Workshop Ecosystem (14+ categories), Ancient Landscapes.
- Role: Integration of disparate elements into a singular journey.

### B. The Stay Collection (Premium Curated Stays)
- Curated portfolio of villas/heritage properties vetted for ethical/architectural integrity.
- Focus: Story-driven properties (Franco-Tamil bungalows, eco-luxury forest villas).

### C. Integrated Mobility Solutions
- Dedicated mobility layer (E-bike fleets, low-emission vehicles).
- Purpose: Stress-free transitions between villas, workshops, and heritage sites.

## 3. Ethical & Regenerative Framework
- **Primary Success Metric**: Regenerative impact. Restoration of the bioregion and social equity.
- **Human Unity**: Empowerment of local storytellers and regional youth.
- **Economic Model**: Direct revenue circulation within the local community.
- **Environmental Stewardship**: Prioritizing e-mobility and sustainable management.

## 4. Delivery Strategy (Multi-App & PWA)
Inspired by the **Raven** architecture, BookPondy will use a multi-tenant, multi-app approach:
- **Admin App**: Integrated into Frappe Desk (standard ERPNext/Frappe) for backend management.
- **Partner/Storyteller SPA**: Mobile-optimized React SPA (via Doppio) for storytellers. Delivered as a **PWA** (Progressive Web App) for high-end mobile experience without the friction of app stores.
- **Guest SPA**: High-end, bespoke itinerary viewer React SPA. Designed for "Aesthetic WOW" and radical transparency.
- **Mobile-First**: Optimization for mobile touch-points using **Capacitor** (as used in Raven) if native device features (camera/gps) become critical.

## 5. Key Success Metrics (KPIs)
1. **Community Economic Benefit**: Direct revenue paid to storytellers and local units.
2. **Ecological Restoration Contribution**: Audited funds contributed to regional restoration.
3. **Customization Depth**: Complexity and "narrative quality" of bespoke itineraries.
4. **Guest Consciousness Shift**: (Qualitative) feedback on educational and pedagogical value.

## 5. Technical Focus Areas
- **Dynamic Itinerary Logic**: Handling dependencies between stays, mobility, and time-bound experiences.
- **Auditing & Transparency**: Tracking revenue distribution for ethical reporting.
- **Premium UX**: Reflecting the "High-end, digital-first" hospitality model.

## 6. External Integrations
- **Payments**: Razorpay (via ERPNext integration).
- **Geolocation**: Google Maps API (for vehicle tracking and property locating).
- **Communication**: WhatsApp (likely via Raven integration) for guest/storyteller coordination.
- **Sustainability**: External Sustainability Auditing platform (integrated for "Restoration Fund" tracking).
- **Booking Channels**: Channel Manager integration for synchronizing inventory with Travel Agents.

## 7. Data Strategy & Source of Truth
- **Primary Source of Truth**: Frappe / ERPNext. All inventory, customer profiles, booking logs, and financial records reside here.
## 8. Behavioral Rules
- **Booking Lifecycle**: Itineraries remain modifiable after deposit, subject to **Operations Team Approval**. A manual toggle or approval status is required for post-deposit changes.
- **Storyteller Verification**: Physical presence (GPS) verification is **not** required for the initial release.
- **Impact Transparency**: Restoration Fund contributions are **not** visible to guests in real-time. This will be managed as a backend audited field for now.
- **Schema First**: Any DocType change must be updated in `gemini.md` before execution.
