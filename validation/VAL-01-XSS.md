# VAL-01: XSS (Candidate) Manual Validation

## Scanner Alert
Reflected XSS (candidate)

## Endpoint
- URL: http://localhost:3000/search?q=...
- Method: GET

## Validation Method
- Reproduced the request through proxy to observe where user-controlled input is reflected in the response.
- Determined reflection context (HTML body / attribute / script / DOM).
- Checked for output encoding/sanitization.

## Result
- Status: ⚠️ Pending / ✅ Confirmed / ❌ False Positive (update after test)
- Evidence saved to: `evidence/requests/` and `evidence/screenshots/`

## Impact (if confirmed)
Could enable client-side code execution in victim’s browser, leading to session/account abuse depending on cookie/session protections and app actions.

## Remediation
- Apply contextual output encoding
- Sanitize untrusted input when rich text is required
- Add CSP (defense-in-depth)
