# High-Ticket Deal Closer API

Minimal NestJS backend for managing leads, deals, proposals and payments. Uses Prisma/PostgreSQL, Firebase for auth and Stripe for payments.

## Setup

```bash
npm install
npx prisma migrate dev --name init
npm run dev
```

See `.env.example` for required environment variables.

## Notes

- Protected routes require a Firebase ID token via `Authorization: Bearer <token>` header.
- Multi-tenancy is simulated through an `X-Account-Id` header.
- Stripe Checkout is used for payments and webhook updates payment status.
