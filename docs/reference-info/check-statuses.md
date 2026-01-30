# Check Statuses

{% table %}

- Status
- Description
- idv
- fav
- iddv
- amlv
- wbv

---

- `created`
- The verification has been created
- ✓
- ✓
- ✓
- ✓
- ✓

---

- `pending`
- You created an attempt and the verification_url is available
- ✓
- ✓
-
-
-

---

- `capture_in_progress`
- The applicant is performing the capture
- ✓
- ✓
-
-
-

---

- `refused`
- The applicant refused to perform the verification
- ✓
- ✓
-
-
-

---

- `quality_checks_in_progress`
- Checkout.com assesses the quality of the submitted assets
-
-
- ✓
-
-

---

- `checks_in_progress`
- Checkout.com performs the security checks for the applicant's verification
- ✓
- ✓
- ✓
- ✓
- ✓

---

- `approved`
- The applicant's verification has been approved
- ✓
- ✓
- ✓
- ✓
- ✓

---

- `declined`
- The applicant's verification had an irregularity
- ✓
- ✓
- ✓
- ✓
- ✓

---

- `retry_required`
- Checkout.com could not perform all of the required checks for the applicant's verification
- ✓
- ✓
- ✓
-
-

---

- `review_required`
- An AML verification case has been opened, you should manually investigate it
-
-
-
- ✓
-

---

- `inconclusive`
- The verification checks were not completed and a retry is no longer available
- ✓
- ✓
- ✓
- ✓
- ✓

{% /table %}
