# utubei/v1
## Method and Values:
Method: `GET`

Possible Values: /v1/#{`followers`, `logo`, `banner`, `legacy_id`, `c`}

### Description:
The `/v1/` endpoint can be used to return specific data from any channel or all data when no values are requested.

If no query is specified, no data will be returned. A 'reqwestFailed' will be displayed.

The refresh request button returns all data ordered by the UiD system implemented.

This endpoint can also return data by search query.
`/v1/#followers=6` will return the first channel found with 100 followers.

Querying by `logo` returns the first channel with similar logo data to that queried.

Querying by `banner` returns the first channel that uses that banner.

Querying by `followers`, `logo` or `banner` is broken, so it is not recommended.

Querying by `legacy id` or `channel` return **one** specific channel, and all it's data. `/v1/#channel=CKStudios2018` - `/v1/#legacy_id='legacy id'`

**The legacy id system is currently deprecated, and will be decommissioned soon.**

#### To Note:
Everything in this doc was written to query with `#` (hash), and can only be queried like so.

Queries are also structured following Firefox's standard of adding a `/` before a query, but on Chromium based browsers you can directly access endpoints with `/v1#`.
