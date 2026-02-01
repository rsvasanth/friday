# Findings & Research

## Technical Stack
- **Backend**: Frappe Framework (Bench)
- **Frontend**: React (via Doppio)
- **SDK**: Frappe React SDK
- **Styling**: Radix UI / Tailwind CSS

## Constraints
- Production requires "Boot Data" pattern for CSRF.
- Socket.io requires dynamic site name resolution for multi-tenancy.
- Vite proxy must target 127.0.0.1.

## Integration Notes
- **WhatsApp**: Raven integration is the primary candidate for unified messaging.
- **Razorpay**: Standard Frappe/ERPNext Payment Gateway integration.
- **Sustainability**: Will require custom DocTypes for impact logs and API hooks for external auditing syncing.

## Raven Research (The-Commit-Company/raven)
- **Tech Stack**: React, Vite, Tailwind CSS, Lucide Icons.
- **Mobile**: Uses **Capacitor** for hybrid mobile wrapping.
- **Frappe Linkage**: Uses `website_route_rules` and `FrappeUI` core patterns.
- **Architecture**: Separates `frontend/` (React SPA) from `raven/` (Python backend) within the Frappe app structure.
