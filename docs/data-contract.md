# Observation contract

Input is a JSON array with at most 500 observations. Each record requires nonempty `name`, `category`, `unit`, `source`, and `observedAt` strings; a positive finite numeric `previous`; and a nonnegative finite numeric `current`.

Change = (current − previous) / previous × 100. Flag when absolute change meets or exceeds the selected threshold. A tiny numeric tolerance handles floating-point boundary comparisons.

Keep the same unit, region, product specification, role, service bundle, taxes, and purchasing terms within each pair. The demo stores a source label and date string but does not validate URLs, dates, or provenance. Different currencies must be normalized before comparison.
