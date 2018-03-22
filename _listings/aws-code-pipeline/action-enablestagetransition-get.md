---
swagger: "2.0"
info:
  title: AWS Code Pipeline API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=EnableStageTransition:
    get:
      summary: ' Enable Stage Transition '
      description: Enables artifacts in a pipeline to transition to a stage in a pipeline
      operationId: enableStageTransition
      parameters:
      - in: query
        name: Device
        description: The device name
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Force
        description: Forces detachment if the previous detachment attempt did not
          occur cleanly (for example,      logging into an instance, unmounting the
          volume, and detaching normally)
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: pipelineName
        description: The name of the pipeline in which you want to enable the flow
          of artifacts from one            stage to another
        type: string
      - in: query
        name: stageName
        description: The name of the stage where you want to enable the transition
          of artifacts, either            into the stage (inbound) or from that stage
          to the next stage (outbound)
        type: string
      - in: query
        name: transitionType
        description: Specifies whether artifacts will be allowed to enter the stage
          and be processed by            the actions in that stage (inbound) or whether
          already-processed artifacts will be            allowed to transition to
          the next stage (outbound)
        type: string
      - in: query
        name: VolumeId
        description: The ID of the volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - enable
      - stage
      - transition
definitions: []
x-collection-name: AWS Code Pipeline
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