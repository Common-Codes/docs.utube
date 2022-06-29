# utubei/v1
## Method and Values:
Method: `GET`

Possible Values: /v1/#{`followers`, `logo`, `banner`, `legacy_id`, `c`}

### Description:
The `v1` endpoint can be used to return specific data from any channel or all data when no values are requested.

If no query is specified, no data will be returned. A [`lengthRequired` error type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/411) <svg width="24px" height="24px" viewBox="0 0 24 24" style="cursor:pointer"><g stroke-width="2.1" stroke="#666" fill="none" stroke-linecap="round" stroke-linejoin="round"><polyline points="17 13.5 17 19.5 5 19.5 5 7.5 11 7.5"></polyline><path d="M14,4.5 L20,4.5 L20,10.5 M20,4.5 L11,13.5"></path></g></svg> will be displayed, with a refresh request button.

This refresh request button returns all data ordered by the UiD system implemented.

This endpoint can also return data by search query.
`/v1/#followers=6` will return some channels found with 6 followers.

Querying by `logo` returns the first channel with similar logo data to that queried.

Querying by `banner` returns all channels that use the same specific banner.

Querying by `followers`, `logo` or `banner` can return some completely irrelevant data, so it's not recommended.

Querying by `legacy id` or `channel` return **one** specific channel, and all it's data. `/v1/#channel=CKStudios2018` - `/v1/#legacy_id='legacy id'`

**Legacy ID's are currently deprecated, and will be decommissioned soon.**

#### To Note:
Everything in this doc was written to query with hash — `#` — and can only be queried like so.

Queries are also structured following Firefox's standard of adding a `/` — `/v1/#` — before a query, but on Chromium based browsers you can directly access endpoints with `/v1#`.
