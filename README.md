# unlimited bandwidth proxies: how to tell real unmetered plans from fair-use ones, and pick the package that fits your traffic

If you typed *unlimited bandwidth proxies* into a search box, the odds are you're reacting to a bill rather than shopping for a category. A scraping run that was budgeted at $30 lands at $140 because the target pages got heavier halfway through. Or a traffic pack expires with gigabytes still sitting in it. Or you bought "unlimited" and got an email at 90 GB telling you the rest of the month bills at pay-as-you-go rates.

Three completely different arrangements hide behind the same two words, and only one of them is actually about bandwidth:

1. **Unmetered per-IP packages.** You buy a fixed number of IPs and pay nothing per gigabyte. Traffic simply isn't counted. The constraint is how many IPs you hold and how long each one stays alive.
2. **Metered packs with no monthly reset.** You still pay per gigabyte, but the balance doesn't evaporate on the 1st of the month.
3. **Fair-use "unlimited."** The plan page says unlimited; the fair-use policy defines a threshold and describes what happens when you cross it.

Most comparison articles cover only the third category, usually by paraphrasing the homepage. So here's what the published policies actually say, where the per-IP model wins on cost, and how 9Proxy structures its packages if you want to test the unmetered route with something concrete.

## The fine print behind "unlimited"

This is the part worth reading slowly, because the thresholds are not in the headlines.

| Provider | What "unlimited" is limited by | What the policy says happens next |
| --- | --- | --- |
| Bright Data | 100 GB per proxy per month on unlimited ISP proxies (shared or dedicated) | Email reminders, then overage billed at the current pay-as-you-go rate |
| Oxylabs | Unlimited traffic on dedicated datacenter and ISP IPs, with fair-use rules applied to concurrent sessions | Session allowance is reduced for the remainder of the month once the threshold is crossed |
| Decodo | Two conditions combined: total traffic for the subscription term, plus traffic per individual IP | Concurrent sessions reduced for the rest of the term |
| Webshare | Unlimited bandwidth only at high proxy counts (1,000 premium, 100 private, or 75 dedicated proxies) | Lower tiers stay metered; speed may be temporarily reduced if you breach the policy |
| IPRoyal | Unmetered on dedicated ISP and datacenter; mobile has a daily soft cap | Mobile throughput is capped per day |
| 9Proxy | IP-based packages aren't traffic-metered at all — the limit is unlimited *while an IP is active* | The real constraints are IP count and session lifetime, not gigabytes |

Those thresholds move, and vendors phrase them differently, so treat the table as a map of where to look rather than a permanent record. The pattern is consistent though: when a provider sells unlimited by traffic, they usually protect themselves with either a per-proxy ceiling or a limit on concurrent sessions. When a provider sells unlimited by IP, they protect themselves with how long each IP lives and how many you must buy.

That distinction matters more than the word "unlimited."

## The math that actually decides between per-IP and per-GB

Work it out in bytes per IP and the choice stops being a matter of taste.

Take 9Proxy's smallest IP-based package: 100 residential IPs for **$24**, with no traffic metering. Push 50 GB through those 100 IPs and your effective rate is $0.48/GB, which is worse than the 100 GB traffic pack at $1.50/GB. Push 500 GB through the same 100 IPs and the effective rate drops to $0.048/GB — roughly 30x cheaper per gigabyte than the same money buys in traffic. The $24 never changes; the denominator does.

Flip it around. If your job needs 5,000 different IPs but each request fetches a 40 KB HTML page, you'd have burned a fortune in IP purchases to move maybe 200 MB. A traffic pack is the honest answer there, because 9Proxy's GB model lets you generate unlimited proxy endpoints and only deducts the gigabytes you consume.

So the deciding question is simple: **how many bytes does each IP carry?**

- High bytes per IP (long sessions, large payloads, logged-in workflows, video-adjacent tasks) → per-IP, unmetered.
- Low bytes per IP but high IP diversity (SERP checks, price spot-checks, ad verification, geo tests) → per-GB.
- Both at once (stable sessions *and* rotation) → a bundle.

The catch on the per-IP side isn't bandwidth, it's concurrency and lifespan. In 9Proxy's IP-based model each forwarded IP counts as one used IP from your balance, and it stays live somewhere between a few hours and about 24 hours depending on the peer's connection. If your workflow assumes a proxy that stays put for a month, this is the wrong product category. If it just needs a clean residential IP for one working session, it's exactly right.

👉 [Compare 9Proxy's unmetered IP packages and per-GB traffic packs](https://bit.ly/9-Proxy)

## How 9Proxy's model is built

9Proxy is a residential proxy network covering 20M+ IPs across 90+ countries. Targeting goes down to country, state, city, ZIP and ISP level, and it speaks HTTP/HTTPS and SOCKS5. The vendor lists 99.95% uptime as a network figure, and a 2025 review in iTWire measured uptime "nearing 99%" for scraping and account management work.

Two things are worth understanding before you buy anything.

**IP-based packages.** You buy a block of IPs; unused ones never expire; traffic while an IP is active isn't counted. Connecting requires the 9Proxy desktop app, which forwards local ports. That's a real trade-off rather than a footnote: it works on Windows, macOS and Linux, but it is less convenient than a browser extension or a plain username-and-password endpoint when you want the same proxies on several machines.

**GB-based packages.** Entirely dashboard-driven, no app. Generate as many endpoints as you like, authenticate with username/password or IP whitelisting, and choose sticky or rotating sessions. Traffic here is metered against your balance and valid for 180 days, and it's worth noting that 9Proxy's June 2026 price adjustment left GB pricing untouched while IP-based and bundle pricing moved.

Two operational details matter more than the spec sheet. Auto-refresh swaps out dead IPs within about 60 seconds, and a reuse feature pulls back IPs used in the previous 24 hours so you can run them again for free instead of buying fresh ones. Reuse is the kind of thing that quietly cuts spend for anyone running repeating jobs against the same targets.

Teams get a separate structure: the Enterprise tier removes the 180-day traffic expiry, supports one owner plus up to five members, and lets traffic be shared inside the team with per-member controls and activity logs.

## Every package 9Proxy currently lists

Prices below are the published ones at the time of writing. IP-based and bundle pricing was adjusted in June 2026; GB-based pricing was left as-is.

| Package | What you get | Price | Effective rate | Billing & validity | Purchase |
| --- | --- | --- | --- | --- | --- |
| 100 IPs | 100 residential IPs, unmetered traffic | $24 | $0.24/IP | One-time balance purchase; unused IPs don't expire | [Get the 100-IP pack](https://bit.ly/9-Proxy) |
| 500 IPs | 500 residential IPs, unmetered traffic | $72 | $0.144/IP | One-time; IPs don't expire | [Get the 500-IP pack](https://bit.ly/9-Proxy) |
| 1,000 + 500 IPs | 1,500 IPs including bonus | $126 | $0.084/IP | One-time; IPs don't expire | [Get the 1,500-IP pack](https://bit.ly/9-Proxy) |
| 2,500 IPs | 2,500 residential IPs, unmetered | $210 | $0.084/IP | One-time; IPs don't expire | [Get the 2,500-IP pack](https://bit.ly/9-Proxy) |
| 5,000 IPs | 5,000 residential IPs, unmetered | $360 | $0.072/IP | One-time; IPs don't expire | [Get the 5,000-IP pack](https://bit.ly/9-Proxy) |
| 15,000 IPs | 15,000 residential IPs, unmetered | $720 | $0.048/IP | One-time; IPs don't expire | [Get the 15,000-IP pack](https://bit.ly/9-Proxy) |
| 25,000 IPs | 25,000 residential IPs, unmetered | $863 | $0.035/IP | One-time; IPs don't expire | [Get the 25,000-IP pack](https://bit.ly/9-Proxy) |
| 50,000 IPs | 50,000 residential IPs, unmetered | $1,438 | $0.029/IP | One-time; IPs don't expire | [Get the 50,000-IP pack](https://bit.ly/9-Proxy) |
| Business 100,000 IPs | High-volume residential block | $2,300 | $0.023/IP | One-time; IPs don't expire | [Get the business 100,000-IP pack](https://bit.ly/9-Proxy) |
| Business 200,000 IPs | High-volume residential block | $4,140 | $0.021/IP | One-time; IPs don't expire | [Get the business 200,000-IP pack](https://bit.ly/9-Proxy) |
| Business 500,000 IPs | Highest-volume residential block | $8,625 | $0.018/IP | One-time; IPs don't expire | [Get the business 500,000-IP pack](https://bit.ly/9-Proxy) |
| 5 GB | Metered traffic, rotating endpoints | $15 | $3.00/GB | 180-day validity | [Get the 5 GB pack](https://bit.ly/9-Proxy) |
| 50 + 5 GB | Metered traffic with bonus | $105 | $2.10/GB | 180-day validity | [Get the 55 GB pack](https://bit.ly/9-Proxy) |
| 100 GB | Metered traffic | $150 | $1.50/GB | 180-day validity | [Get the 100 GB pack](https://bit.ly/9-Proxy) |
| 200 GB | Metered traffic | $200 | $1.00/GB | 180-day validity | [Get the 200 GB pack](https://bit.ly/9-Proxy) |
| 1,000 GB | Metered traffic | $800 | $0.80/GB | 180-day validity | [Get the 1,000 GB pack](https://bit.ly/9-Proxy) |
| 2,000 GB | Metered traffic | $1,500 | $0.75/GB | 180-day validity | [Get the 2,000 GB pack](https://bit.ly/9-Proxy) |
| Enterprise 3,000 GB | Metered traffic, no expiry | $2,160 | $0.72/GB | Traffic never expires | [Get the enterprise 3,000 GB pack](https://bit.ly/9-Proxy) |
| Enterprise 6,000 GB | Metered traffic, no expiry | $4,200 | $0.70/GB | Traffic never expires | [Get the enterprise 6,000 GB pack](https://bit.ly/9-Proxy) |
| Enterprise 10,000 GB | Metered traffic, no expiry | $6,800 | $0.68/GB | Traffic never expires | [Get the enterprise 10,000 GB pack](https://bit.ly/9-Proxy) |
| Starter bundle | 100 IPs + 5 GB | $30 | Mixed IP + traffic | 180-day traffic validity | [Get the Starter bundle](https://bit.ly/9-Proxy) |
| Popular bundle | 1,500 IPs + 50 GB | $180 | Mixed IP + traffic | 180-day traffic validity | [Get the Popular bundle](https://bit.ly/9-Proxy) |
| Pro bundle | 5,000 IPs + 500 GB | $720 | Mixed IP + traffic | 180-day traffic validity | [Get the Pro bundle](https://bit.ly/9-Proxy) |

The shape of that list is the useful part. Per-IP pricing falls from $0.24 to $0.018 as volume rises, which is roughly a 13x spread for the same product. If you're buying 100 IPs repeatedly instead of 1,000 at once, you're paying for convenience at a steep rate. On the traffic side, the spread runs from $3.00/GB down to $0.68/GB, and only the Enterprise tier removes the 180-day clock.

## Matching a package to a real workload

**Testing whether unlimited bandwidth works for you at all.** The 100-IP pack at $24 or the 5 GB pack at $15. Both are small enough to be a learning expense, and the IP pack doubles as a bandwidth experiment — run a week of normal traffic through it and look at what your metered provider would have charged.

**A few hundred long-lived account sessions with unpredictable data use.** Somewhere between the 500-IP and 2,500-IP packs. You're buying stability and the freedom to stop thinking about gigabytes, which is the entire point of the unmetered model.

**SERP tracking, price checks, ad verification, geo testing.** Thousands of tiny requests, each needing a fresh IP. The 100 GB or 200 GB traffic packs fit, since rotating across the whole pool is included rather than billed as IP activations.

**Agency work with mixed jobs.** The Popular bundle at $180 is the awkward-middle-justifier: 1,500 IPs for clients who need persistent sessions, 50 GB for the ones who need rotation, one invoice.

**Reseller or platform-scale operations.** The 25,000-IP tier and above, or the Business blocks. Volume discounts are the whole game here, and the per-IP rate at 500,000 is a quarter of what it is at 500.

## Things worth checking before you pay

The IP-based model needs the desktop app. If your stack lives in containers or you're running proxies across several machines, plan for that, or use the GB model instead, which authenticates by username/password or IP whitelist straight from the dashboard.

There's no standing free tier on the pricing page. Trial access has historically been promotion-based rather than permanent, and reviewers have noted that you ask support for trial codes when they're available. Budget for a small paid package instead of assuming a free trial will appear.

IP lifespan is measured in hours, not months. That's normal for residential, but it rules out anything that needs a genuinely permanent sticky address.

Streaming isn't the target use case. A 2025 review found the service worked well against e-commerce anti-bot systems but ran into detection on services like Netflix, which is a fair warning to anyone searching for unlimited bandwidth for streaming rather than data work.

Support runs 24/7 through Telegram, email and a ticket system, and third-party directories currently list the provider in the 3.9-to-4 star band. That's a mid-market rating, not an enthusiast one — consistent with the budget positioning.

## FAQ

**Is unlimited bandwidth the same as unlimited proxies?**
No. On per-IP packages, the bandwidth is unlimited while an IP is active; your IP count is finite and each forwarded IP is deducted from the block you bought. The traffic packs are the reverse: unlimited endpoints to generate, but a finite number of gigabytes.

**Do unused IPs expire?**
No. 9Proxy's IP-based balance is stored until used. Traffic balance is different: 180 days on standard GB packs, unlimited on Enterprise.

**Do I need the desktop app?**
For IP-based proxies, yes. For GB-based proxies, no.

**What's the cheapest way to test the unmetered model?**
100 IPs for $24. It's the smallest IP block listed, and since bandwidth isn't metered there, the cost is capped no matter how much you push through it.

**Can a team share one package?**
The Enterprise tier supports one owner plus up to five members with shared, non-expiring traffic and per-member usage controls.

## The short version

"Unlimited bandwidth proxies" is not one product. On most large providers it means a fair-use threshold you'll find in the terms rather than the pricing table. On per-IP packages it means traffic genuinely stops being the unit of billing, and the real limits shift to how many IPs you hold and how long each one lives.

If your cost problem is heavy, unpredictable data use across a manageable number of sessions, 9Proxy's IP-based packages at $24 for 100 IPs are the cheapest way to stop counting gigabytes. If your cost problem is needing thousands of different IPs for small requests, the traffic packs and bundles are the better fit — the 1,500 IPs plus 50 GB bundle at $180 covers both halfway decently.

👉 [Check 9Proxy's current packages and pick the one that matches your workload](https://bit.ly/9-Proxy)
