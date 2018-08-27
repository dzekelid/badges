---
swagger: "2.0"
x-collection-name: Data.Gov
x-complete: 0
info:
  title: Data.gov API Get Organizations Badges
  description: List all available organization badges and their labels
  version: "3"
host: catalog.data.gov
basePath: /api/3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /datasets/badges/:
    get:
      summary: Get Datasets Badges
      description: List all available dataset badges and their labels
      operationId: getDatasetsBadges
      x-api-path-slug: datasetsbadges-get
      responses:
        200:
          description: OK
      tags:
      - Datasets
      - Badges
  /datasets/{dataset}/badges/:
    post:
      summary: Add Datasets Dataset Badges
      description: Create a new badge for a given dataset
      operationId: postDatasetsDatasetBadges
      x-api-path-slug: datasetsdatasetbadges-post
      parameters:
      - in: path
        name: dataset
        description: The dataset ID or slug
      - in: body
        name: payload
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Datasets
      - Dataset
      - Badges
  /datasets/{dataset}/badges/{badge_kind}/:
    delete:
      summary: Delete Datasets Dataset Badges Badge Kind
      description: Delete a badge for a given dataset
      operationId: deleteDatasetsDatasetBadgesBadgeKind
      x-api-path-slug: datasetsdatasetbadgesbadge-kind-delete
      parameters:
      - in: path
        name: badge_kind
      - in: path
        name: dataset
        description: The dataset ID or slug
      responses:
        200:
          description: OK
      tags:
      - Datasets
      - Dataset
      - Badges
      - Badge
      - Kind
  /organizations/badges/:
    get:
      summary: Get Organizations Badges
      description: List all available organization badges and their labels
      operationId: getOrganizationsBadges
      x-api-path-slug: organizationsbadges-get
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Badges
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