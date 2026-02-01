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
