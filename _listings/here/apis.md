---
name: HERE
x-slug: here
description: HERE Technologies enables people, enterprises and cities around the world
  to harness the power of location and create innovative solutions that make our lives
  safer and more efficient. We transform information from devices, vehicles, infrastructure
  and...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
x-kinRank: "7"
x-alexaRank: "3011"
tags: Transit
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/apis.md
specificationVersion: "0.14"
apis:
- name: Map Tile API - Color-reduced Transit Map
  x-api-slug: maptilenewestnormal-day-transit1220741409256png8-get
  description: |-
    *Request a color-reduced map tile with public transport*

    Color-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/maptilenewestnormal-day-transit1220741409256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/maptilenewestnormal-day-transit1220741409256png8-get-openapi.md
- name: Public Transport API - Avoid Transit Routes Involving Transfers
  x-api-slug: metarouterrestrouteservicev2route-json-get
  description: "*Request a direct public transit route excluding changes and transfers*\n\nPublic
    transit routes can be requested using the `metarouter/rest/routeservice/v2/route.json`
    endpoint. The `changes `parameter is used to indicate the number of changes or
    transfers desired. \n\n\n\n* **startX**  `number`\n \\- The longitude of the start
    point of your journey.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude
    of the start point of your journey.    e.g. `52.515`\n\n* **destX**  `number`\n
    \\- The longitude of the destination point of your journey.    e.g. `13.377`\n\n*
    **destY**  `number`\n \\- The latitude of the destination point of your journey.
    \   e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **routing**
    \ `enum`\n \\- Type of routing response required.  tt: time-table routing, i.e.
    route response will show scheduled arrival/departure times of the transit at the
    stations.  sr: simple (or estimated) routing, i.e. route response will only show
    \nthe transit journey but without scheduled arrival/departure times.  all: for
    both estimated and time-table routing.  Default: tt  \n\n    Valid values are
    : `tt`, `sr`, `all`\n\n* **changes**  `enum`\n \\- Maximum number of changes or
    transfers. \n                Valid values: 0-6 or -1. Default: -1 (any number
    of transfers permitted).\n\n    >**NOTE:** In areas where this parameter is not
    supported the route response will show an attribute `sup_changes=0` in the `Connections`
    node.\n\n    Valid values are : `-1`, `0`, `1`, `2`, `3`, `4`, `5`, `6`"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/metarouterrestrouteservicev2route-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/metarouterrestrouteservicev2route-json-get-openapi.md
- name: Public Transport API - Transit Coverage Nearby
  x-api-slug: coveragev1nearby-json-get
  description: "*Request a list of transit operators and station coverage nearby*\n\nOperator
    coverage is requested using the `coverage/v1/nearby.json` endpoint specifying
    the location using the `x` and `y` parameters.\n\n\n\n* **details**  `enum`\n
    \\- Don't show line info in Explored Coverage\n\n    Valid values are : `0` -
    disabled, `1` - enabled\n\n* **y**  `number`\n \\- The latitude of the center
    point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude
    of the center point of your search.    e.g. `13.377`\n\n* **chinaconfig**  `enum`\n
    \\- A switch that allows grouping results from Taiwan\ntogether with results from
    China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid
    values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20
    bytes Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/coveragev1nearby-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/coveragev1nearby-json-get-openapi.md
- name: Public Transport API - Transit Coverage Within a City
  x-api-slug: coveragev1search-json-get
  description: "*Request a list of transit operator coverage within a specified city*\n\nA
    list of operators working within a city is requested using the `coverage/v1/search.json`
    endpoint. The city is specified using the  `q` parameter.\n\n\n\n* **q**  `text`\n
    \\- The name or a part of the name of the city to search.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request.\n\n* **max**  `number`\n \\- Maximum number of
    results to be returned. Default is null.\n\n* **details**  `enum`\n \\- With this
    value set to 1, the list of supported operators and population of the city is
    returned.   When the value is set to 0, only the list of matching city names will
    be returned.  Default value = 1\n\n    Valid values are : `0` - disabled, `1`
    - enabled\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results
    from Taiwan\ntogether with results from China.      \n\n    Valid values are :
    `0` - disabled, `1` - enabled\n\n* **lang**  `text`\n \\- The language of the
    response. The value complies with the ISO 639-1 standard and defaults to <i>en</i>."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/coveragev1search-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/coveragev1search-json-get-openapi.md
- name: Public Transport API - Find Transit Coverage in Cities Nearby
  x-api-slug: coveragev1city-json-get
  description: "*Request a list of transit operators available in cities nearby*\n\nCity
    coverage can be found using the `coverage/v1/city.json` endpoint. The `x` and
    `y` parameters specify the location of the search.\n  The response also includes
    the number of transit lines and transit stops available for each city.\n  \n\n\n\n*
    **x**  `number`\n \\- The longitude of the center point of your search.    e.g.
    `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.
    \   e.g. `52.515`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping
    results from Taiwan\ntogether with results from China.    When enabled, Taiwan
    will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1`
    - enabled\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined
    with a center point defines the area of the search.\n\n* **app_id**  `text`\n
    \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an app_code and app_code with every request.\n\n*
    **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for
    the authentication of the client application.    You must include an app_code
    and app_code with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/coveragev1city-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/here/coveragev1city-json-get-openapi.md
x-common:
- type: x-blog-rss
  url: https://developer.here.com/blog/feed
- type: x-github
  url: https://github.com/heremaps
- type: x-postman-collection
  url: https://github.com/heremaps/postman-collections
- type: x-api-gallery
  url: http://healthcare.gov.api.gallery.streamdata.io
- type: x-api-stack
  url: http://here.stack.network
- type: x-blog
  url: https://developer.here.com/blog
- type: x-crunchbase
  url: https://crunchbase.com/organization/here-inc
- type: x-developer
  url: https://developer.here.com
- type: x-email
  url: dirk.popp@here.com
- type: x-email
  url: sebastian.kurme@here.com
- type: x-email
  url: jordan.stark@here.com
- type: x-email
  url: amy.stupavsky@here.com
- type: x-email
  url: minna.laub@here.com
- type: x-email
  url: stefanie.sirc@here.com
- type: x-email
  url: rachel.kuta@here.com
- type: x-email
  url: laurel.davis-lyons@here.com
- type: x-email
  url: linda.bradley@here.com
- type: x-email
  url: press@here.com
- type: x-twitter
  url: https://twitter.com/here
- type: x-website
  url: https://here.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---