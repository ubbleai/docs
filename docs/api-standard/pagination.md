# Pagination

List endpoints that return multiple items support pagination.

## Request parameters
You can control pagination using the following optional query parameters:
- `skip` (optional): Number of items to skip (offset). Default: 0
- `limit` (optional): Maximum number of items to return per page. Default: 10

## Navigation methods
You can navigate through pages using either:
1. **Navigation links**: Use the URLs provided in the `_links` object (recommended)
2. **Manual parameters**: Construct your own URLs using `skip` and `limit` query parameters

## Response structure
Paginated responses include the following fields:
- `total_count`: Total number of items available
- `skip`: Number of items skipped (offset)
- `limit`: Maximum number of items returned per page
- `data`: Array of items for the current page
- `_links`: Navigation links object containing:
  - `self`: Link to the current page
  - `next`: Link to the next page (if available)
  - `previous`: Link to the previous page (if available)

```json
{
  "total_count": 42,
  "skip": 10,
  "limit": 10,
  "data": [
    {
      "id": "iatp_tkoi5db4hryu5cei5vwoabr7we",
      "status": "checks_in_progress",
      "created_on": "2017-07-21T17:32:28Z"
      ...
    }
  ],
  "_links": {
    "self": {
      "href": "https://api.ubble.ai/v2/identity-verifications/idv_xxx/attempts"
    },
    "next": {
      "href": "https://api.ubble.ai/v2/identity-verifications/idv_xxx/attempts?skip=20&limit=10"
    },
    "previous": {
      "href": "https://api.ubble.ai/v2/identity-verifications/idv_xxx/attempts?skip=0&limit=10"
    }
  }
}
```
