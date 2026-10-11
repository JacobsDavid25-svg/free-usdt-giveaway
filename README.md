# Free USDT Giveaway — Starter Demo

This is a beginner-friendly starter project for a Telegram Mini App-style rewards dashboard.

## Important limitations

- **DEMO ONLY.** No real USDT is held, earned, or transferred.
- Demo balances, check-ins, and wallet addresses are stored in server memory and reset when the server restarts.
- The `X-Demo-User` header is only a local demo identity. It is not secure authentication.
- Referral rewards are deliberately not implemented.
- A wallet address entered here is not verified for ownership.
- Do not advertise a guaranteed payout or collect deposits from users.

## Run locally

Requires Node.js 18 or newer.

```bash
npm install
npm start
```

Open `http://localhost:3000`.

## Deploying

Deploy this Node.js project to a hosting service that supports Node apps. Set the start command to `npm start`. The service must support Express and expose its assigned `PORT`.

## Before a public launch

A developer must implement and test all of the following:

1. Verify Telegram Web App `initData` on the server using Telegram's documented HMAC validation. Never trust a user ID sent by the browser.
2. Use a persistent database and transactional updates for claims, tasks, referrals, and balances.
3. Add rate limits, audit logs, duplicate-account controls, and abuse review.
4. Verify channel membership and referral task completion server-side where possible.
5. Define transparent reward terms and anti-fraud rules.
6. Obtain affiliate-program approval before displaying affiliate links.
7. Do not enable withdrawals until funding, payout operations, security review, and applicable legal requirements are addressed.
8. Keep bot tokens and secrets in the hosting provider's server-side environment variables, never in frontend JavaScript or a public repository.

Telegram Mini Apps documentation: https://core.telegram.org/bots/webapps
