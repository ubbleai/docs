# Set up an initial risk scoring 

You can get an initial risk scoring based on a model that you can customize in the ComplyAdvantage dashboard. 

The applicant will then be scored before the AML verification has been performed. The result of this scoring will be available as a `risk_level` in the results and can be one of `LOW`, `MEDIUM`, `HIGH` or `PROHIBITED`.

If the risk level is `PROHIBITED`, the AML verification is not performed and the `status` is declined. If the risk level is `LOW`, `MEDIUM` or `HIGH`, the AML verification will be performed and the results will depend on raised alerts. See below for more details.
