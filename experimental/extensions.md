## 🌐 Domain For-Sale DNS Record Extensions

While basic sales metadata is defined under **RFC10023**, some registrars and marketplaces implement additional proprietary extensions to provide more granular financial details. 💰

### 🏷️ Standard vs. Proprietary Tags
The records typically follow the pattern `v=FORSALE1;[tag]=[value]`. While tags like `furi`, `ftxt`, `fval`, and `fcod` adhere to the RFC10023 standard for domain sales, tags such as `fmin`, `frnt`, and `flto` are **proprietary extensions used by NameShift**. These extensions are already (partly) interpreted by specialized industry tools, such as **DomainsToolBelt**, to automate the extraction of detailed pricing models. 🔍

### 📊 Tag Definitions

| Tag | Origin | Description | Example |
| :--- | :--- | :--- | :--- |
| `furi` | RFC10023 | **For Sale URI**: The direct URL to the marketplace listing. | `https://buy.nameshift.com/...` |
| `fval` | RFC10023 | **For Sale Value**: The asking price for the domain. | `EUR14999.00` |
| `fcod` | RFC10023 | **For Sale Code**: A unique identifier for the listing. | `NLFS-OTQ0...` |
| `fmin` | NameShift | **Minimum Offer**: The lowest acceptable offer the seller will consider. | `EUR500.00` |
| `frnt` | NameShift | **Rental Price**: The cost to lease the domain monthly. (e.g., `P1M` = Period 1 Month). | `EUR649.95/P1M` |
| `flto` | NameShift | **Lease-to-Own**: Terms for an installment-based purchase agreement. | `EUR1312.00/P1M/P2M/P12M` |

### ⚙️ Technical Implementation
These values are typically hosted on a dedicated subdomain (e.g., `_for-sale.[domain]`). This structure ensures that sales metadata remains organized and can be efficiently queried by automated brokers and valuation tools without interfering with the primary domain's DNS configuration. 🛠️

***

⚠️ **Disclaimer:** *The exact meaning and syntax of the proprietary NameShift tags (fmin, frnt, flto) are not officially documented by the provider. The definitions provided here are based on observed patterns and industry interpretation and should not be treated as official technical documentation.*
