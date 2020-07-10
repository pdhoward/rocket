# Rocket 
https://rocketdeliveries.io

Testing a simple onboarding, a hosted dashboard, verification, and payouts management with Stripe.

## Web onboarding 

Use [Connect Custom accounts](https://stripe.com/connect/account-types) to get them paid. 

Custom allows you to control every part of the user experience; accounts can be created directly via the Stripe API. 

This demo also uses [Connect Onboarding]((https://stripe.com/docs/connect/connect-onboarding)) to provide onboarding and identity verification for your platform

This platform also uses the Stripe API to create payments for pilots, fetch their available and pending balance, and let them view transfers.

It also creates [Instant Payouts](https://stripe.com/docs/connect/payouts#instant-payouts) for pilots who use a debit card as their payout account.


To integrate Stripe Connect in your own app, check out these two files in particular:
1. [`routes/pilots/stripe.js`](routes/pilots/stripe.js) shows how to easily create Connect Custom accounts and interact with the Stripe API.
2. [`routes/pilots/pilots.js`](routes/pilots/pilots.js) shows how to create payments going straight to pilots.

### Getting started

Install dependencies using npm (or yarn):

    cd server
    npm install

### Use the Stripe CLI to receive webhook events

Relies on webhook events to receive updates from Stripe on a pilot's verification. 