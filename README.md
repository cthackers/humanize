# humanize

Numbers, byte counts, durations and instants formatted the way people read them.

```adm
use humanize

// bytes
humanize.bytes(1536000)             // "1.5 MB"
humanize.bytes(1536, true)          // "1.5 KiB"
humanize.bytesPerSecond(1536000)    // "1.5 MB/s"
humanize.parseBytes("1.5 MB")       // 1500000

// numbers
humanize.comma(1234567)             // "1,234,567"
humanize.ordinal(22)                // "22nd"
humanize.number(1234567)            // "1.2M"
humanize.percent(2, 3, 1)           // "66.7%"
humanize.percent(0.42)              // "42%"
humanize.words(1234)                // "one thousand two hundred thirty-four"
humanize.fuzzyNumber(48713)         // "about 49k"

// durations
humanize.span(2h + 5m)              // "2h 5m"
humanize.spanLong(2h + 5m)          // "2 hours 5 minutes"
humanize.clock(1h + 5m + 9s)        // "01:05:09"

// instants
humanize.ago(then)                  // "3 minutes ago" / "in 2 hours"
humanize.until(deadline)            // "2 hours"
humanize.date(then)                 // "yesterday" / "Mon 7 Sep" / "7 Sep 2025"

// text
humanize.list(["a", "b", "c"])      // "a, b and c"
humanize.truncate("hello world", 8) // "hello w…"
```

Install: `adm get cthackers:humanize`. Tests: `adm test .`.
