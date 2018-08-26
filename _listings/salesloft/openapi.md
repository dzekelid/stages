---
swagger: "2.0"
x-collection-name: SalesLoft
x-complete: 1
info:
  title: SalesLoft
  description: salesloft-helps-transform-sales-teams-into-modern-sales-organizations---converting-more-target-accounts-into-customer-accounts
  version: v2
host: api.salesloft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/person_stages.json:
    get:
      summary: List person stages
      description: |-
        Fetches multiple person stage records. The records can be filtered, paged, and sorted according to
        the respective parameters.
      operationId: v2.person_stages.json.get
      x-api-path-slug: v2person-stages-json-get
      parameters:
      - in: query
        name: ids
        description: IDs of person stages to fetch
      - in: query
        name: include_paging_counts
        description: Whether to include total_pages and total_count in the metadata
      - in: query
        name: page
        description: The current page to fetch results from
      - in: query
        name: per_page
        description: How many records to show per page in the range [1, 100]
      - in: query
        name: sort_by
        description: 'Key to sort on, must be one of: created_at, updated_at'
      - in: query
        name: sort_direction
        description: 'Direction to sort in, must be one of: ASC, DESC'
      responses:
        200:
          description: OK
      tags:
      - Sales
      - List
      - Person
      - Stages
    post:
      summary: Create a person stage
      description: Creates a person stage.
      operationId: v2.person_stages.json.post
      x-api-path-slug: v2person-stages-json-post
      parameters:
      - in: formData
        name: name
        description: The name of the new stage
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Person
      - Stage
  /v2/person_stages/{id}.json:
    delete:
      summary: Delete an person stage
      description: |-
        Deletes a person stage. This operation is not reversible without contacting support.
        This operation can be called multiple times successfully.
      operationId: v2.person_stages.id.json.delete
      x-api-path-slug: v2person-stagesid-json-delete
      parameters:
      - in: path
        name: id
        description: Stage ID
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Person
      - Stage
    get:
      summary: Fetch a person stage
      description: Fetches a person stage, by ID only.
      operationId: v2.person_stages.id.json.get
      x-api-path-slug: v2person-stagesid-json-get
      parameters:
      - in: path
        name: id
        description: Stage ID
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Fetch
      - Person
      - Stage
    put:
      summary: Update a person stage
      description: Updates a person stage.
      operationId: v2.person_stages.id.json.put
      x-api-path-slug: v2person-stagesid-json-put
      parameters:
      - in: path
        name: id
        description: Stage ID
      - in: formData
        name: name
        description: The name of the stage
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Person
      - Stage
---