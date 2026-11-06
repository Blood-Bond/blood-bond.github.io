# Blood Bond — Blood Donor Platform

A starter website for the Blood Bond initiative, beginning in Bogura, Bangladesh. The interface is bilingual (Bangla + English).

## Included
- Home page
- Donor registration form
- Urgent blood request form
- Search for approved, public-consent donors
- Supabase database schema with Row Level Security enabled

## Important before launch
This is an early MVP starter, not a production-ready medical or emergency service. New donor and request entries are `pending`. Review and approve records manually in Supabase Table Editor. Do not expose the Supabase `service_role` key. Only use the public anon key in the browser.

Donor phone/WhatsApp details should only be shown for donors who explicitly consent and have been approved. A website listing does not guarantee donor availability, blood compatibility, or medical eligibility. A hospital/clinician must perform appropriate screening and compatibility checks.

Before public launch, add authenticated admin tools, CAPTCHA/rate limiting, privacy policy and consent wording, backups, security review, and legal review. The starter does not send automated SMS/WhatsApp notifications.

## Setup (computer recommended)
1. Install Node.js (LTS).
2. Extract this ZIP.
3. In the project folder, run `npm install`.
4. Copy `.env.example` to `.env.local`.
5. In Supabase, open SQL Editor and run `supabase/schema.sql`.
6. Add your Supabase Project URL and anon/public key to `.env.local`.
7. Run `npm run dev` and open `http://localhost:3000`.

Environment variables:
- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`

Never put a `service_role` key in frontend code or in `.env.local` variables beginning with `NEXT_PUBLIC_`.
