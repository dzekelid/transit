{
  "info": {
    "name": "Bay Area 511 Transit API Transit Patterns API",
    "_postman_id": "2043c751-36a6-475a-8784-1d3f84065e70",
    "description": "San francisco 511 transit transit patterns api.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "511",
      "item": [
        {
          "id": "90cfd3a8-4ab9-4dec-be63-5ce4d6684059",
          "name": "LinesGet",
          "request": {
            "url": "http://api.511.org/transit/lines?api_key=%7B%7D&operator_id=%7B%7D",
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
            "description": "San francisco 511 transit lines api."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dbf55e59-a544-4fb3-8e07-495b84933a8b"
            }
          ]
        },
        {
          "id": "20a73efb-dc90-4855-8d1c-45f031d0477c",
          "name": "PatternsGet",
          "request": {
            "url": "http://api.511.org/transit/patterns?api_key=%7B%7D&operator_id=%7B%7D&pattern_id=%7B%7D",
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
            "description": "San francisco 511 transit transit patterns api."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "606a0436-274d-4c7c-b015-9a9df003b252"
            }
          ]
        }
      ]
    }
  ]
}