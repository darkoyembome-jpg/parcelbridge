# Backend optimization

Applied migration index_delivery_decision_actor: CREATE INDEX IF NOT EXISTS delivery_requests_decided_by_idx ON public.delivery_requests(decided_by).

Verified index in pg_indexes. Security advisor: zero findings. Performance advisor: missing foreign key index resolved; seven auth policy findings, three unused index findings (including newly created index), and three overlapping policy findings remain. Retain new index pending workload evidence. No authorization policies changed. Supabase markdown changelog could not be retrieved; RLS documentation lookup succeeded.
