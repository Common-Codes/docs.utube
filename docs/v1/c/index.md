# /c/{`#`, `?`} (channel)
## Usage and Examples:
Method: `GET`

Possible Values: /c/#{`followers`, `type`, `logo`, `banner`, `url`, `legacy id`, `channel`}

### Description:
The /c/ endpoint can be used to return specific data from any channel or all data when no values are requested.

If no channel is requested, all channel data available will be returned, ordered by the uid system implemented.

This endpoint can also return data by search query. `/c/#followers=100` will return all channels with 100 to 199 followers.

Querying by `type` is useless. All channels are of type `channel`, so `/c/#type=channel` will return everything.

Filtering by `URL`, `logo` & `banner` is sometimes very broken, so it is not recommended.

Queries by `legacy id` & `channel` return **one** specific channel, and all it's data. `/c/#channel=CKStudios2018` - `/c/#legacy_id=`legacy id

#### To Note:
Everything in this doc was written to query with `#`, but can also be queried with `?`.
Queries are also structured following Firefox's standard of adding a `/` before a query, but on Chromium based browsers you can directly access endpoints with `/c?`.
