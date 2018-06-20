---
swagger: "2.0"
x-collection-name: YouTube
x-complete: 0
info:
  title: Youtube Add Live Broadcasts Transition
  description: Changes the status of a YouTube live broadcast and initiates any processes
    associated with the new status. For example, when you transition a broadcast's
    status to testing, YouTube starts to transmit video to that broadcast's monitor
    stream. Before calling this method, you should confirm that the value of the status.streamStatus
    property for the stream bound to your broadcast is active.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: 1.0.0
host: www.googleapis.com
basePath: /youtube/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /liveBroadcasts/transition:
    post:
      summary: Add Live Broadcasts Transition
      description: Changes the status of a YouTube live broadcast and initiates any
        processes associated with the new status. For example, when you transition
        a broadcast's status to testing, YouTube starts to transmit video to that
        broadcast's monitor stream. Before calling this method, you should confirm
        that the value of the status.streamStatus property for the stream bound to
        your broadcast is active.
      operationId: postLivebroadcastsTransition
      x-api-path-slug: livebroadcaststransition-post
      parameters:
      - in: query
        name: broadcastStatus
        description: The broadcastStatus parameter identifies the state to which the
          broadcast is changing
      - in: query
        name: id
        description: The id parameter specifies the unique ID of the broadcast that
          is transitioning to another status
      - in: query
        name: onBehalfOfContentOwner
        description: 'Note: This parameter is intended exclusively for YouTube content
          partners'
      - in: query
        name: onBehalfOfContentOwnerChannel
        description: This parameter can only be used in a properly authorized request
      - in: query
        name: part
        description: The part parameter specifies a comma-separated list of one or
          more liveBroadcast resource properties that the API response will include
      responses:
        200:
          description: OK
      tags:
      - Livebroadcasts
      - Transition
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