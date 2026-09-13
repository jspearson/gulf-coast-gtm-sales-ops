# Gulf Coast GTM Co — Sales Ops Portfolio

Synthetic Salesforce Trailhead Playground demonstrating **Sales Ops / RevOps** craft: pipeline hygiene, director-ready dashboards, funnel metrics, and SOQL exception queries.

**Owner:** Joe Pearson ([LinkedIn](https://www.linkedin.com/in/joe-pearson-Salesforce))  
**Org:** Trailhead Playground `Gulf Coast GTM Co` (login monthly so it stays active)

> Honest framing: synthetic data in a Developer / Playground org. The *process* mirrors real Sales Ops work (CRM hygiene, forecast trust, conversion math) — not a claim of Gong/Outreach admin ownership or CPQ.

---

## What’s in the org

| Layer | What’s there |
|---|---|
| Accounts / Contacts | 48 real-sounding companies (Suncoast Mutual, Mangrove Health, Palmetto Freight, …) |
| Opportunities | ~103 opps across stages, TTM closed history, quote dates, risk flags |
| Reps | 5 users (license-capped): Marcus Cole, Priya Shah, Elena Vargas, Jordan Blake, Avery Quinn |
| Leads | 80 leads; **30 converted** for conversion metrics |
| Custom fields | Region, Segment, Product Line, Forecast Risk, Quote Sent / Amount, Competitors, Next Step Last Updated + formulas (Days Open, Days Past Close, Has Next Step, Quote→Close Days, Is Stale) |

---

## Dashboards

### 1. GTM Monday Board — Dir Sales
Filters: **Region**, **Segment**, **Close Date**

Intended story for a Director of Sales:
- Open pipeline $ by stage / by rep
- Hygiene: past-due / missing next step / stale
- Won $ TTM + quote→close motion
- Stuck opps where **Close Date ≤ today** (open)

![Dir Sales board](screenshots/dir-sales-monday-board.webp)

### 2. GTM Lead Engine — Conversion
Filters: **Region**, **Segment**, **Lead Source**

- Leads by status / source / rep
- Converted vs open
- Region / segment slices

![Lead Engine](screenshots/lead-engine-conversion.webp)

---

## SOQL solos

See [`soql/`](soql/) — exception queries a Sales Ops hire should be able to write cold:

1. Stale open opps  
2. Missing next step  
3. Pipeline by stage  
4. Stuck: Close Date ≤ today  
5. Quote→close days on Won  
6. No recent activity (after Tasks/Emails exist)

---

## How a 90-second Loom should go

1. **Problem** — leaders can’t trust the forecast  
2. **Board** — filter Region/Segment, land on hygiene + stuck list  
3. **SOQL** — same exception in Inspector  
4. **Lead engine** — conversion by source (not vanity lead volume)

---

## Data samples

Small CSV snippets under [`data-samples/`](data-samples/) show shape (Account names, OwnerEmail, Region/Segment, Quote fields). Full load files stay private / in the org.

---

## Roadmap / next enrichments

- Activity history on opps (Tasks / Emails / Events) so `LastActivityDate` powers “no touch in 14 days”
- Loss Reason + Push Count (original close date vs current)
- Content Notes on high-risk deals
- Optional standard Quotes object (vs Quote_* fields on Opp)

---

## License

Synthetic demo content for portfolio use. Company names are fictional.
