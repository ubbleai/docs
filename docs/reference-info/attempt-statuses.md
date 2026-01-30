# Attempt Statuses

{% table %}

- Status
- Description
- idv
- fav
- iddv

---

- `pending_redirection`
- The attempt has been created and applicant can be redirected
- ✓
- ✓
-

---

- `capture_in_progress`
- The attempt has been started by the applicant
- ✓
- ✓
-

---

- `capture_aborted`
- The applicant terminated the capture without completing it
- ✓
- ✓
-

---

- `capture_refused`
- The applicant refused to perform the identity verification
- ✓
- ✓
-

---

- `expired`
- The link expired without applicant being redirected to the web application, please note the default expiration time is 15 minutes
- ✓
- ✓
-

---

- `quality_checks_in_progress`
- The assets have been submitted and we are assessing their quality
-
-
- ✓

---

- `quality_checks_aborted`
- The assets provided are not of good enough quality to perform the verification
-
-
- ✓

---

- `checks_in_progress`
- We have all assets required and we are performing checks
- ✓
- ✓
- ✓

---

- `completed`
- We completed the checks. Verification is closed
- ✓
- ✓
- ✓

---

- `checks_inconclusive`
- The assets provided by the applicant did not allow us to perform the checks
- ✓
- ✓
- ✓

---

- `terminated`
- You created a new attempt, the previous one was forcibly closed
- ✓
- ✓
- ✓

{% /table %}
