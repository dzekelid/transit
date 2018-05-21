---
swagger: "2.0"
x-collection-name: AWS Code Pipeline
x-complete: 1
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
  /?Action=EnableStageTransition:
    get:
      summary: Enable Stage Transition
      description: Enables artifacts in a pipeline to transition to a stage in a pipeline.
      operationId: enableStageTransition
      x-api-path-slug: actionenablestagetransition-get
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
      - Enable
      - Stage
      - Transition
---