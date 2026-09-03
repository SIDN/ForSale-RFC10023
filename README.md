# 🪧 ForSale - a digital for sale sign on domain names

Various resources with regard to [RFC10023](https://datatracker.ietf.org/doc/rfc10023/) [^1] - a lightweight method to add digital for sale signs to domain names.

🎉 Ready to sell your domain name? Why not put it up for sale with a [digital For Sale sign](https://www.sidnlabs.nl/en/news-and-blogs/a-digital-for-sale-sign-for-nl-domain-names) ?

## 👩🏻‍💻 It's that simple!

~~~
_for-sale.example.nl.	1800	IN	TXT	"v=FORSALE1;ftxt=Some human-readable info here."
_for-sale.example.nl.	1800	IN	TXT	"v=FORSALE1;furi=https://domain-sale.example.com/contact"
_for-sale.example.nl.	1800	IN	TXT	"v=FORSALE1;fval=USD1500"
~~~

Not sure yet? 🎓 Learn about the concept via the [ForSale Expert](https://expert.bitfire.nl) (an 🧠 AI agent).

> [!IMPORTANT]
> 🚨 Make sure to add the version tag `v=FORSALE1;` first, followed by a valid content tag (such as `ftxt=` or `furi=`) before entering the actual content value. Only then does it count as an official "for sale" sign that specialized tools will recognize.

ℹ️ More info here: https://rfc10023.nl/

## 👀 Check our one pager on http://forsaletxt.nl
> [!CAUTION]
> The _for-sale method documented here predates `forsaletxt.org`. The latter is an unrelated proposal and should not be confused with the original _for-sale method.

## ⓘ About ForSale

> **ForSale** is a standardized "_for-sale" DNS name for signaling that a domain name is available for purchase (or lease). The proposal addresses a common operational need by providing a machine-readable, globally consistent mechanism to indicate that domains are for sale, complementing inconsistent web-based parking pages and proprietary signaling methods.

## 💭 Why ForSale?

- **Machine-readable** – systems can automatically detect which domains are for sale.
- **Globally consistent** – the same mechanism works across top-level domains worldwide.
- **Supports automation** – helps domain brokers, domain investors, and acquisition tools reliably discover domains for sale.
- **Lightweight** – uses the DNS, so no extra infrastructure or web scraping is needed.

A paradigm shift in domain discovery: registrars, marketplaces and others can automatically query for-sale records and surface available domains directly in buyer-facing search results.

## 🤔 For whom ?
- **Individual domain owners** - just put up the For Sale sign and increase your chances of being discovered as this method gains traction.
- **Brokers** - add the For Sale indicator to every domain name in your portfolio and increase visibility.
- **Mediation services** - your case is much stronger when the domain name is clearly marked with a For Sale sign.
- **Domain name suggestion tools** - look for a For Sale indicator for every domain name you generate, rather than only checking whether the domain name is already registered.
- **Registries and registrars** - work together to improve visibility, [as SIDN did with the For Sale button in its WHOIS service](/examples/use-cases.md).
- **Online WHOIS/RDAP services** - check for a For Sale sign and let your users know when a domain name is available for purchase.
- **Coders** - build tools that make it easy to generate syntactically correct records or discover existing ones, making life easier for non-technical users.

> [!TIP]
> Check out the [examples](/examples) directory for more cool, advanced stuff!

## 🗞️ In the news
- https://www.bortzmeyer.org/10023.html
- https://domainincite.com/31851-now-you-can-plant-for-sale-signs-directly-into-your-domains
- https://www.techtimes.com/articles/322752/20260803/dns-gets-first-standard-commercial-intent-rfc-10023-enables-sale-tags.htm
- https://webhosting.today/2026/08/03/a-dns-record-now-flags-domains-for-sale-adoption-is-up-to-registrars/
- https://seodisias.com/blog/rfc-10023-for-sale-dns/
- https://nameocean.net/article/rfc-10023-the-dns-record-that-could-revolutionize-domain-flipping/
- https://www.inwx.com/en/blog/for-sale-dns-record-explained
- https://catches.io/blog/dns-for-sale-records-verified-sale-paths
- https://tech-blog.chatujme.cz/clanek/rfc-10023-for-sale-dns
- https://ecosistemastartup.com/rfc-10023-2026-como-vender-dominios-sin-perder-trafico-con-dns/
- https://www.gtldti.com/blog/rfc-10023-the-new-ietf-standard-turning-dns-into-a-commercial-signals-layer
- https://elsolitario.org/2026/08/09/registro-dns-for-sale-rfc-10023/
- https://www.top10hebergeurs.com/guide/infos-industrie/un-enregistrement-dns-peut-desormais-signaler-un-domaine-mis-en-vente
- https://domainbrief.de/artikel/ein-rfc-bringt-das-verkaufsschild-ins-dns
- https://www.weaving.news/news/019fe1bc-618b-7d89-b450-ee0b328836f3
- https://dzen.ru/a/andRGVisDFMq7eug
- https://www.xela.au/saas/a-domain-can-now-say-it-is-for-sale-in-dns-7e6f90
- https://www.dyj.live/knowledge/story_id-gm_explore-rss_a883b083f3d8a86da5d9a206d1553052
- https://tldtab.com/nl/updates/rfc-10023-for-sale-dns
- https://news.hada.io/topic?id=32278
- https://fr.news.hada.io/topic?id=32278
- https://asibiont.com/blog/a-domain-can-pochemu-domen-teper-mozhet-soobshchit-o-prodazhe-cherez-dns
- https://419.consulting/encrypted-dns/f/dns-in-the-news-17th-august-2026
- https://okky.kr/spaces/it-news/1561969
- https://imasters.com.br/noticia/dominio-agora-pode-se-declarar-a-venda-direto-no-dns-via-rfc-10023
- https://news.linxi.com.au/news/new-dns-standard-allows-domain-owners-to-signal-sale-intent-without-disrupting-traffic

## 🗂️ Other resources
- https://icannwiki.org/RFC_10023
- https://specification.website/spec/foundations/for-sale-dns/

## 🧰 Third-party implementations

A few implementations and tools that already support RFC 10023:

* **[forsaledns.net](https://forsaledns.net/)** — The first implementation, and still our recommended starting point.
* **[for-sale-dns.hx-std.com](https://for-sale-dns.hx-std.com/)** — Simple, lightweight, and does the job nicely.
* **[tldx](https://github.com/brandonyoungdev/tldx#domains-for-sale-rfc-10023)** — RFC 10023 support built right into the domain lookup tool.
* **[happyDomain](https://github.com/happyDomain/happydomain)** — Supports RFC 10023 for identifying domains that are for sale.
* **[PWhois.net](https://ipwhois.net/domain/example.nl)** — Now with RFC 10023 support too.
* **[Inspect My DNS](https://inspectmydns.com/example.nl)** - Has a banner on top when a `_for-sale` label is found.
* **[badge.forsale](https://badge.forsale/)** - Not entirely sure what this is, it feels a bit rough around the edges.
* **[Chromium Extension](https://github.com/mdavids/ForSale-RFC10023-browser-extensions)** - Experimental, but fully functional Chrome browser extension

<!-- ## ⚒ WORK IN PROGRESS - PLEASE CHECK BACK LATER -->

![ForSale logo](media/ForSale-banner.png)

[^1]: https://datatracker.ietf.org/doc/rfc10023/
