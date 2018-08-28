---
swagger: "2.0"
x-collection-name: AWS Code Pipeline
x-complete: 0
info:
  title: AWS Code Pipeline API Disable Stage Transition
  version: 1.0.0
  description: |-
    Prevents artifacts in a pipeline from transitioning to the next stage in the
                pipeline.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DisableStageTransition:
    get:
      summary: Disable Stage Transition
      description: |-
        Prevents artifacts in a pipeline from transitioning to the next stage in the
                    pipeline.
      operationId: disableStageTransition
      x-api-path-slug: actiondisablestagetransition-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of volume results returned by DescribeVolumeStatus
          in      paginated output
        type: string
      - in: query
        name: NextToken
        description: The NextToken value to include in a future DescribeVolumeStatus      request
        type: string
      - in: query
        name: pipelineName
        description: The name of the pipeline in which you want to disable the flow
          of artifacts from            one stage to another
        type: string
      - in: query
        name: reason
        description: The reason given to the user why a stage is disabled, such as
          waiting for manual            approval or manual tests
        type: string
      - in: query
        name: stageName
        description: The name of the stage where you want to disable the inbound or
          outbound transition            of artifacts
        type: string
      - in: query
        name: transitionType
        description: Specifies whether artifacts will be prevented from transitioning
          into the stage and            being processed by the actions in that stage
          (inbound), or prevented from transitioning            from the stage after
          they have been processed by the actions in that stage            (outbound)
        type: string
      - in: query
        name: VolumeId.N
        description: One or more volume IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Disable
      - Stage
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