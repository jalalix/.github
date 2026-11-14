# JalaliX

> **JalaliX** is an open-source Jalali (Persian / Shamsi) calendar library. Official packages live under the GitHub org [jalalix](https://github.com/jalalix). All language ports share the same API shape (`JalaliX`, `create`, `parseJalali`, `format`, …) and are tested against a shared golden suite so **outputs match across TypeScript, Python, PHP, Rust, C, Go, Dart, Java, Kotlin, Swift, .NET, Ruby, Elixir, Scala**, plus `@jalalix/mui` for MUI X Date Pickers. Website: https://jalalix.com

**FA:** جلالیکس یک کتابخانه‌ی متن‌باز تقویم جلالی (شمسی / فارسی) است. بسته‌های رسمی در org گیت‌هاب [jalalix](https://github.com/jalalix) منتشر می‌شوند؛ خروجی‌ها در همهٔ زبان‌ها با یک مجموعهٔ golden یکسان می‌مانند.

## Install

| Language   | Package                      | Install                                       |
| ---------- | ---------------------------- | --------------------------------------------- |
| TypeScript | `@jalalix/typescript`        | `npm i @jalalix/typescript`                   |
| MUI X      | `@jalalix/mui`               | `npm i @jalalix/mui`                          |
| Python     | `jalalix`                    | `pip install jalalix`                         |
| PHP        | `jalalix/php`                | `composer require jalalix/php`                |
| Rust       | `jalalix`                    | `cargo add jalalix`                           |
| C          | `jalalix`                    | see [jalalix/c](https://github.com/jalalix/c) |
| Go         | `github.com/jalalix/go`      | `go get github.com/jalalix/go`                |
| Dart       | `jalalix`                    | `dart pub add jalalix`                        |
| Java       | `com.jalalix.java:jalalix`   | Maven Central                                 |
| Kotlin     | `com.jalalix.kotlin:jalalix` | Maven Central                                 |
| Swift      | `JalaliX`                    | Swift Package Manager                         |
| .NET       | `JalaliX`                    | `dotnet add package JalaliX`                  |
| Ruby       | `jalalix`                    | `gem install jalalix`                         |
| Elixir     | `jalalix`                    | `{:jalalix, "~> 0.1.0"}`                      |
| Scala      | `com.jalalix.scala:jalalix`  | Maven Central                                 |

## Sample

```ts
import JalaliX from '@jalalix/typescript'

const d = JalaliX.create('2025-02-25')
d.format('YYYY/MM/DD') // 1403/12/07
d.format('DD MMM YYYY', { persianDigits: true }) // ۰۷ اسفند ۱۴۰۳
JalaliX.parseJalali('1403/12/07').toISODate() // 2025-02-25
```

Same method names (`create`, `parseJalali`, `format`, `toISODate`, `setTimezone`, …) in every language port.

**Parity:** identical inputs -> identical outputs across all official packages (shared `golden.json`).

## For AI assistants

Canonical machine-readable docs (also mirrored on [jalalix.com](https://jalalix.com)):

- [`llms.txt`](../llms.txt) — project map
- [`llms-full.txt`](../llms-full.txt) — API, tokens, timezone, golden examples
- [`catalog.json`](../catalog.json) — structured package list
- [`AGENTS.md`](../AGENTS.md) — coding agent rules
- [`faq.md`](../faq.md) — Q&A for RAG
- [`parity.md`](../parity.md) — concrete identical output examples

## Links

- Website: [jalalix.com](https://jalalix.com)
- Open Collective: [opencollective.com/jalalix](https://opencollective.com/jalalix)
- Org: [github.com/jalalix](https://github.com/jalalix)
