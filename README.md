# IDX Content Vocabulary

The canonical controlled vocabulary for classifying corporate website content across the IDX portfolio.

## The vocabulary

**105 nodes** across **5 domains** and **27 subdomains**, each with a governed definition, AEO priority rating, freshness threshold, and provenance source.

| Code | Domain | Subdomains | Nodes |
|------|--------|------------|-------|
| **E** | ESG | 5 | 27 |
| **I** | Investor Relations | 5 | 25 |
| **C** | Corporate Communications | 6 | 20 |
| **T** | Careers and Talent | 5 | 18 |
| **B** | Brand and Product | 6 | 15 |

## Files

| File | Format | Purpose |
|------|--------|---------|
| [`spine.json`](spine.json) | JSON | Machine-readable canonical source |
| [`pinakes.yaml`](pinakes.yaml) | YAML | Human-readable reference with full hierarchy |
| [`governance.md`](governance.md) | Markdown | Governance rules and change process |

## Node structure

Every node carries six fields:

```yaml
- id: E1.1                    # Stable identifier (never changes)
  name: Climate strategy       # Human-readable label
  definition: "..."            # One-sentence scope statement
  aeo_priority: Critical       # Critical | High | Standard
  freshness: 12 mo             # Maximum acceptable content age
  source: External             # External | Portfolio | Market
```

**ID format:** `{domain}{subdomain}.{node}` — e.g. `I3.1` = Investor Relations, subdomain 3 (Strategy And Equity Story), node 1 (Corporate strategy).

## Domains at a glance

### E — ESG (27 nodes)

| Sub | Subdomain | Nodes | Example |
|-----|-----------|-------|---------|
| E1 | Climate And Energy | 6 | E1.1 Climate strategy and targets |
| E2 | Environment And Nature | 5 | E2.1 Nature and biodiversity |
| E3 | Social And People | 7 | E3.1 Workforce health, safety and wellbeing |
| E4 | Governance And Integrity | 5 | E4.4 Supply chain and suppliers |
| E5 | Reporting And Performance | 4 | E5.2 Framework alignment |

### I — Investor Relations (25 nodes)

| Sub | Subdomain | Nodes | Example |
|-----|-----------|-------|---------|
| I1 | Financial Results And Reporting | 5 | I1.1 Results and financial performance |
| I2 | Capital And Returns | 4 | I2.1 Capital allocation |
| I3 | Strategy And Equity Story | 4 | I3.1 Corporate strategy |
| I4 | Governance And Risk | 6 | I4.1 Board composition and effectiveness |
| I5 | Investor Engagement | 6 | I5.1 Investor events and presentations |

### C — Corporate Communications (20 nodes)

| Sub | Subdomain | Nodes | Example |
|-----|-----------|-------|---------|
| C1 | Press Office Output | 4 | C1.1 Press releases and announcements |
| C2 | Corporate Narrative | 4 | C2.3 Leadership and executive team |
| C3 | Reputation And Issues | 4 | C3.1 Crisis and issues communication |
| C4 | Campaigns And Thought Leadership | 4 | C4.2 Thought leadership and opinion |
| C5 | Digital Presence | 3 | C5.1 Social media presence |
| C6 | Stakeholder Operations | 1 | C6.1 Supplier engagement and procurement |

### T — Careers and Talent (18 nodes)

| Sub | Subdomain | Nodes | Example |
|-----|-----------|-------|---------|
| T1 | Job Search And Application | 4 | T1.1 Job listings and search |
| T2 | Employee Value Proposition | 4 | T2.1 Why work here |
| T3 | Culture And Inclusion | 4 | T3.1 Culture and ways of working |
| T4 | Purpose And Impact In Work | 3 | T4.3 Innovation and technology careers |
| T5 | Employer Presence And Reputation | 3 | T5.1 Life at the organisation |

### B — Brand and Product (15 nodes)

| Sub | Subdomain | Nodes | Example |
|-----|-----------|-------|---------|
| B1 | Brand Portfolio | 3 | B1.1 Brand portfolio overview |
| B2 | Products And Services | 3 | B2.1 Product and service catalogue |
| B3 | Market And Customer | 3 | B3.1 Markets and geographies |
| B4 | Brand Governance | 3 | B4.1 Brand guidelines and identity |
| B5 | Sector-Specific Brand Expression | 2 | B5.1 Consumer brand content |
| B6 | Operational Presence | 1 | B6.1 Operations and business units |

## Source provenance

Each node records how its inclusion was justified:

- **External** (93 nodes) — Grounded in a regulatory framework or recognised external standard (CSRD, ISSB, UK Corporate Governance Code, CIPD, etc.)
- **Portfolio** (5 nodes) — No external standard covers this concept; IDX is the originating authority, grounded in portfolio traffic evidence
- **Market** (7 nodes) — Market convention or best practice without formal regulatory backing

The five portfolio-derived nodes are the vocabulary's original contributions:
- E2.1 Nature and biodiversity
- E2.4 Plastics and packaging
- E3.5 Livelihoods
- E3.6 Consumer and stakeholder engagement
- E4.4 Supply chain and suppliers

## Live explainer

Interactive spine explorer: **https://mb-uc.github.io/idx-spine/**

## Governance

See [`governance.md`](governance.md) for the three-question test, change process, and controller rules.

## Schema owner

Simon Heath, Principal Consultant, IDX
