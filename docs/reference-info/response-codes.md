# Response Codes

{% admonition type="warning" %}
Please note that we consider adding new response codes as backward compatible. You should then build you business rules based on the status and use response codes as additional information, rather than use response codes as required information.
{% /admonition %}


## Check status: `approved`

{% table %}

- Code
- Summary
- Description
- idv
- certified idv
- fav
- iddv
- wbv

---

- 10000
- approved
- The verification has been approved
- ✓
- ✓
- ✓
- ✓
- ✓

{% /table %}

## Check status: `retry_required`

{% table %}

- Code
- Summary
- Description
- idv
- certified idv
- fav
- iddv

---

- **Applicant engagement issue**
-
-
-
-
-
-

---

- 61101
- applicant_never_started
- Applicant was probably not redirected to the application and never started the flow
- ✓
- ✓
- ✓
-

---

- 61111
- applicant_not_ready
- Applicant explicitly stated that they wanted to perform the identity verification later by clicking on the dedicated button
- ✓
- ✓
- ✓
-

---

- 61112
- applicant_no_document
- Applicant explicitly stated that they did not have their document with them by clicking on the dedicated button
- ✓
- ✓
-
-

---

- 61113
- camera_access_refused
- Applicant did not give access to the camera despite the dedicated instructions
- ✓
- ✓
- ✓
-

---

- 61121
- applicant_drop
- Applicant left the process before the capture phase and the verification URL expired (by default the expiration time is 15 minutes)
- ✓
- ✓
- ✓
-

---

- **Video streaming issue**
-
-
-
-
-
-

---

- 61201
- connection_insufficient
- Applicant did not have a sufficient connection to perform the capture
- ✓
- ✓
- ✓
-

---

- 61202
- browser_not_supported
- Applicant's browser was not suitable for video streaming
- ✓
- ✓
- ✓
-

---

- 61203
- camera_not_found
- Applicant's device did not have any camera
- ✓
- ✓
- ✓
-

---

- 61911
- corrupted_videos
- The received videos cannot be played
- ✓
- ✓
- ✓
-

---

- 61205
- sms_not_received
- DEPRECATED
-
-
-
-

---

- **Document capture issue**
-
-
-
-
-
-

---

- 61301
- document_blurry
- Applicant's document is too blurry (mostly due to too much movement but if this error persists the camera quality might be at fault)
- ✓
- ✓
-
- ✓

---

- 61302
- document_lighting_issue
- Applicant performed the document capture under poor lighting conditions
- ✓
- ✓
-
- ✓

---

- 61303
- document_not_in_color
- Applicant's document is not captured in color
-
-
-
- ✓

---

- 61310
- document_front_not_captured
- Applicant has not captured the front of the document
- ✓
- ✓
-
- ✓

---

- 61311
- document_back_not_captured
- Applicant has not captured the back of the document
- ✓
- ✓
-
- ✓

---

- 61312
- document_partially_hidden
- Applicant hides part of the document
- ✓
- ✓
-
- ✓

---

- 61313
- document_not_tilted
- Applicant did not present a dynamic view of the document
- ✓
- ✓
-
-

---

- 61314
- document_challenge_timeout
- Applicant failed to meet the document challenge and the verification expired
-
- ✓
-
-

---

- 61315
- document_barcode_unreadable
- DEPRECATED
-
-
-
-

---

- **Secondary document capture issue**
-
-
-
-
-
-

---

- 61321
- secondary_document_blurry
- Applicant's secondary document is too blurry (mostly due to too much movement but if this error persists the camera quality might be at fault)
- ✓
-
-
-

---

- 61322
- secondary_document_lighting_issue
- Applicant performed the secondary document capture under poor lighting conditions
- ✓
-
-
-

---

- 61330
- secondary_document_front_not_captured
- Applicant has not captured the front of the secondary document
- ✓
-
-
-

---

- 61331
- secondary_document_back_not_captured
- Applicant has not captured the back of the secondary document
- ✓
-
-
-

---

- 61332
- secondary document_partially_hidden
- Applicant hides part of the secondary document
- ✓
-
-
-

---

- 61333
- secondary_document_not_tilted
- Applicant did not present a dynamic view of the secondary document
- ✓
-
-
-

---

- **Face capture issue**
-
-
-
-
-
-

---

- 61401
- face_video_blurry
- Applicant's video of their face is too blurry (mostly due to too much movement but if this error persists the camera quality might be at fault)
- ✓
- ✓
-
-

---

- 61402
- face_video_lighting_issue
- Applicant performed their identity verification under poor lighting conditions
- ✓
- ✓
-
-

---

- 61410
- face_not_captured
- Applicant has not presented a face
- ✓
- ✓
- ✓
-

---

- 61411
- face_partially_hidden
- Applicant did not show the full front view of their face
- ✓
- ✓
- ✓
-

---

- 61412
- face_not_turned
- Applicant did not move to prove the liveness
- ✓
- ✓
- ✓
-

---

- 61413
- face_challenge_timeout
- Applicant failed to meet the face challenge and the verification expired
-
- ✓
-
-

---

- 61414
- various_faces_detected
- DEPRECATED
-
-
-
-

---

- **Other issues**
-
-
-
-
-
-

---

- 61901
- internal_error
- An internal error prevents us from completing the verification, we do our best to reduce the occurrence of this case
- ✓
- ✓
- ✓
- ✓

{% /table %}

## Check status: `declined`

{% table %}

- code
- summary
- Description
- idv
- certified idv
- fav
- iddv
- wbv

---

- **Document non compliant**
-
-
-
-
-
-
-

---

- 62101
- document_expired
- Applicant presented an expired document
- ✓
- ✓
-
- ✓
-

---

- 62102
- document_not_accepted
- Applicant presented a document which is not accepted
- ✓
- ✓
-
- ✓
-

---

- 62103
- document_damaged
- Applicant has submitted a damaged document
- ✓
- ✓
-
- ✓
-

---

- 62104
- unsupported_alphabet
- Applicant has submitted a document containing an unsupported alphabet
- ✓
- ✓
-
- ✓
-

---

- 62201
- document_photocopy
- Applicant presented a photocopy of the document
- ✓
- ✓
-
- ✓
-

---

- 62202
- document_screenshot
- Applicant presented the document on a screen
- ✓
- ✓
-
- ✓
-

---

- **Secondary document non compliant**
-
-
-
-
-
-
-

---

- 62121
- secondary_document_expired
- Applicant presented an expired secondary document
- ✓
-
-
-
-

---

- 62122
- secondary_document_not_accepted
- Applicant presented an secondary document which is not accepted
- ✓
-
-
-
-

---

- 62123
- secondary_document_damaged
- Applicant has submitted a damaged secondary document
- ✓
-
-
-
-

---

- 62124
- secondary_document_unsupported_alphabet
- Applicant presented an secondary document containing an unsupported alphabet
- ✓
-
-
-
-

---

- 62221
- secondary_document_photocopy
- Applicant presented a photocopy of the secondary document
- ✓
-
-
-
-

---

- 62222
- secondary_document_screenshot
- Applicant presented the secondary document on a screen
- ✓
-
-
-
-

---

- **Identity fraud**
-
-
-
-
-
-
-

---

- 62301
- document_counterfeit
- Applicant has submitted a counterfeit or falsification
- ✓
-
-
- ✓
-

---

- 62302
- document_stolen
- Applicant presented a document declared as stolen or lost
- ✓
-
-
- ✓
-

---

- 62303
- document_swap
- Applicant presented the front and back of two different documents
- ✓
-
-
-
-

---

- 62331
- secondary_document_counterfeit
- Applicant has submitted a counterfeit or falsification as an secondary document
- ✓
-
-
-
-

---

- 62332
- secondary_document_stolen
- Applicant presented an secondary document declared as stolen or lost
- ✓
-
-
-
-

---

- 62333
- secondary_document_swap
- Applicant presented the front and back of two different documents
- ✓
-
-
-
-

---

- 62334
- secondary_document_mismatch
- Applicant is not the owner of the secondary document
- ✓
-
-
-
-

---

- 62304
- face_mismatch
- Applicant does not match the photograph of the document
- ✓
-
-
-
-

---

- 62305
- face_not_live
- Applicant has presented a photography or a video of someone else's face on a screen or on a physical medium
- ✓
-
- ✓
-
-

---

- 62306
- face_alteration
- Applicant has altered their appearance
- ✓
-
- ✓
-
-

---

- 62307
- asset_digital_alteration
- Applicant has digitally altered the assets
- ✓
-
- ✓
- ✓
-

---

- 62321
- face_face_mismatch
- Applicant of the face authentication is not the one who performed the identity verification
-
-
- ✓
-
-

---

- 62399
- generic_fraud
- Replace all other Identity Fraud codes for certified identity verification
-
- ✓
-
-
-

---

- **Prohibited behavior**
-
-
-
-
-
-
-

---

- 62401
- declared_identity_mismatch
- Applicant's identity does not match with the expected one
- ✓
- ✓
-
- ✓
-

---

- 62402
- suspicious_device
- Applicant used a device that has been technically altered
- ✓
- ✓
- ✓
-
-

---

- 62403
- consent_unclear
- Applicant seems to have performed the capture against their will
- ✓
- ✓
- ✓
-
-

---

- 62404
- multiple_documents
- Applicant show multiple documents
- ✓
- ✓
-
- ✓
-

---

- 62405
- known_fraudulent_face
- The applicant has recently performed a fraud attempt
- ✓
- ✓
- ✓
-
-

---

- **Website compliance issues**
-
-
-
-
-
-
-

---

- 72381
- missing_terms_and_conditions
- T&Cs are missing
-
-
-
-
- ✓

---

- 72382
- missing_privacy_policy
- Privacy Policy is missing
-
-
-
-
- ✓

---

- 72383
- missing_refund_policy
- Refund Policy is missing
-
-
-
-
- ✓

---

- 72384
- missing_customer_service_contact
- Customer Service contact is missing
-
-
-
-
- ✓

---

- 72385
- missing_legal_entity_name
- Legal entity name is missing
-
-
-
-
- ✓

---

- 72386
- missing_legal_entity_address
- Legal entity address is missing
-
-
-
-
- ✓

---

- 72387
- missing_country_of_incorporation
- Country of Incorporation is missing
-
-
-
-
- ✓

{% /table %}

## Check status: `inconclusive`

Meaning the verification checks could not be completed

{% table %}

- Code
- Summary
- Description
- idv
- certified idv
- fav
- iddv
- wbv

---

- **Medium issue**
-
-
-
-
-
-
-

---

- 71181
- url_does_not_exist
- URL does not exist
-
-
-
-
- ✓

---

- 71182
- website_not_available
- Website could not be reached
-
-
-
-
- ✓

---

- **Other issues**
-
-
-
-
-
-
-

---

- 71901
- internal_error
- An internal error prevents us from completing the verification, we do our best to reduce the occurrence of this case
-
-
-
-
- ✓

{% /table %}

## Verification status: `refused`

{% table %}

- Code
- Summary
- Description
- idv
- certified idv
- fav
- iddv

---

- 63001
- applicant_refusal
- Applicant explicitly refused to do the verification process by clicking on the dedicated button.
- ✓
- ✓
- ✓
-

{% /table %}

## Verification status: `pending` or `inconclusive`

{% table %}

- Code
- Summary
- Description
- idv
- certified idv
- fav
- iddv

---

- 64001
- forcibly_closed
- You have created a new attempt or the verification has been anonymised while the attempt was still valid
- ✓
- ✓
- ✓
- ✓

{% /table %}
