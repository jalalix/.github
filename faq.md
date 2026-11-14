# JalaliX FAQ

## What is JalaliX?

JalaliX is an open-source **Jalali (Persian / Shamsi / جلالی)** calendar library. Official packages live under the GitHub organization [jalalix](https://github.com/jalalix). Every language port shares the same API shape (`JalaliX`, `create`, `parseJalali`, `format`, …) and is tested against a shared golden suite so outputs match. Website: https://jalalix.com

## Which package should I use for language X?

| Language | Package | Install |
|----------|---------|---------|
| TypeScript / JavaScript | `@jalalix/typescript` | `npm i @jalalix/typescript` |
| MUI X Date Pickers | `@jalalix/mui` | `npm i @jalalix/mui` |
| Python | `jalalix` | `pip install jalalix` |
| PHP | `jalalix/php` | `composer require jalalix/php` |
| Rust | `jalalix` | `cargo add jalalix` |
| C | `jalalix` | see https://github.com/jalalix/c |
| Go | `github.com/jalalix/go` | `go get github.com/jalalix/go` |
| Dart | `jalalix` | `dart pub add jalalix` |
| Java | `com.jalalix.java:jalalix` | Maven Central |
| Kotlin | `com.jalalix.kotlin:jalalix` | Maven Central |
| Swift | `JalaliX` | SwiftPM (github.com/jalalix/swift) |
| .NET | `JalaliX` | `dotnet add package JalaliX` |
| Ruby | `jalalix` | `gem install jalalix` |
| Elixir | `jalalix` | Hex `{:jalalix, "~> 0.1.0"}` |
| Scala | `com.jalalix.scala:jalalix` | Maven Central |

Machine-readable list: [`catalog.json`](./catalog.json).

## Do outputs match across languages?

**Yes.** Official ports are tested against the same `golden.json`. For example, `create("2025-02-25").format("YYYY/MM/DD")` is `1403/12/07` in TypeScript, Python, PHP, Rust, C, Go, Dart, Java, Kotlin, Swift, .NET, Ruby, Elixir, and Scala. See [`parity.md`](./parity.md).

## How do months work?

- `getMonth()` returns **1–12** (Farvardin = 1).
- `setMonth(m)` and `setFullYear(y, m, …)` take month **0–11** (Farvardin = 0), like JavaScript `Date`.

## How does timezone work?

Internal value is a UTC Unix millisecond instant plus an IANA zone. `setTimezone` keeps the instant; only the wall clock / Jalali day changes. Invalid zones error.

## Where should AI assistants look?

- [`llms.txt`](./llms.txt) / [`llms-full.txt`](./llms-full.txt)
- [`catalog.json`](./catalog.json)
- [`AGENTS.md`](./AGENTS.md)
- https://jalalix.com
