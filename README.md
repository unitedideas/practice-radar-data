# Behavioral-health NPI data for credentialing and provider-enrollment research

Practice Radar publishes weekly, versioned evidence for newly enumerated Type 2 behavioral-health organizations in the CMS National Plan and Provider Enumeration System (NPPES). Credentialing firms, provider-enrollment consultants, medical-billing teams, and healthcare vendors can use the organization signal to build a current research queue.

## Current edition receipt

The 2026-07-13 through 2026-07-19 edition screened 2,631 newly enumerated Type 2 organizations and selected 450 after the disclosed behavioral-health filter.

| State evidence page | Code | Selected organizations |
| --- | --- | ---: |
| California | CA | 36 |
| Texas | TX | 35 |
| Florida | FL | 26 |
| North Carolina | NC | 24 |
| Washington | WA | 18 |

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

## Get every current row

- [Buy the current national CSV for **$19 once**](https://buy.stripe.com/6oUdR29Ue7rDg80fLd6oo0i?client_reference_id=github_practice_radar_data&utm_source=github&utm_medium=repository&utm_campaign=practice_radar_edition) for private browser delivery with no Apify account, subscription, or renewal. The purchased edition does not update.
- Use the [hosted Apify Actor](https://apify.com/actablesite/new-behavioral-health-practices-actor) when the full edition belongs in an automated workflow. It charges one **$9 event** plus bounded buyer-paid platform usage and runs only after the latest CMS archive passes parsing, validation, and record-count gates.

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
