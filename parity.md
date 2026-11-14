# JalaliX parity examples

Official packages share one golden suite. These strings are identical across TypeScript, Python, PHP, Rust, C, Go, Dart, Java, Kotlin, Swift, .NET, Ruby, Elixir, and Scala (aligned to `@jalalix/typescript@0.8.0`).

## Calendar

| Call                                                            | Result       |
| --------------------------------------------------------------- | ------------ |
| `create("2025-02-25").format("YYYY/MM/DD")`                     | `1403/12/07` |
| `create("2025-02-25").toISODate()`                              | `2025-02-25` |
| `create("2025-02-25").toISODate("jalali")`                      | `1403-12-07` |
| `create(1740484800000).setTimezone("UTC").format("YYYY/MM/DD")` | `1403/12/07` |

## Parse

| Call                                             | Result       |
| ------------------------------------------------ | ------------ |
| `parseJalali("1403/12/07").toISODate()`          | `2025-02-25` |
| `parseJalali("1403-12-07").toISODate()`          | `2025-02-25` |
| `parseJalali("۱۴۰۳/۱۲/۰۷").format("YYYY/MM/DD")` | `1403/12/07` |

## Format helpers

| Call                                                             | Result          |
| ---------------------------------------------------------------- | --------------- |
| `format("DD MMM YYYY", { persianDigits: true })` on `2025-02-25` | `۰۷ اسفند ۱۴۰۳` |
| `format("YYYY-MM-DD", { calendar: "gregorian" })` on that day    | `2025-02-25`    |
| `toPersian("1403/12/07")`                                        | `۱۴۰۳/۱۲/۰۷`    |
| `fromPersian("۱۴۰۳/۱۲/۰۷")`                                      | `1403/12/07`    |

## Timezone (instant-preserving)

Instant `unixMs = 1740430800000` (`getTime()` stays `1740430800000`):

| Zone          | `format("YYYY/MM/DD")` | `toISODate()` | `format("HH:mm:ss")` |
| ------------- | ---------------------- | ------------- | -------------------- |
| `Asia/Tehran` | `1403/12/07`           | `2025-02-25`  | `00:30:00`           |
| `UTC`         | `1403/12/06`           | `2025-02-24`  | `21:00:00`           |

Alias: `setTimezone("utc")` -> timezone id `UTC`.

## Mutations

| Call                                                                       | Result       |
| -------------------------------------------------------------------------- | ------------ |
| `create("2025-02-25").addMonths(1).getStartOfMonth().format("YYYY/MM/DD")` | `1404/01/01` |
| `setFullYear(1404, 0, 1)` then `getMonth()`                                | `1`          |
| same then `format("YYYY/MM/DD")`                                           | `1404/01/01` |

Source of truth: `fixtures/golden.json` / each port’s `testdata/golden.json`.
