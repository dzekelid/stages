---
swagger: "2.0"
x-collection-name: AWS API Gateway
x-complete: 0
info:
  title: AWS API Gateway API Stage Update
  version: 1.0.0
  description: Changes information about the stage.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapis/fugvjdxtri/stages/stage1:
    patch:
      summary: Stage Update
      description: Changes information about the stage.
      operationId: stageUpdate
      x-api-path-slug: restapisfugvjdxtristagesstage1-patch
      parameters:
      - in: header
        name: '&quot;op&quot;'
        type: string
      - in: header
        name: '&quot;patchOperations&quot;'
        type: string
      - in: header
        name: '&quot;path&quot;'
        type: string
      - in: header
        name: '&quot;value&quot;'
        type: string
      - in: header
        name: Authorization
        type: string
      - in: header
        name: Content-Type
        type: string
      - in: body
        name: from
        description: Not supported
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Host
        type: string
      - in: body
        name: op
        description: An update operation to be performed with this PATCH request
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: path
        description: The op operation&#39;s target, as identified by a JSON Pointer
          value that references a location within the targeted resource
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: value
        description: The new target value of the update operation
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: X-Amz-Date
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stage
  /restapis/uycll6xg9a/stages/alpha:
    delete:
      summary: Stage Delete
      description: Deletes a named stage of a given API.
      operationId: stageDelete
      x-api-path-slug: restapisuycll6xg9astagesalpha-delete
      parameters:
      - in: header
        name: Authorization
        type: string
      - in: header
        name: Content-Type
        type: string
      - in: header
        name: Host
        type: string
      - in: header
        name: X-Amz-Date
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stage
  /restapis/uycll6xg9a/stages/alpha/cache/data:
    delete:
      summary: Stage Flush
      description: Flushes the cached data of a named stage.
      operationId: stageFlush-cache
      x-api-path-slug: restapisuycll6xg9astagesalphacachedata-delete
      parameters:
      - in: header
        name: Authorization
        type: string
      - in: header
        name: Content-Type
        type: string
      - in: header
        name: Host
        type: string
      - in: header
        name: X-Amz-Date
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stage
      - Flush
  /restapis/uycll6xg9a/stages/alpha/cache/authorizers:
    delete:
      summary: Stage Flush
      description: Flushes all cached Authorizer entries on a named stage.
      operationId: stageFlush-authorizer-cache
      x-api-path-slug: restapisuycll6xg9astagesalphacacheauthorizers-delete
      parameters:
      - in: header
        name: Authorization
        type: string
      - in: header
        name: Content-Type
        type: string
      - in: header
        name: Host
        type: string
      - in: header
        name: X-Amz-Date
        type: string
      responses:
        200:
          description: OK
      tags:
      - Stage
      - Flush
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