# Choose your scenario

To choose the scenario you want to test, you will have to [create an applicant](#tag/Applicants/operation/create_applicant) and set the `external_applicant_id` value to one of the values described in the table below.

  {% table %}

  - #
  - Scenario
  - external_applicant_id

  ---

  - 1
  - Approved verification
  - `eaplt_10000000000000000000000000`

  ---

  - 2
  - Approved verification on retry after capture aborted
  - `eaplt_61XXXA10000000000000000000`

  ---

  - 3
  - Approved verification on retry after checks inconclusive
  - `eaplt_61XXXI10000000000000000000`

  ---

  - 4
  - Declined verification
  - `eaplt_62XXX000000000000000000000`

  ---

  - 5
  - Declined verification on retry after capture aborted
  - `eaplt_61XXXA62XXX000000000000000`

  ---

  - 6
  - Declined verification on retry after checks inconclusive
  - `eaplt_61XXXI62XXX000000000000000`

  {% /table %}   

- Replace 61XXX with any of the response codes starting with 61, that you would like to test for.
- Replace 62XXX with any of the response codes starting with 62, that you would like to test for.

For example, if you would like to test a "Declined" scenario with `62201`, then set the value to `eaplt_62201000000000000000000000`.      

Make a note of the applicant `id` value in the response. You'll need it to create verifications later.
