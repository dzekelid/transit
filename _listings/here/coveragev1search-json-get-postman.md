{
  "info": {
    "name": "HERE Public Transit API Transit Coverage Within a City",
    "_postman_id": "ee10e49e-16d6-4e45-8233-4a190021c465",
    "description": "*Request a list of transit operator coverage within a specified city*\n\nA list of operators working within a city is requested using the `coverage/v1/search.json` endpoint. The city is specified using the  `q` parameter.\n\n\n\n* **q**  `text`\n \\- The name or a part of the name of the city to search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Maximum number of results to be returned. Default is null.\n\n* **details**  `enum`\n \\- With this value set to 1, the list of supported operators and population of the city is returned.   When the value is set to 0, only the list of matching city names will be returned.  Default value = 1\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.      \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **lang**  `text`\n \\- The language of the response. The value complies with the ISO 639-1 standard and defaults to <i>en</i>.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transit",
      "item": [
        {
          "id": "a2326811-69c5-469e-87f2-f463a5d81a3d",
          "name": "CoverageV1SearchJsonGet",
          "request": {
            "url": "http://cit.transit.api.here.com/coverage/v1/search.json?app_code=%7B%7D&app_id=%7B%7D&chinaconfig=%7B%7D&details=%7B%7D&lang=%7B%7D&max=%7B%7D&q=%7B%7D",
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
            "description": "*Request a list of transit operator coverage within a specified city*\n\nA list of operators working within a city is requested using the `coverage/v1/search.json` endpoint. The city is specified using the  `q` parameter.\n\n\n\n* **q**  `text`\n \\- The name or a part of the name of the city to search.\n\n* **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the authentication of the client application.    You must include an app_code and app_code with every request.\n\n* **max**  `number`\n \\- Maximum number of results to be returned. Default is null.\n\n* **details**  `enum`\n \\- With this value set to 1, the list of supported operators and population of the city is returned.   When the value is set to 0, only the list of matching city names will be returned.  Default value = 1\n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **chinaconfig**  `enum`\n \\- A switch that allows grouping results from Taiwan\ntogether with results from China.      \n\n    Valid values are : `0` - disabled, `1` - enabled\n\n* **lang**  `text`\n \\- The language of the response. The value complies with the ISO 639-1 standard and defaults to <i>en</i>."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "28692f12-c3e1-48fb-ad35-4a4f76a18450"
            }
          ]
        }
      ]
    }
  ]
}