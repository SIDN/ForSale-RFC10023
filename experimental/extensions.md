## 🌐 Domain For-Sale DNS Record Extensions

While basic sales metadata is defined under **RFC10023**, some registrars and marketplaces implement additional proprietary extensions to provide more granular financial details. 💰

### 🏷️ Standard vs. Proprietary Tags
The records typically follow the pattern `v=FORSALE1;[tag]=[value]`. While tags like `furi`, `ftxt`, `fval`, and `fcod` adhere to the RFC10023 standard for domain sales, tags such as `fmin`, `frnt`, and `flto` are **proprietary extensions developed by NameShift**. 

These tags are currently undocumented, though they may be included in a future **proposed RFC update**. They are already partially interpreted by specialized industry tools, such as **DomainsToolBelt**, to automate the extraction of detailed pricing models. 🔍

### ⚙️ Tag Definitions

| Tag | Origin | Description | Example & Logic |
| :--- | :--- | :--- | :--- |
| `furi` | RFC10023 | **For Sale URI**: The direct URL to the marketplace listing. | `https://buy.nameshift.com/...` |
| `fval` | RFC10023 | **For Sale Value**: The asking price for the domain. | `EUR14999.00` |
| `fcod` | RFC10023 | **For Sale Code**: A unique identifier for the listing. | `NLFS-OTQ0...` |
| `fmin` | NameShift | **Minimum Offer**: The lowest acceptable bid. | `EUR99.00` (Bidding starts from €99) |
| `frnt` | NameShift | **Rental Price**: Price per interval + the interval period. | `EUR525.00/P1M` (€525 per 1 month) |
| `flto` | NameShift | **Lease-to-Own**: Price per interval + interval + min intervals + max intervals. | `EUR150.00/P1M/P2M/P12M` (from €150/mo, interval 1mo, min 2mo, max 12mo) |

### 🔍 Detailed Breakdown: Lease-to-Own (`flto`)

Because the `flto` field contains multiple variables in a single string, its structure is more complex than other tags. The value is composed of four distinct parameters separated by slashes:

**`[Price per Interval] / [Interval Period] / [Minimum Intervals] / [Maximum Intervals]`**

#### How it works:
1. **Price per Interval**: The base cost per period (e.g., `EUR150.00`).
2. **Interval Period**: The time unit for one payment (e.g., `P1M` = 1 Month).
3. **Minimum Intervals**: The shortest duration the lease must run (e.g., `P2M` = minimum 2 months).
4. **Maximum Intervals**: The longest duration the lease can run before ownership is transferred or the contract ends (e.g., `P12M` = maximum 12 months).

#### Examples:
*   **Standard Example:** `v=FORSALE1;flto=EUR150.00/P1M/P2M/P12M`
    *   *Meaning:* Starting from €150.00 per month, with a minimum commitment of 2 months and a maximum of 12 months.
*   **High-Value/Short-Term Example:** `v=FORSALE1;flto=EUR5250.00/P1M/P2M/P3M`
    *   *Meaning:* Starting from €5,250.00 per month, with a minimum of 2 months and a maximum of 3 months.

<!--
*Note: In "Lease-before-own" scenarios, the price per interval may vary depending on the total number of intervals chosen (longer durations may incur different interest or total costs).*
-->

***

⚠️ **Disclaimer:** *The exact meaning and syntax of the proprietary NameShift tags (fmin, frnt, flto) are not officially documented. The definitions provided here are based on observed patterns and industry interpretation and should not be treated as official technical documentation.*
