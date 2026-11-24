# Krsko Studio

An open-source, browser-local workspace for independent photographers, videographers and other freelancers. Manage jobs, prepare invoice drafts, review a quarter or custom date range, and export deadlines to a calendar.

Created by Adrián Krško from his own freelance workflow. This is an early prototype; there are no claims of established adoption or community traction. The current interface is in Slovak.

## Run locally

Requires Python 3, with no package installation or build step:

```sh
python3 -m http.server 8765 --directory .
```

Open http://localhost:8765 in a modern browser.

## Available now

- Jobs: add, edit, search, filter by stage, group by client and review deadlines.
- Browser-local persistence and JSON backup / restore, including invoices and business profile.
- Invoice drafts from jobs, client registration and VAT fields, references and payment terms.
- Price including/excluding VAT; cent rounding; manual VAT selection; immutable issued snapshots and a paid flag.
- Browser print / Save as PDF. No automatic email delivery.
- Current quarter, previous quarter, year or inclusive custom date range, by invoice date or supply date.
- Separate issued, outstanding and draft totals; CSV export with unknown tax amounts left blank.
- One-time iCalendar (.ics) export of active job deadlines, using stable event IDs.
- Fictional starter jobs. No real client records are distributed with this code.

## Data and accounting limits

All operational records stay in this browser's localStorage. They are not synced between devices or backed up on a server. Export backups regularly and keep them private. Publishing the source does not publish the records stored in your existing browser.

Invoice numbering is local to this browser. Do not issue invoices from parallel installations using the same number series. Issued records cannot be edited in this prototype; corrective documents must currently be handled outside it. A manually marked paid invoice has no payment timestamp; reports are not cash-basis accounting.

Krsko Studio does not determine VAT treatment, filing deadlines, invoice deadlines or country-specific legal compliance. A quarter is a reporting filter, not a statement of a universal tax rule. CSV exports are review material, not a tax return; nothing is submitted to tax authorities. Confirm tax treatment and mandatory information before issuing an invoice.

## Planned, not implemented

See [ROADMAP.md](ROADMAP.md): multi-device storage, reviewed Gmail intake, Google Calendar sync, configurable country-specific reminders and optional AI assistance. There is currently no Gmail OAuth connection, background automation, LLM/API call or tax-authority integration.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Bug reports and small, useful contributions are welcome. Use fictional records in examples and screenshots.

## License

MIT — see [LICENSE](LICENSE).
