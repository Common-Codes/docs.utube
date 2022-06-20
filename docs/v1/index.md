# utubei/v1
## Method and Values:
Method: `GET`

Possible Values: /v1/#{`followers`, `logo`, `banner`, `url`, `legacy_id`, `c`}

### Description:
The /v1/ endpoint can be used to return specific data from any channel or all data when no values are requested.

If no channel is requested, all channel data available will be returned, ordered by the uid system implemented.

This endpoint can also return data by search query.
`/c/#followers=100` will return all channels with 100 to 199 followers.

Filtering by `URL`, `logo` & `banner` is sometimes very broken, so it is not recommended.

Queries by `legacy id` & `channel` return **one** specific channel, and all it's data. `/c/#channel=CKStudios2018` - `/c/#legacy_id=`legacy id - **the legacy id system is currently deprecated, and will be removed soon.**

#### To Note:
Everything in this doc was written to query with `#`, and can only be queried like so.

Queries are also structured following Firefox's standard of adding a `/` before a query, but on Chromium based browsers you can directly access endpoints with `/c#`.
