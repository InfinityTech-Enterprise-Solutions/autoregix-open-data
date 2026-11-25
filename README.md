# EU compliance deadlines and EU product recall statistics

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24538493.svg)](https://doi.org/10.5281/zenodo.24538493)

Open data from [Autoregix](https://autoregix.com), a free reference site on the EU rules that businesses have to meet.

This repository is a weekly copy of the files published on the site. The live files are the source; use them if you need the latest state.

## Files

| File | What it holds | Live address |
|---|---|---|
| `data/deadlines.csv` | About 160 dates on which EU rules for businesses start to apply | https://autoregix.com/data/deadlines.csv |
| `data/deadlines.json` | The same entries as JSON | https://autoregix.com/data/deadlines.json |
| `data/deadlines-en.ics` | The dated entries as all-day calendar events, English | https://autoregix.com/en/deadlines/calendar.ics |
| `data/deadlines-de.ics` | The same calendar in German | https://autoregix.com/de/fristen/calendar.ics |
| `data/recalls.json` | Counts of EU Safety Gate alerts over the last 52 weeks | https://autoregix.com/data/recalls.json |

To follow the deadlines in a calendar, subscribe to the live calendar address instead of importing the file. A subscription picks up new and postponed dates.

## Deadlines

Each entry covers one date under one EU act: product rules, customs, VAT, data protection, the AI Act, sustainability reporting, cybersecurity, employment and platform law.

| Field | Meaning |
|---|---|
| `id` | Stable identifier of the entry |
| `date` | ISO date, empty where no date is fixed yet |
| `status` | `applies` (as adopted), `postponed`, `proposed` (a change is proposed) or `notlaw` (the act is not yet law) |
| `topic` | One of products, trade, tax, privacy, ai, sustainability, cyber, employment, platforms |
| `act` | Name and number of the EU act |
| `celex` | CELEX number of the act |
| `legalText` | Link to the act on EUR-Lex |
| `what`, `who`, `note` | What starts to apply, who is affected, and what was postponed or proposed, in English |
| `whatDe`, `whoDe`, `noteDe` | The same in German |

The human-readable version, with a filter by topic, is at https://autoregix.com/en/deadlines/.

## Recall statistics

Safety Gate is the EU rapid alert system for dangerous non-food products. The file counts alerts for the last 52 weeks:

- `weeks` and `months`: alerts per period, with the leading category and country of origin per week
- `categories`: alerts per product category, with the main risks, origins and laws breached in each
- `origins`, `notifiers`, `risks`, `laws`: alerts per country of origin, notifying country, risk type and law breached

One alert is one notified measure against one product model. It can stand for a handful of items or for many thousands, so the counts show where authorities find problems, not how many units were affected.

The human-readable version is at https://autoregix.com/en/recalls/.

## Licence and credit

The compilation is licensed under [Creative Commons Attribution 4.0](LICENSE) (CC BY 4.0). You may copy, share and adapt it for any purpose if you give credit with a link:

> Source: Autoregix, https://autoregix.com

The recall statistics are compiled from Safety Gate reports of the European Commission. If you use them, name Safety Gate as the original source as well.

## How to cite

Autoregix. EU compliance deadlines and EU product recall statistics. Zenodo. https://doi.org/10.5281/zenodo.24538493

That DOI always points to the latest archived version. Each release also has its own DOI on the Zenodo page, for citing one exact snapshot.

## Accuracy

The deadlines were checked against the legal texts and each entry links to its act. They are information, not legal advice. To report an error, open an issue in this repository.
