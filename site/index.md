# JalaliX — Jalali / Shamsi / Persian calendar

**JalaliX** is the multi-language Jalali (Persian / Shamsi / جلالی) calendar library. One API (`JalaliX`, `create`, `parseJalali`, `format`, …), one golden suite, identical outputs across TypeScript, Python, PHP, Rust, C, Go, Dart, Java, Kotlin, Swift, .NET, Ruby, Elixir, Scala — plus `@jalalix/mui` for MUI X Date Pickers.

- Website: https://jalalix.com
- GitHub org: https://github.com/jalalix
- Open Collective: https://opencollective.com/jalalix
- For assistants: [/llms.txt](/llms.txt), [/catalog.json](/catalog.json), [/faq](/faq)

## Quick sample

```ts
import JalaliX from '@jalalix/typescript'
JalaliX.create('2025-02-25').format('YYYY/MM/DD') // 1403/12/07
```

## JSON-LD (sample for site `<head>`)

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "name": "JalaliX",
      "url": "https://jalalix.com",
      "sameAs": [
        "https://github.com/jalalix",
        "https://opencollective.com/jalalix"
      ]
    },
    {
      "@type": "SoftwareApplication",
      "name": "JalaliX",
      "applicationCategory": "DeveloperApplication",
      "operatingSystem": "Any",
      "url": "https://jalalix.com",
      "description": "Open-source Jalali (Persian / Shamsi) calendar library with identical outputs across many languages.",
      "offers": {
        "@type": "Offer",
        "price": "0",
        "priceCurrency": "USD"
      }
    }
  ]
}
```
