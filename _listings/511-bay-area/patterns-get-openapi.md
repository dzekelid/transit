---
swagger: "2.0"
x-collection-name: 511 Bay Area
x-complete: 0
info:
  title: Bay Area 511 Transit API Transit Patterns API
  description: San francisco 511 transit transit patterns api.
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: api.511.org
basePath: /transit
paths:
  /patterns:
    get:
      summary: Transit Patterns API
      description: San francisco 511 transit transit patterns api.
      operationId: PatternsGet
      x-api-path-slug: patterns-get
      parameters:
      - in: query
        name: api_key
      - in: query
        name: operator_id
      - in: query
        name: pattern_id
      responses:
        200:
          description: OK
      tags:
      - "511"
      - Transit
      - Patterns
      - API
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---