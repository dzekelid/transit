{
  "info": {
    "name": "HERE Public Transit API Transit Coverage Nearby",
    "_postman_id": "5670afb4-285f-4697-a369-f33cdb759ec7",
    "description": "*Request a list of transit operators and station coverage nearby*\n\nOperator coverage is requested using the `coverage/v1/nearby.json` endpoint specifying the location using the `x` and `y` parameters.\n\n\n\n* **details**  `enum`\n \\- Don't show line info in Explored Coverage\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "c52cfdec-19fd-4c56-b4d4-09b6de832769",
          "name": "SearchByNameJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/search/by_name.json?app_code=%7B%7D&app_id=%7B%7D&max=%7B%7D&method=%7B%7D&name=%7B%7D&radius=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of public transit stations based on name*\n\nA station search request can be made using the `search/by_name.json` endpoint and adding the `name` parameter. The focal point of the search is defined using the `x` and `y` parameters. The number of results can be further restricted by `max `and the `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **name**  `text`\n \\- Specifies the name or a part of the name of the station to search for and can be one word, multiple words or partial word separated by either comma or space.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the maximum number of stations/stops included in the response.\n  The minimum value is 1 and the maximum value is not limited.\n  The default value is 5.     \n\n* **method**  `enum`\n \\- Specifies if the matching method is *fuzzy* or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy - search for stations with the name having similar sounding and/or similar spelling to the names requested\n    * strict - search for stations with the name exactly matching the names requested or contains it as its part.\n\n   Valid values are : `fuzzy`, `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with a center point defines the area of the search. The minimum value is 0 and the maximum value is not limited.\n  The default value is 20000km."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba94a054-f084-41b1-8b4d-ab8eda8cb6c5"
            }
          ]
        }
      ]
    },
    {
      "name": "Avoid",
      "item": [
        {
          "id": "788b4095-1e5e-4c4a-8d07-4a8f67f98a76",
          "name": "MetarouterRestRouteserviceV2RouteJsonGet8",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/routeservice/v2/route.json?app_code=%7B%7D&app_id=%7B%7D&changes=%7B%7D&destX=%7B%7D&destY=%7B%7D&routing=%7B%7D&startX=%7B%7D&startY=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a direct public transit route excluding changes and transfers*\n\nPublic transit routes can be requested using the `metarouter/rest/routeservice/v2/route.json` endpoint. The `changes `parameter is used to indicate the number of changes or transfers desired. \n\n\n\n* **startX**  `number`\n \\- The longitude of the start point of your journey.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the start point of your journey.    e.g. `52.515`\n\n* **destX**  `number`\n \\- The longitude of the destination point of your journey.    e.g. `13.377`\n\n* **destY**  `number`\n \\- The latitude of the destination point of your journey.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **routing**  `enum`\n \\- Type of routing response required.  tt: time-table routing, i.e. route response will show scheduled arrival/departure times of the transit at the stations.  sr: simple (or estimated) routing, i.e. route response will only show \nthe transit journey but without scheduled arrival/departure times.  all: for both estimated and time-table routing.  Default: tt  \n\n    Valid values are : `tt`, `sr`, `all`\n\n* **changes**  `enum`\n \\- Maximum number of changes or transfers. \n                Valid values: 0-6 or -1. Default: -1 (any number of transfers permitted).\n\n    >**NOTE:** In areas where this parameter is not supported the route response will show an attribute `sup_changes=0` in the `Connections` node.\n\n    Valid values are : `-1`, `0`, `1`, `2`, `3`, `4`, `5`, `6`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d4b89411-f141-4893-b277-a2753afc60d8"
            }
          ]
        }
      ]
    },
    {
      "name": "Reachability",
      "item": [
        {
          "id": "20da3833-9bf4-435b-8724-8fec3360a3aa",
          "name": "IsochroneV1SearchJsonGet2",
          "request": {
            "url": "http://cit.transit.api.here.com/isochrone/v1/search.json?app_code=%7B%7D&app_id=%7B%7D&max_dur=%7B%7D&time=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of the public transit stations that can be reached in a given time*\n\nTo find the stations reachable in a specified time use the `isochrone/v1/search.json` endpoint specifying a center point using the `x` and `y` parameters and a maximum total duration in minutes using the `max_dur `parameter.\n  \n\n\n\n* **max_dur**  `number`\n \\- Maximum duration of the journeys, in minutes.   Minimum = 5, Maximum = 90.    The default duration is 15 minutes.    \n\n* **y**  `number`\n \\- The latitude of the start point of your journey.    e.g. `52.515`  \n\n* **x**  `number`\n \\- The longitude of the start point of your journey.    e.g. `13.377`    \n\n* **time**  `text`\n \\- Specifies the time in ISO 8601 (for example, 2015-10-18T06:36:40)\n        format. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eab78de3-abbd-4b1f-afbb-24f885a9109f"
            }
          ]
        }
      ]
    },
    {
      "name": "All",
      "item": [
        {
          "id": "1fdc79f1-c55a-4179-bb51-ffa3b13dd264",
          "name": "MetarouterRestBoardserviceV1MultiboardJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/metarouter/rest/boardservice/v1/multiboard.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&max=%7B%7D&max_stn=%7B%7D&prod=%7B%7D&startX=%7B%7D&startY=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of all next departure times and destinations from a location.*\n\nAll next departures information can be requested using the `metarouter/rest/boardservice/v1/multiboard.json` and specifying a `time` and `coordinates. `The maximum numbers of nearby stations and number of departures per station can be restricted by using the `max_stn` and `max` parameters, respectively.\n  \n  <b>NOTE:</b> This API has been deprecated and replaced with 2 new endpoints. Please see \n  <b><i>All Next Departures from a Location </i></b>and <b><i>All Next Departures for a list of Stations </i></b>for more details.\n  \n  \n\n\n\n* **lang**  `text`\n \\- Language of the response\n\n* **startX**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **startY**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **time**  `text`\n \\- Time in format `yyyy-mm-ddThh:mm:ss`.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `text`\n \\- The  maximum number of next departures per station to be included in the response.    The default value is 40.  \n\n* **max_stn**  `text`\n \\-  The maximum number of stations for which departures are required. The default value is 40.    \n\n* **prod**  `text`\n \\- A 16-bit binary number, where each bit represents one type of transit.  \n  0: High-speed Trains  \n  1: Intercity/EuroCity Trains  \n  2: Inter-regional and fast trains  \n  3: Regional and other trains  \n  4: City trains  \n  5: Buses  \n  6: Boat/Ferries  \n  7: Metro/Subway  \n  8: Tram  \n  9: Ordered services/Taxi  \n  10: Inclined/Funicular  \n  11: Aerial/Cable Car  \n  12: Rapid Bus  \n  13: Monorail  \n  14: Air plane  \n  15: Not yet defined  \n  The default is 1111111111111111, meaning all supported transit types are permitted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e0f0df8-4da8-4ec7-8ba6-a98875a9699f"
            }
          ]
        }
      ]
    },
    {
      "name": "Transit",
      "item": [
        {
          "id": "363aecc7-0df4-4306-89cd-a1d01f78176a",
          "name": "CoverageV1NearbyJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/coverage/v1/nearby.json?app_code=%7B%7D&app_id=%7B%7D&chinaconfig=%7B%7D&details=%7B%7D&x=%7B%7D&y=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a list of transit operators and station coverage nearby*\n\nOperator coverage is requested using the `coverage/v1/nearby.json` endpoint specifying the location using the `x` and `y` parameters.\n\n\n\n* **details**  `enum`\n \\- Don't show line info in Explored Coverage\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2dcc86ae-0486-41c8-8db6-a352aa4195e7"
            }
          ]
        }
      ]
    }
  ]
}