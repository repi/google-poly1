Lists assets that the user has liked. Only the value &#39;me&#39;, representing
the currently-authenticated user, is supported. May include assets with an
access level of UNLISTED.
# Required Scalar Argument
* **&lt;name&gt;** *(string)*
    - A valid user id. Currently, only the special value &#39;me&#39;, representing the
        currently-authenticated user is supported. To use &#39;me&#39;, you must pass
        an OAuth token with the request.

# Optional Output Flags

The method's return value a JSON encoded structure, which will be written to standard output by default.

* **-o out**
    - *out* specifies the *destination* to which to write the server's result to.
      It will be a JSON-encoded structure.
      The *destination* may be `-` to indicate standard output, or a filepath that is to contain the received bytes.
      If unset, it defaults to standard output.
# Optional Method Properties

You may set the following properties to further configure the call. Please note that `-p` is followed by one 
or more key-value-pairs, and is called like this `-p k1=v1 k2=v2` even though the listing below repeats the
`-p` for completeness.

* **-p order-by=string**
    - Specifies an ordering for assets. Acceptable values are:
        `BEST`, `NEWEST`, `OLDEST`, &#39;LIKED_TIME&#39;. Defaults to `LIKED_TIME`, which
        ranks assets based on how recently they were liked.

* **-p page-size=integer**
    - The maximum number of assets to be returned. This value must be between `1`
        and `100`. Defaults to `20`.

* **-p format=string**
    - Return only assets with the matching format. Acceptable values are:
        `BLOCKS`, `FBX`, `GLTF`, `GLTF2`, `OBJ`, `TILT`.

* **-p page-token=string**
    - Specifies a continuation token from a previous search whose results were
        split into multiple pages. To get the next page, submit the same request
        specifying the value from
        next_page_token.

# Optional General Properties

The following properties can configure any call, and are not specific to this method.

* **-p $-xgafv=string**
    - V1 error format.

* **-p access-token=string**
    - OAuth access token.

* **-p alt=string**
    - Data format for response.

* **-p callback=string**
    - JSONP

* **-p fields=string**
    - Selector specifying which fields to include in a partial response.

* **-p key=string**
    - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.

* **-p oauth-token=string**
    - OAuth 2.0 token for the current user.

* **-p pretty-print=boolean**
    - Returns response with indentations and line breaks.

* **-p quota-user=string**
    - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.

* **-p upload-type=string**
    - Legacy upload protocol for media (e.g. &#34;media&#34;, &#34;multipart&#34;).

* **-p upload-protocol=string**
    - Upload protocol for media (e.g. &#34;raw&#34;, &#34;multipart&#34;).
