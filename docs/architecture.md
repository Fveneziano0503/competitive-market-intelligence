# Architecture

Implemented: manually entered observation JSON → type validation → percentage changes → threshold flags → filtered brief and CSV. The browser makes no network requests and retains no data after reload.

Proposed: authorized feeds and permitted web sources → scheduled collection → normalization and units → source/date/version retention → anomaly checks → optional AI synthesis → human-reviewed brief. The planned collector must handle failures and stale data rather than silently reusing an old value as current. Duplicate or changed source definitions need review before comparison.

AI synthesis should reference underlying observations and separate supported facts from hypotheses. The current brief is template-based. No agent autonomously visits sources or acts on findings.
