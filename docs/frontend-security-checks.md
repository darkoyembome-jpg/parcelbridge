# Frontend security verification

2026-11-26 — inspected index.html blob 71ac878509f794d20754f289595718ac0f5e0ebe and app.js blob a77584cd091e5a9239f78b179ca6ba17693d3d5a.

Eight static checks passed: external module linkage, no inline script, restrictive script-src, no inline event attributes, no common HTML injection sinks, pinned Supabase import, no detected privileged key markers, and presence of statically referenced DOM IDs.

These are source checks, not runtime or penetration tests. CDN integrity and dependency vulnerabilities have not been verified. Browser CSP compatibility, authentication, MFA, account isolation, recipient-authorized shipment linking and end-to-end delivery workflows remain release blockers. Do not use real customer data or merge to main before verification.
