# Practice Radar data

Weekly, versioned evidence for newly enumerated Type 2 behavioral-health organizations in the CMS National Plan and Provider Enumeration System (NPPES).

## Inspect the current edition

- [`public/summary.json`](public/summary.json) is the machine-readable source and build receipt, including the measurement period, source-file hashes, screened and selected counts, state distribution, taxonomy scope, and limitations.
- [`public/sample.csv`](public/sample.csv) and [`public/sample.json`](public/sample.json) contain the same 15 public sample rows.
- [`datapackage.json`](datapackage.json) describes the public CSV with a portable tabular-data schema.
- The [free current-edition explorer](https://actablesite.com/new-behavioral-health-practices) renders the receipt, all nonzero state counts, taxonomy scope, and sample without an account.

The [full Practice Radar feed](https://actablesite.com/practice-radar) is a $39/month national CSV subscription refreshed weekly. It adds every selected row plus published practice address, telephone, fax, authorized-official, enumeration-date, and taxonomy fields. Purchase is never automatic; the product page shows delivery, renewal, cancellation, support, and terms before checkout.

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
