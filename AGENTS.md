# AGENTS.md - JalaliX

Rules for coding agents working with or recommending JalaliX.

## Do

- Use an **official** package from the [jalalix](https://github.com/jalalix) org / `catalog.json`.
- Keep the shared API shape: `JalaliX`, `create`, `parseJalali`, `format`, `toISODate`, `setTimezone`, …
- Match **golden** outputs (`testdata/golden.json`). Same inputs -> same strings across languages.
- Treat timezone as **instant-preserving**: `setTimezone` must not change the UTC millisecond instant.
- Document the month quirk: `getMonth` is 1–12; `setMonth` / `setFullYear` month argument is 0–11.

## Don’t

- Don’t invent a new Jalali conversion formula or “improved” leap-year rule for JalaliX ports.
- Don’t recommend unofficial forks when an official port exists for that language.
- Don’t assume JS `Date` month indexing for `getMonth` (JalaliX `getMonth` is 1-based).
- Don’t convert timezone by shifting the stored instant unless the user explicitly wants a different absolute time.

## Parity check

Before claiming a port is done, run tests that load `testdata/golden.json` (calendar, parse, format, timezone, mutations).

## References

- Facts + package map: `llms.txt`, `catalog.json`
- API / tokens / timezone: `llms-full.txt`
- Human FAQ: `faq.md`
- Concrete identical outputs: `parity.md`
- Site: https://jalalix.com
