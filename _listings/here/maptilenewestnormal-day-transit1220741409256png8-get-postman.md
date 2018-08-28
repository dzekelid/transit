{
  "info": {
    "name": "HERE Map Tile API Color-reduced Transit Map",
    "_postman_id": "effa6276-7ff3-48b1-a899-24b7981118a5",
    "description": "*Request a color-reduced map tile with public transport*\n\nColor-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Terrain",
      "item": [
        {
          "id": "b4efe97d-00c6-4258-9cc3-40d695402465",
          "name": "TerrainDay76645256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/terrain.day/7/66/45/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a terrain map tile*\n\nTerrain map tile are available by passing `terrain.day` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1bef4833-4ac6-4277-8026-fec139ad9a47"
            }
          ]
        }
      ]
    },
    {
      "name": "Multiple",
      "item": [
        {
          "id": "789a0966-32fc-4a3f-8de1-a8f31bc269a8",
          "name": "MaptileNewestNormalDay63024256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/6/30/24/256/png8?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D&range=%7B%7D",
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
            "description": "*Request multiple base64 encoded map tiles*\n\nA square consisting of multiple base64 encoded tiles is requested by adding the parameters `output=base64` and `range=NxN` to the request URL. The `column` and `row` in the path of the URL, defining the top left-hand corner of the tile group must be divisible by the value of the `range` parameter.\n  \n  Click on the response to decode the tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates the size of the array of tiles returned. Valid values are `2x2`, `3x3` or `4x4`\n\n Valid values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "add9f58a-cf02-4d77-92f6-a3f434f175a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Color-reduced",
      "item": [
        {
          "id": "19beadf4-850e-452b-9a78-cfdd32837785",
          "name": "MaptileNewestNormalDayTransit1220741409256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day.transit/12/2074/1409/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a color-reduced map tile with public transport*\n\nColor-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "47b42b64-aa2d-42e4-ac29-c96fa13a4b18"
            }
          ]
        },
        {
          "id": "ddba0c18-03c1-4c26-8c45-a3caa4ac8d9a",
          "name": "MaptileNewestNormalDayGrey11525761256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day.grey/11/525/761/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a greyed out street map tile*\n\nMaps using a reduced color palette can be requested by passing `normal.day.grey` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "462168a4-6483-4454-8813-92b25435bccd"
            }
          ]
        }
      ]
    },
    {
      "name": "Hybrid",
      "item": [
        {
          "id": "70d951b2-1c4a-4076-b122-cbddf85ef772",
          "name": "HybridDay485256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/hybrid.day/4/8/5/256/png8?app_code=%7B%7D&app_id=%7B%7D&lg=%7B%7D",
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
            "description": "*Request a hybrid map tile - satellite imagery with labels*\n\nHybrid map tile are available by passing `hybrid.day` in the path of the request URL. The map tiles will display using the default language of the server unless the `lg` query parameter is used to change the map tile language. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26ad71d4-db3f-42a5-b91e-c27946395d4e"
            }
          ]
        }
      ]
    },
    {
      "name": "Truck",
      "item": [
        {
          "id": "96d00ec1-067c-411c-9e55-97b3073adbbe",
          "name": "TrucktileNewestNormalDay1221991342256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/trucktile/newest/normal.day/12/2199/1342/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a street map tile showing restrictions for heavy vehicles*\n\nTo obtain a map tile displaying route restrictions for trucks, use the `trucktile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f4ebe75-be4b-46b0-87e2-2a1719a5bc92"
            }
          ]
        }
      ]
    },
    {
      "name": "Toll",
      "item": [
        {
          "id": "1f530932-60cd-4233-8fcf-7da67ebab351",
          "name": "MaptileNewestNormalDay9255170256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/9/255/170/256/png8?app_code=%7B%7D&app_id=%7B%7D&congestion=%7B%7D",
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
            "description": "*Request a street map tile highlighting congestion and environmental toll zones*\n\nTo highlight such toll zones, add the `congestion` parameter to the request URL.\n\n\n\n* **congestion**  `null`\n \\- Flag to indicate if congestion zones are to be shown on the map.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "352fac38-a040-4726-a3e4-f5e5983bf38a"
            }
          ]
        }
      ]
    },
    {
      "name": "Satellite",
      "item": [
        {
          "id": "40407081-edbf-4b26-9702-59d95e71f584",
          "name": "SatelliteDay51512256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/satellite.day/5/15/12/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a satellite map tile*\n\nSatellite map tiles do not display labels and are available by passing `satellite.day` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "02254155-5174-4407-bd8d-9a07775f829b"
            }
          ]
        }
      ]
    },
    {
      "name": "Fleet",
      "item": [
        {
          "id": "e4822d12-afae-437d-8398-13dd8c781cda",
          "name": "MaptileNewestNormalDay1340932723256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/13/4093/2723/256/png8?app_code=%7B%7D&app_id=%7B%7D&style=%7B%7D",
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
            "description": "*Request a street map tile using the fleet vehicle color scheme*\n\nFleet color scheme map tiles are available by passing `style=fleet` as a parameter of the request URL.\n\n\n\n* **style**  `enum`\n \\- If present, selects the style to use to render the tile.\n\n Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`, `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9adbbc79-5b06-4c80-b64a-2ba23923815a"
            }
          ]
        }
      ]
    },
    {
      "name": "Base64",
      "item": [
        {
          "id": "d715b58c-d500-4cce-9c2a-761771eb3ed0",
          "name": "MaptileNewestNormalDay11525761256Png8Get4",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/11/525/761/256/png8?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D",
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
            "description": "*Request a base64 encoded map tile*\n\nBase64 encoded tiles are requested by adding the parameter `output=base64` to the request URL.\n  \n  Click on the response to decode the tile returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return the tile as base64 encoded text.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "beae95a3-7182-40fe-b776-37b4100c2e2e"
            }
          ]
        }
      ]
    },
    {
      "name": "Map",
      "item": [
        {
          "id": "9b588f61-aac6-4161-a3da-537ef92d3528",
          "name": "InfoGet",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/info?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D",
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
            "description": "*Request information about the types of map tiles available on a server*\n\nTo make a request for metadata information, use the `info` parameter in the path of the request URL.\n\n\n\n* **output**  `enum`\n \\- Indicates whether to return the information in XML format, JSON format or as an XML schema (XSD) of the API metadata\n\n Valid values are : `json`, `xml`, `xsd`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13cb39fe-e73b-4bbd-9894-a26fd8bc3e26"
            }
          ]
        }
      ]
    },
    {
      "name": "Transparent",
      "item": [
        {
          "id": "15218fc3-9572-4283-bd91-d5adf0a69b15",
          "name": "TruckonlytileNewestNormalDay1221991342256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/truckonlytile/newest/normal.day/12/2199/1342/256/png8?app_code=%7B%7D&app_id=%7B%7D",
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
            "description": "*Request a transparent tile showing restrictions for heavy vehicles only*\n\nTo obtain a transparent map tile displaying route restrictions for trucks, use the `truckonlytile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b961764f-a4a9-4a50-882b-5a70507c5c40"
            }
          ]
        }
      ]
    }
  ]
}