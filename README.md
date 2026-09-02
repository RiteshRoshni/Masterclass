# ₹99 Online Earning Masterclass

A production-oriented starter for a ₹99 online masterclass with a public landing page, student email verification, UPI QR payment claim, and protected admin dashboard.

## Structure

- `cloudflare/` — static frontend and admin UI for Cloudflare Pages.
- `backend/` — Node.js + Express + PostgreSQL API.
- `DEPLOYMENT-ORDER.md` — deployment checklist.

## Important

Never commit passwords, API keys, Gmail app passwords, JWT secrets, database URLs, or other credentials. Use environment variables on the backend.

The UPI flow is intentionally manual: the student submits a payment claim and an admin verifies it before access is granted. This does not automatically confirm a bank/UPI transaction.
