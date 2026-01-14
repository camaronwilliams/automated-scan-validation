# Automated Web App Scan + Manual Validation (DAST)

## Overview
This project demonstrates an application security workflow combining automated dynamic scanning (DAST) with manual validation to confirm exploitability and reduce false positives. It mirrors a pre-production security certification process used by application security teams.

I executed an automated DAST scan using OWASP ZAP, preserved raw scanner output, performed analyst triage, manually validated findings, and produced a risk-adjusted security review aligned with pre-production certification workflows.

## Target / Environment
- Target: OWASP Juice Shop (local lab)
- URL: http://localhost:3000
- Host: Personal MacBook (local-only)
- Deployment: Docker
- Tools: OWASP ZAP (automated scan), Burp Suite (manual validation), browser dev tools

## Scope
- Automated crawl + active scan (OWASP ZAP)
- Triage: risk/confidence review, deduplication, prioritization
- Manual validation: confirm/deny top findings with request/response evidence
- Final output: risk-adjusted report + remediation guidance

## Repo Contents
- `scans/zap/` – exported scan outputs (HTML, JSON, screenshots)
- `triage/findings-triage.md` – findings triage table
- `validation/` – manual validation writeups (confirmed/false positive)
- `report/Final_Security_Review.md` – final report (risk-adjusted)
- `evidence/` – screenshots + redacted requests/responses

## How to Run Juice Shop (Lab)
```bash
docker run --rm -p 3000:3000 bkimminich/juice-shop
