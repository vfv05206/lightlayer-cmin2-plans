# Lightlayer CMIN2: Which Plans Actually Include It, What Premium Costs Over Global, and Is the $49.99 Annual VPS Worth It? (Full Plan Table + Test IPs)

CMIN2 sits on exactly one LightLayer route tier, Premium. Any plan you order on the Standard or Global route runs on ordinary transit and gets none of it, regardless of what the plan name or the headline price suggests. On the same 1-core/1GB Los Angeles VPS, that difference shows up as $4/month on Global, $5.60/month on Standard, and roughly $7+/month on Premium, or $29.99, $39.99 and $49.99 if you pay for a year up front.

What follows is the full plan list with the routes you can actually order on each, an honest breakdown of how CN2 GIA and CMIN2 split the work, the yearly cost of the Premium upgrade, and two published test IPs you can ping before spending anything.

## Quick answer before the details

> **Most readers:** Los Angeles Premium, **$49.99/year** for 1 core / 1GB RAM / 50GB SSD with China Telecom CN2 GIA plus China Mobile CMIN2. It is the cheapest confirmed way to get CMIN2 on a US IP. 👉 [Order the Los Angeles Premium annual plan](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74)
>
> **Asia node, tight budget:** Manila or Taiwan at **$24.99/year** (about $2.08/month). Both list Premium, Standard and Global as selectable routes, so pick Premium in the cart and confirm the route label before paying.
>
> **No mainland China or APAC traffic:** Los Angeles Global at **$29.99/year**, or $4/month. Paying for CMIN2 you will not use is the most common way to waste money here.

## Every LightLayer cloud plan currently listed

The monthly tiers are the same across regions, with resource add-ons handled through the configurator rather than fixed bundles.

| Plan | CPU / RAM / Storage | Bandwidth | Price | Order |
| --- | --- | --- | --- | --- |
| Startup | 1 core / 1GB / 50GB SSD | 100Mbps, unlimited | **$4.00/month** | [Order Startup](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74) |
| Pay As You Go (Base) | 2+ cores / 2GB+ / scalable storage | 200Mbps, unlimited | **from $5.60/month** | [Configure a custom plan](https://account.lightlayer.net/index.php?/cart/specialoffer/&affid=74) |
| Business | 32 cores / 32GB / scalable storage | 200Mbps, unlimited | **$53.60/month** | [Order Business](https://account.lightlayer.net/index.php?/cart/specialoffer/&affid=74) |

The annual listings are where the route choice becomes explicit, and they are all the same 1-core/1GB/50GB SSD spec:

| Location | Route | Annual price | Effective monthly | Order |
| --- | --- | --- | --- | --- |
| Manila | Premium / Standard / Global | **$24.99/year** | ~$2.08 | [Get Manila annual](https://account.lightlayer.net/index.php?/cart/manila/&affid=74) |
| Taiwan | Premium / Standard / Global | **$24.99/year** | ~$2.08 | [Get Taiwan annual](https://account.lightlayer.net/index.php?/cart/taiwan/&affid=74) |
| Los Angeles | Global | **$29.99/year** | ~$2.50 | [Get LA Global annual](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74) |
| Los Angeles | Standard | **$39.99/year** | ~$3.33 | [Get LA Standard annual](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74) |
| Los Angeles | Premium (CN2 GIA + CMIN2) | **$49.99/year** | ~$4.17 | [Get LA Premium annual](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74) |

Two things the tables do not tell you. The cart also surfaces a mid-range configuration around 4 cores / 4GB / 80GB SSD in the $11–18/month band depending on route, and resource limits are set per node, so the configurator is the authoritative quote. Billing cycles run monthly, quarterly, semi-annual and annual, with the longer commitments priced lower.

A caveat on Manila and Taiwan worth stating plainly: the annual table lists all three routes at the same $24.99, but it does not confirm that the Premium variant at that price carries CN2 GIA and CMIN2 the way the Los Angeles Premium listing does. Check the route label and the network description in the cart before you pay. If the Premium option shows a different price, the cart is correct and the summary table is not.

## What Premium, Standard and Global actually change

Same hardware, different path to the internet. LightLayer offers all three tiers across its 25+ locations, which span Los Angeles, San Jose and Ashburn in North America; Hong Kong, Manila, Taiwan, Tokyo, Singapore and Bangkok in Asia-Pacific; and Frankfurt and London in Europe.

**Premium** routes traffic over China Telecom's CN2 GIA backbone and China Mobile's CMIN2 network. Those are the two premium international paths for the two largest Chinese carriers, and having both matters because a mainland audience is split between them. A server optimized only for China Telecom still leaves China Mobile visitors on congested transit at peak hours. This is the tier LightLayer itself frames as the one to buy when your users are in China or your application needs consistent latency to Asia-Pacific.

**Standard** is conventional BGP transit. It is a reasonable general-purpose international path with no carrier-specific optimization, and it is what the $5.60 Pay As You Go base sits on.

**Global** is the international/Anycast tier, built for broad reach rather than any single region. It is the cheapest and the right answer for a US or European audience.

CMIN2 is China Mobile. CN2 GIA is China Telecom. Neither appears on Standard or Global, and no amount of upgrading CPU or RAM adds them, because the surcharge is transit cost, not compute.

## The price arithmetic: $20 a year for CMIN2

Los Angeles, identical 1-core/1GB/50GB configuration:

- Monthly: Global $4.00 → Standard $5.60 → Premium $7.00+ (a $3/month jump from the bottom)
- Annual: Global $29.99 → Standard $39.99 → Premium $49.99 (a $20/year jump from the bottom)

The annual Premium surcharge works out to about **$1.67 per month** over Global. Annual also beats monthly Premium by roughly 40% ($49.99 versus $84 if you paid $7 twelve times). If your users are in mainland China and the site is staying up for a year, that $20 is the cheapest performance upgrade on the entire order form. If they are not, it buys nothing you can measure.

The Manila and Taiwan annual plans are the low-cost entry point. At $24.99/year they undercut even Los Angeles Global, which makes them the sensible place to test whether a Premium Asia route is worth it to you before committing to a larger box.

👉 [Compare the Los Angeles route options side by side](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74)

## CMIN2 beyond Cloud VPS

**Dedicated servers.** LightLayer's US dedicated lineup in San Jose and Los Angeles is marketed with premium CMIN2 routing as a selectable option alongside standard and international BGP. Promotional pricing on these moves constantly and configurations vary by chassis, so treat any figure you see quoted in a review as historical and confirm the current quote on the order page. The route option is the part that stays relevant to this keyword.

**GPU servers.** NVIDIA RTX 4090 configurations in Dallas, from single card up to eight for AI training, inference and rendering. No route information is published for these, and pricing is quoted rather than listed, so ask before assuming CMIN2 is available.

**San Jose SJ-Lite.** A budget cloud line launched in San Jose on 24 September 2026, announced as 1C1G / 50G HDD / 1 IP / "300M-500G Premium Network". That spec string does not say whether 300M-500G refers to port speed, monthly traffic, or something else, and the announcement does not clarify it. Read the cart description if the $4.90-class price appeals to you.

## Ping it before you buy

LightLayer publishes Premium test IPs, which is more than most budget hosts do:

- **Los Angeles Premium:** `128.241.250.254`
- **Hong Kong Premium:** `156.245.234.254`

Run a ping and a traceroute from where your actual users sit, not from your laptop if those are different places. Look at two numbers: median latency, and the spread between best and worst. The spread is what CN2 GIA and CMIN2 are really buying. Congested transit can show a decent average and still swing 80ms at 9pm Beijing time, which is exactly when a route without premium capacity falls apart.

If the traceroute from your city shows China Telecom's CN2 path (59.43.x.x hops) and China Mobile's CMIN2 path, the Premium tier is doing what you are paying for. If it resolves to ordinary transit, you are on the wrong route or the wrong location.

## Who should buy Premium, and who should not

Premium earns its $20/year for: a site or API whose visitors are mostly in mainland China or East Asia; remote development boxes accessed from China; small SaaS products sold into APAC; anyone whose current host is fine in the morning and unusable at peak.

Skip it for: a US-only audience, a European audience, a staging server, or anything where the visitor geography is genuinely unclear. The $4 Global plan and the $29.99 annual are the correct purchase in those cases, and buying Premium "just in case" is money spent on routing you will never exercise.

LightLayer as a whole is a budget provider with the trade-offs that implies. There are no managed services, no hand-holding, and no published SLA that I could verify. Multiple reviews and forum threads describe ticket response times as inconsistent, the control panel as functional but plain, and performance as variable between nodes within the same data center. For development environments, side projects, small and mid-size sites, and cost-sensitive APAC deployments, those trade-offs are reasonable. For a revenue-critical production system where an hour of downtime has a dollar figure attached, budget hosting without contractual uptime is the wrong tool.

## Renewals, promo codes and the refund question

LightLayer runs recurring promotions, and historically these have included Hong Kong, London and Los Angeles cloud plans discounted to around $15/month, plus regional percentage discounts on Japan cloud and Philippines dedicated hardware. Whether any specific code from a 2025 or early 2026 review is still live in November 2026 is something I cannot confirm, and a dead code at checkout is a worse experience than no code at all. Check the Special Offer page before you order instead of trusting a list.

On renewals, multiple reviews and user reports say promotional pricing has held at renewal rather than reverting to list price, including on recurring promo codes. That is a genuinely uncommon behavior in this price bracket and worth weighing. It is also user-reported, not a contractual term, so screenshot your invoice and confirm the renewal rate shown in the client area.

On refunds, I found no advertised money-back window. Third-party plan trackers list LightLayer's policy as covering provider-side faults only, with no refund for change of mind on regular or promotional products. Assume the purchase is final and test with the IPs and a monthly term first if you are unsure.

Payment is PayPal, major credit cards and Alipay, which removes the usual card-only friction for buyers in China.

## FAQ

**Is CMIN2 the same as CN2 GIA?**
No. CN2 GIA is China Telecom's premium backbone, CMIN2 is China Mobile's international network. LightLayer's Premium tier uses both, which is why it works reasonably for a mixed Chinese audience. A provider advertising only CN2 GIA is optimizing for Telecom users and leaving Mobile users on whatever transit is available.

**Does the $4 plan include CMIN2?**
No. The $4 Startup plan is the entry configuration on the Global route. CMIN2 requires selecting Premium, which on the Los Angeles 1-core/1GB spec starts around $7/month or $49.99/year.

**Is the $24.99 Manila or Taiwan annual plan CMIN2?**
Only if you select the Premium route at checkout. Those locations list Premium, Standard and Global as options at the same headline annual price, and the listing does not spell out the network details per variant. Confirm the route in the cart.

**Can I pay with Alipay?**
Yes, alongside PayPal and major credit cards.

**Will the renewal price go up?**
Users report that promotional rates have held at renewal. There is no official no-increase commitment that I could verify, so confirm the renewal figure on your invoice rather than assuming.

## The decision

Users in mainland China or APAC, want a US IP: Los Angeles Premium at $49.99/year. It is $20 more than Global annually and the only confirmed CMIN2 option on a US node.

Budget first, Asia location acceptable: Manila or Taiwan at $24.99/year with Premium selected, roughly $2.08/month.

No China or APAC traffic: Los Angeles Global at $29.99/year, or $4/month if you want to walk away after four weeks.

Want to test the route on a monthly term first: Los Angeles Premium at about $7+/month, then convert to annual once the traceroute looks right from your users' location.

Two things to check before you pay: the route label in the cart (Premium, not Standard or Global), and the renewal price shown on the invoice. Everything else on this page is secondary to those two lines.

👉 [Start with the Los Angeles Premium cart and confirm the route before checkout](https://account.lightlayer.net/index.php?/cart/los-angeles/&affid=74)
