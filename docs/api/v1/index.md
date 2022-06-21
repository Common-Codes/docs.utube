# utubei/v1
## Method and Values:
Method: `GET`

Possible Values: /v1/#{`followers`, `logo`, `banner`, `legacy_id`, `c`}

### Description:
The /v1/ endpoint can be used to return specific data from any channel or all data when no values are requested.

If no query is specified, all channel data available will be returned, ordered by the UiD system implemented.

This endpoint can also return data by search query.
`/v1/#followers=100` will return all channels with 100 followers.

Filtering by `logo` returns all channels with similar logo data to that queried.

Filtering by `banner` returns all channels that use the same banner.
Filtering by `logo` & `banner` is sometimes very broken, so it is not recommended.

Queries by `legacy id` & `channel` return **one** specific channel, and all it's data. `/v1/#channel=CKStudios2018` - `/v1/#legacy_id=`legacy id - **the legacy id system is currently deprecated, and will be removed soon.**

#### To Note:
Everything in this doc was written to query with `#`, and can only be queried like so.

Queries are also structured following Firefox's standard of adding a `/` before a query, but on Chromium based browsers you can directly access endpoints with `/v1#`.
