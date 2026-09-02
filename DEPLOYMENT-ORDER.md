# Deployment order

1. Create a hosted PostgreSQL database and run `backend/schema.sql` (enable the `pgcrypto` extension if your provider requires it).
2. Deploy `backend/` to a Node host and set all variables from `backend/.env.example`.
3. Generate an admin bcrypt password hash and a strong JWT secret; never commit them.
4. Copy the backend URL into `cloudflare/config.js` as `window.API_BASE`.
5. Deploy the `cloudflare/` folder as a static site.
6. Set `FRONTEND_ORIGIN` and `VERIFY_REDIRECT` to the final frontend URL, then redeploy/restart the backend.
7. Open `/admin.html`, sign in, and upload the UPI QR image.
8. Test registration → email verification → QR → UTR claim → admin approval → student access.

For a real paid launch, also add a privacy notice, terms/refund policy and a support contact, and confirm that your payment/business setup complies with the applicable provider rules and local requirements.