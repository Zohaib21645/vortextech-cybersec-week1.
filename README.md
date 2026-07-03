# Vortex Tech Cyber Security Internship — Week 1

## Research the OWASP Top 10 Vulnerabilities

This repository contains my Week 1 submission for the Vortex Tech Cyber Security Internship track. The task was to research five vulnerabilities from the OWASP Top 10, explain each in plain language, walk through how an attacker would exploit it, document a real-world breach caused by it, and give practical developer-facing mitigation steps.

### What's in this repo

| File | Description |
|---|---|
| [`report.pdf`](./report.pdf) | Full 14-page professional report — the primary deliverable, formatted with a table of contents and page numbers. |
| [`report.md`](./report.md) | Same report in Markdown source form (used to generate the PDF). |
| [`README.md`](./README.md) | This file. |

### Vulnerabilities covered

This report uses the **OWASP Top 10:2025** (the current official edition, released early 2026), rather than the older 2021 list, and explicitly maps between the two so the research stays relevant either way.

1. **A01:2025 — Broken Access Control** — case study: First American Financial Corp. (2019), ~885M records exposed via an IDOR flaw.
2. **A02:2025 — Security Misconfiguration** — case study: Capital One (2019), ~106M records exposed via a misconfigured WAF and SSRF.
3. **A04:2025 — Cryptographic Failures** — case study: Adobe (2013), ~153M accounts exposed after passwords were encrypted instead of hashed.
4. **A05:2025 — Injection** — case study: Equifax (2017), ~147.9M individuals exposed via an unpatched Apache Struts code-injection flaw.
5. **Cross-Site Scripting (XSS)**, treated as a specialized case of Injection — case study: the Samy Worm on MySpace (2005), the fastest-spreading XSS worm of its time.

Each section covers: what the vulnerability is, how it's exploited, the real-world breach, and concrete prevention/mitigation steps.

### How to "run" this

There's no code to execute — this is a research and documentation deliverable. To view the report:

- Open [`report.pdf`](./report.pdf) directly, **or**
- Read [`report.md`](./report.md) in any Markdown viewer (including directly on GitHub).

To regenerate the PDF from the Markdown source locally (optional):

```bash
pandoc report.md -o report.pdf \
  --pdf-engine=xelatex \
  -V geometry:margin=1in \
  -V fontsize=11pt \
  -V colorlinks=true \
  --toc --toc-depth=2
```

### Methodology

Research was conducted using the official OWASP Top 10 documentation (owasp.org), cross-referenced against independent security vendor analyses, and each breach case study was verified against multiple public, reputable sources (incident disclosures, investigative journalism, and post-mortem write-ups). See the References section at the end of `report.md` / `report.pdf` for the full source list.

### Author

**Muhammad Zohaib Shabbir**
Track: Cyber Security Internship
Vortex Tech Internship Program 2026
