## 📋 Submission Information

**Name:** Mehmet AŞKIN  
**Email:** mehmetaskn77@gmail.com  
**LinkedIn:** https://www.linkedin.com/in/mehmetaskin/  
**Submission Date:** 2025-11-10

---

## ✅ Deliverables Checklist

Please confirm you've included all required items:

- [✅] **Report** (PDF, max 5 pages)
  - [✅] Section 1: Incident Analysis
  - [✅] Section 2: Architecture Review
  - [✅] Section 3: Response & Remediation
  
- [✅] **Video Presentation** (10-15 minutes)
  - [✅] Link provided in `video_link.md`
  - [✅] Video is accessible (tested in incognito)
  - [✅] Duration is within guidelines

- [ ] **File Structure**
```
  submissions/firstname-lastname/
  ├── report.pdf
  ├── video_link.md
  └── notes.md (optional)
```

---

## 📊 Self-Assessment

**Time spent on this lab:** Approximately ___ hours

**Tools used:**
- Log analysis: excel, python
- Diagrams: draw.io
- Video recording: Snipping Tool

**Confidence level:**
- [✅] Very confident in my analysis
- [ ] Confident but some uncertainties
- [ ] Attempted my best with available knowledge

---

## 🎯 Brief Summary (2-3 sentences)

_Briefly describe your approach and key findings:_

Unusual activities associated with the IP address 203.0.113.45 have been detected. On 15.10.2024 at 06:45:10, a successful login occurred with user ID 1523, followed by unauthorized GET requests using the stolen token jwt_token_1523_stolen to various account_ids from the same IP. The API’s return of 200 OK responses reveals an access control vulnerability. At 09:00:23, phishing emails were sent (opened by user1, user3, and user5); at 09:18:30, a web session was initiated. Starting at 09:20:30, SQL injection attempts (OR 1=1--, DROP TABLE, UNION SELECT) were blocked by the WAF, but an obfuscated variant (/*!50000OR*/) bypassed the protection, resulting in the exfiltration of 892,341 bytes of data via /dashboard/export?format=csv. WAF logs confirm blocking events between 09:20:30–09:22:00, followed by the bypass. According to the security_test_schedule.pdf document, this IP is allocated for an authorized penetration test scheduled for 20–25 October. However, the activities began 5 days early, with initial access occurring via the mobile API application. This discrepancy raises the possibility of an insider threat or compromise of the pentest infrastructure. Consequently, the incident cannot be classified as part of the planned test; it constitutes a genuine security breach.

---

## 🔍 Key Findings Highlight

**Main attack vectors identified:**
1. IDOR
2. SQL Injection
3. Phishing

**Most critical vulnerability:**
Most critical vulnerability: JWT token theft + lack of authorization control + data exfiltration with SQLi.

**Top recommendation:**
Cancellation of all active JWT tokens, strengthening of access control mechanism and updating of WAF rules with OWASP CRS + SQLi bypass detection.

---

## 💭 Challenges & Learnings

**What was most challenging?**
[The mismatch of timestamps in the logs and the suspicion that a penetration test scheduled for a later date may have been executed earlier.]

**What did you learn?**
[Without reaching a firm conclusion, I learned to go through the entire incident from start to finish again to check for missing pieces, and that excessive stress negatively affects our ability to spot issues like this.]

**What would you do differently?**
[I would include the time zone for the timestamps in the report and logs, specifying either UTC or UTC+3.]

---

## 📝 Additional Notes _(optional)_

Any context, assumptions, or additional information you'd like evaluators to know:

[This analysis was based on log data from API, web, email, and WAF sources, cross-referenced with the documented security test schedule. While IP ranges and test account identifiers indicated that some activity aligned with planned penetration testing, the critical factor was that the suspicious access involving user ID 1523 occurred outside the scheduled testing window. This suggests that the activity cannot be categorized as part of the authorized assessment. Additionally, the successful WAF bypass and subsequent data exfiltration highlight that the access control and input validation mechanisms require immediate remediation. Some assumptions were made regarding time zone normalization due to inconsistencies in timestamp formats across log sources. The conclusions and recommendations are based on the correlation of available evidence, and further forensic investigation may provide additional clarity on the threat origin.]

---

## ⚖️ Declaration

I declare that:
- [✅] This work is entirely my own
- [✅] I have not copied from other submissions or answer keys
- [✅] I have not modified the provided log files
- [✅] All sources and tools are properly attributed
- [✅] I understand plagiarism results in disqualification

**Signature:** [Mehmet]  
**Date:** [2025-11-10]

---

## 🚀 Ready for Review

By submitting this PR, I confirm that my work is complete and ready for evaluation.

---

_Thank you for your submission! Our team will review it within 1 week._
