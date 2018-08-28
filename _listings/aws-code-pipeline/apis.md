---
name: AWS Code Pipeline
x-slug: aws-code-pipeline
description: AWS Data Pipeline is a web service that helps you reliably process and
  move data between different AWS compute and storage services, as well as on-premise
  data sources, at specified intervals. With AWS Data Pipeline, you can regularly
  access your data where it&rsquo;s stored, transform and process it at scale, and
  efficiently transfer the results to AWS services such as Amazon S3, Amazon RDS,
  Amazon DynamoDB, and Amazon EMR.AWS Data Pipeline helps you easily create complex
  data processing workloads that are fault tolerant, repeatable, and highly available.
  You don&rsquo;t have to worry about ensuring resource availability, managing inter-task
  dependencies, retrying transient failures or timeouts in individual tasks, or creating
  a failure notification system. AWS Data Pipeline also allows you to move and process
  data that was previously locked up in on-premise data silos.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Developer-Tools_AWSCodePipeline.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Transit
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/aws-code-pipeline/apis.md
specificationVersion: "0.14"
apis:
- name: AWS Code Pipeline API - Disable Stage Transition
  x-api-slug: actiondisablestagetransition-get
  description: |-
    Prevents artifacts in a pipeline from transitioning to the next stage in the
                pipeline.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Developer-Tools_AWSCodePipeline.png
  humanURL: https://aws.amazon.com/datapipeline/
  baseURL: :///
  tags: Amazon Web Services, SDK, Data, Orchestration, Stack Network, API Service
    Provider, API Service Provider, API Provider, Migrations, Profiles, Relative Data,
    Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/aws-code-pipeline/actiondisablestagetransition-get-openapi.md
- name: AWS Code Pipeline API - Enable Stage Transition
  x-api-slug: actionenablestagetransition-get
  description: Enables artifacts in a pipeline to transition to a stage in a pipeline.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Developer-Tools_AWSCodePipeline.png
  humanURL: https://aws.amazon.com/datapipeline/
  baseURL: :///
  tags: Amazon Web Services, SDK, Data, Orchestration, Stack Network, API Service
    Provider, API Service Provider, API Provider, Migrations, Profiles, Relative Data,
    Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/transit/master/_listings/aws-code-pipeline/actionenablestagetransition-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.cloudwatch.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.code.pipeline.stack.network
- type: x-blog
  url: http://blogs.aws.amazon.com/bigdata
- type: x-change-log
  url: http://aws.amazon.com/releasenotes/AWS-Data-Pipeline/
- type: x-documentation
  url: http://docs.aws.amazon.com/datapipeline/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/datapipeline/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=151
- type: x-pricing
  url: https://aws.amazon.com/datapipeline/pricing/
- type: x-tools
  url: http://aws.amazon.com/developertools/AWS-Data-Pipeline/
- type: x-website
  url: https://aws.amazon.com/datapipeline/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---