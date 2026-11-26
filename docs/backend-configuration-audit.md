# Backend configuration audit

All six public application tables have RLS enabled, no anonymous SELECT/INSERT/UPDATE/DELETE table grants or SELECT/INSERT/UPDATE column grants, and no authenticated DELETE/TRUNCATE grants. Supabase security advisor returned zero findings. Performance advisor returned 13 findings: one unindexed foreign key (delivery_requests.decided_by), seven auth RLS initialization plan findings, two unused indexes and three multiple permissive policy findings.

This was a read-only configuration audit, not an end-to-end role test. Earlier six functional assertions predate later admin migrations. Admin MFA and role isolation, authorized shipment linking, API runtime tests and abuse prevention remain release blockers. No real data was accessed or changed.
