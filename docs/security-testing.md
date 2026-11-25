# ParcelBridge v3 security testing

## Verified database checks — 2026-11-25
A transactional SQL test used fictional auth users, organizations, memberships and a shipment, then switched to the authenticated database role with simulated JWT subject claims. All assertions passed and the transaction was rolled back.

- Unrelated recipient cannot read the shipment.
- Assigned recipient can read and submit a request.
- Recipient cannot approve a request.
- Unassigned courier cannot approve a request.
- Assigned verified courier can approve; decision timestamp and actor are recorded.
- Finalized decision cannot be changed by courier.

## Release gates still open
Real email signup and confirmation, password recovery, session expiry, browser/mobile tests, retailer and pending-business isolation, anonymous access tests, administrator onboarding, privacy and retention review, German translation, dependency review, and deployment approval. SQL role simulation is not an end-to-end authentication test. No real carrier integration. Do not use customer data.
