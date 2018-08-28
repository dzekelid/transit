{
  "info": {
    "name": "HERE Public Transit API Find Transit Coverage in Cities Nearby",
    "_postman_id": "c6954883-6785-44e8-9163-3f80687bca21",
    "description": "*Request a list of transit operators available in cities nearby*\n\nCity coverage can be found using the `coverage/v1/city.json` endpoint. The `x` and `y` parameters specify the location of the search.\n  The response also includes the number of transit lines and transit stops available for each city.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with a center point defines the area of the search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Find",
      "item": [
        {
          "id": "4ae664bf-030d-498d-ad8c-992ea89d8866",
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
              "id": "2029c005-b8b2-442c-86ec-d2ed8afebfb1"
            }
          ]
        },
        {
          "id": "c1bbaae7-91c1-42d9-944a-1950a1d5324b",
          "name": "SearchByStopidsJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/search/by_stopids.json?app_code=%7B%7D&app_id=%7B%7D&lang=%7B%7D&stopIds=%7B%7D",
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
            "description": "*Request details of a specific transit station based on a previous request*\n\nStation details are requested using the `search/by_stopids.json` endpoint and appending a comma delimited list of `stop-ids` to the request URL. Usually, the request to this endpoint will be called after making a station search request, to obtain a list of stations Ids.\n  \n\n\n\n* **stopIds**  `text`\n \\- Specifies a list of stopIds separated by comma. Each stopId must contain at least 6 characters and must not exceed a maximum of 1000 characters.     The format of a station Id is 123456789#100. Only the first 9-digits are mandatory and if the full Id is to be used, the `#` character must be encoded as `%23`.      \n\n* **lang**  `text`\n \\- A language of the response. \n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9f1dc56b-4b55-4315-b2a0-9273391793ae"
            }
          ]
        },
        {
          "id": "2417add1-37f5-4929-8084-1a9306d4312c",
          "name": "SearchByGeocoordJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/search/by_geocoord.json?app_code=%7B%7D&app_id=%7B%7D&max=%7B%7D&radius=%7B%7D&x=%7B%7D&y=%7B%7D",
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
            "description": "*Request a list of public transit stations within a given geo-location.*\n\nTo find the nearest stations use the `search/by_geocoord.json` endpoint specifying a center point using the `x` and `y` parameters and a search radius in meters using the `radius` parameter. `Max` value can also be used to restrict the number of results shown in the response.\n\n\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with the geo-coordinates defines the area of the search. The default value is 500m.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Specifies the maximum number of stations/stops included in the response. \n          The default value is 5. The minimum value is 1 and the maximum value is not limited."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59a1bfd0-8566-446f-81f4-b3800dbca7a5"
            }
          ]
        },
        {
          "id": "a75485e1-c5c1-4c46-ad0b-b156bf3da6e4",
          "name": "CoverageV1CityJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/coverage/v1/city.json?app_code=%7B%7D&app_id=%7B%7D&chinaconfig=%7B%7D&radius=%7B%7D&x=%7B%7D&y=%7B%7D",
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
            "description": "*Request a list of transit operators available in cities nearby*\n\nCity coverage can be found using the `coverage/v1/city.json` endpoint. The `x` and `y` parameters specify the location of the search.\n  The response also includes the number of transit lines and transit stops available for each city.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude of the center point of your search.    e.g. `52.515`\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.    When enabled, Taiwan will appear as part of China.    \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **radius**  `number`\n \\- Specifies a radius in meters when combined with a center point defines the area of the search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "508f3a02-4ff5-4794-b794-6d29713092b0"
            }
          ]
        }
      ]
    }
  ]
}