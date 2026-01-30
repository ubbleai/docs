# Error handling

For HTTP error codes 400 and 422 the response body will contain:
- `error_type`: a short description code
- `error_codes`: a list of more detailed codes

Error codes and error types can be formatted as follows:
- `{error}`
- `{target/attribute}__{error}`
- `{nested_object}__{object_attribute}__{error}`

```json
{
  "error_type": "invalid_request",
  "error_codes": [
    "birth_date__invalid_format",
    "first_name__required",
    "phone_number__country_code__invalid"
  ]
}
```
