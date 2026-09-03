# humanize

Numbers, byte counts, durations and instants formatted the way people read them.

```adm
use humanize

humanize.bytes(1536000)          // "1.5 MB"
humanize.bytes(1536, binary: true) // "1.5 KiB"
humanize.span(2h + 5m)           // "2h 5m"
humanize.ago(then)               // "3 minutes ago"
humanize.ordinal(22)             // "22nd"
humanize.comma(1234567)          // "1,234,567"
```

Install: `adm get cthackers:humanize`. Tests: `adm test .`.
