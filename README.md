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
<img width="813" height="597" alt="Screenshot 2026-01-13 at 11 10 37 PM" src="https://github.com/user-attachments/assets/94e2c4ec-7adc-4305-a2a7-9f0ef969241f" />
<img width="809" height="613" alt="Screenshot 2026-01-13 at 11 13 42 PM" src="https://github.com/user-attachments/assets/bed22c13-c9de-40cd-9d36-1d571e3c7dba" />
<img width="816" height="619" alt="Screenshot 2026-01-13 at 11 21 10 PM" src="https://github.com/user-attachments/assets/e29880d9-0093-4bd7-b00d-6f4436d45d5f" />
<img width="824" height="605" alt="Screenshot 2026-01-13 at 11 21 23 PM" src="https://github.com/user-attachments/assets/6d390cb5-1f92-448c-aca8-5b67dedb903f" />
<img width="806" height="611" alt="Screenshot 2026-01-13 at 11 21 30 PM" src="https://github.com/user-attachments/assets/b3519376-323c-4426-95e0-025579426ca3" />

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
