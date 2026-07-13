# Practice Radar data

Weekly, versioned evidence for newly enumerated Type 2 behavioral-health organizations in the CMS National Plan and Provider Enumeration System (NPPES).

## Current edition receipt

The 2026-06-29 through 2026-07-05 edition screened 2,229 newly enumerated Type 2 organizations and selected 423 after the disclosed behavioral-health filter.

| State evidence page | Code | Selected organizations |
| --- | --- | ---: |
| California | CA | 55 |
| Texas | TX | 36 |
| Florida | FL | 30 |
| North Carolina | NC | 30 |
| Washington | WA | 17 |

These counts measure NPI enumeration during the stated period, not practice openings or buying intent.

## Inspect the current edition

- [`public/summary.json`](public/summary.json) is the machine-readable source and build receipt, including the measurement period, source-file hashes, screened and selected counts, state distribution, taxonomy scope, and limitations.
- [`public/sample.csv`](public/sample.csv) and [`public/sample.json`](public/sample.json) contain the same 15 public sample rows.
- [`datapackage.json`](datapackage.json) describes the public CSV with a portable tabular-data schema.
- The [free 15-row Apify preview](https://apify.com/actablesite/new-behavioral-health-practices-actor/examples/new-behavioral-health-practices-free-weekly-preview) duplicates the deterministic current sample into the buyer's own Apify account without a full-edition charge.
- [`public/editions.json`](public/editions.json) indexes dated organization-only receipts and public samples preserved in this repository.

The [hosted Apify Actor](https://apify.com/actablesite/new-behavioral-health-practices-actor) offers a $9 full weekly edition with every validated selected row. Buyer-paid platform usage is separate. The full-edition event is charged only after the latest CMS archive passes parsing, validation, and record-count gates; failed validation does not deliver or charge the full edition.

## Reproducible scope

Each edition starts with the official CMS NPPES weekly V2 file and then:

1. selects newly enumerated Type 2 organizations;
2. removes deactivated records;
3. matches the eight behavioral-health taxonomy codes disclosed in `public/summary.json`; and
4. deduplicates organization, city, and state combinations.

The repository preserves public receipts and samples in Git history. Per-subscriber full editions are encrypted with AES-256-GCM; their filenames and contents do not expose Stripe checkout-session IDs.

## Material limitations

An NPI does not prove licensure, credentialing, active operation, independence, service availability, a newly opened physical practice, demand, or buying intent. Enumeration is the measured event. Verify every record and follow applicable calling, privacy, and marketing rules before contact.

Source: [Centers for Medicare & Medicaid Services, NPPES Data Dissemination](https://download.cms.gov/nppes/NPI_Files.html).
