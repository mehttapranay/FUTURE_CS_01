# FUTURE_CS_01
# Vulnerability Assessment Report — testaspnet.vulnweb.com

## Overview
This repository contains a passive (read-only) vulnerability assessment of the publicly accessible demo website **testaspnet.vulnweb.com**, completed as part of Future Interns' Cyber Security Task 1 (2026).

## Website Tested
- **Target:** testaspnet.vulnweb.com
- **Type:** Publicly available intentionally-vulnerable demo site (Acunetix ASP.NET test site), used specifically for security testing practice
- **Access level:** No login/authenticated testing performed

## Scope
This assessment was strictly limited to:
- Public-facing pages only
- Passive scanning and observation
- HTTP header inspection
- Configuration analysis

The following were explicitly **out of scope** and were not performed:
- Login bypass
- Exploitation of any kind
- Brute-force or credential attacks
- Denial-of-Service (DoS) testing
- Any activity that could disrupt or harm the target website

## Tools Used
| Tool | Purpose |
|------|---------|
| Nmap 7.94SVN | Passive port scan and service/version detection (`-Pn -F`, `-Pn -sV`) |
| Browser DevTools (Chrome) | Inspection of HTTP request/response headers and cookies |
| OWASP ZAP | Passive vulnerability scanning while manually browsing the site |
| Canva | Report design and layout |

## Methodology Summary
1. Selected a public, intentionally-vulnerable test website appropriate for practice testing
2. Performed a passive Nmap scan to identify open ports and running services
3. Reviewed HTTP response headers via browser DevTools to check for security headers and information disclosure
4. Reviewed cookie configuration for security flags (Secure, HttpOnly, SameSite)
5. Checked robots.txt for unintended exposure
6. Ran OWASP ZAP in passive mode while manually navigating the site to independently validate findings
7. Documented, classified, and prioritized all findings in the final report

## Findings Summary
12 issues were identified, ranging from High to Low risk. The most significant findings relate to the absence of HTTPS and unencrypted transmission of session cookies. Full details, risk classifications, and remediation steps are provided in the report PDF.

| Risk Level | Count |
|------------|-------|
| High | 2 |
| Medium | 5 |
| Low / Low-Medium | 5 |



## Disclaimer
This assessment was conducted for educational purposes on a publicly designated test website. No unauthorized access, exploitation, or disruption of any system was performed at any point during this engagement.

## Author
Pranay Mehtta
