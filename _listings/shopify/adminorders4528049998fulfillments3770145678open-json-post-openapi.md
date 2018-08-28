---
swagger: "2.0"
x-collection-name: Shopify
x-complete: 0
info:
  title: Shopify Transition a fulfillment from pending to open.
  description: Transition a fulfillment from pending to open..
  version: 1.0.0
host: DefaultParameterValue:DefaultParameterValue@DefaultParameterValue.myshopify.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/orders/4528049998/fulfillments/3770145678/open.json:
    post:
      summary: Transition a fulfillment from pending to open.
      description: Transition a fulfillment from pending to open..
      operationId: postAdminOrders4528049998Fulfillments3770145678Open.json
      x-api-path-slug: adminorders4528049998fulfillments3770145678open-json-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Transition
      - Fulfillment
      - From
      - Pending
      - To
      - Open
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