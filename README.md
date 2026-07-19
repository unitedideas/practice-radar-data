# Behavioral-health NPI data for credentialing and provider-enrollment research

Practice Radar publishes weekly, versioned evidence for newly enumerated Type 2 behavioral-health organizations in the CMS National Plan and Provider Enumeration System (NPPES). Credentialing firms, provider-enrollment consultants, medical-billing teams, and healthcare vendors can use the organization signal to build a current research queue.

## Current edition receipt

The 2026-07-06 through 2026-07-12 edition screened 2,722 newly enumerated Type 2 organizations and selected 486 after the disclosed behavioral-health filter.

| State evidence page | Code | Selected organizations |
| --- | --- | ---: |
| California | CA | 49 |
| Texas | TX | 36 |
| Florida | FL | 37 |
| North Carolina | NC | 30 |
| Washington | WA | 9 |

These counts measure NPI enumeration during the stated period, not practice openings or buying intent.

## What the signal can and cannot do

The feed supplies a current organization entity, Type 2 NPI, published location, telephone, taxonomy, enumeration date, and source receipt. It is not a credentialing file: NPI enumeration does not establish licensure, CAQH status, payer enrollment, panel participation, active operation, service availability, need, decision authority, or buying intent. Verify every row before operational use or contact.

## Inspect the current edition

- [`public/summary.json`](public/summary.json) is the machine-readable source and build receipt, including the measurement period, source-file hashes, screened and selected counts, state distribution, taxonomy scope, and limitations.
- [`public/sample.csv`](public/sample.csv) and [`public/sample.json`](public/sample.json) contain the same 15 public sample rows.
- [`datapackage.json`](datapackage.json) describes the public CSV with a portable tabular-data schema.
- The [no-token GitHub Actions preview](https://github.com/marketplace/actions/new-behavioral-health-practices-weekly) downloads this same current sample, supports state filters, and writes a source-linked workflow summary without an account or charge.
- The [free 15-row Apify preview](https://console.apify.com/create-task-from-example/mWSjyRgMOUIk9IiJr) duplicates the deterministic current sample into the buyer's own Apify account without a full-edition charge.
- Credentialing and provider-enrollment teams can use the [credentialing-specific free preview](https://console.apify.com/create-task-from-example/Z22XvAAbiUlbxnDCw), which preserves the same source fields and verification limits while starting with that workflow's filters.
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
