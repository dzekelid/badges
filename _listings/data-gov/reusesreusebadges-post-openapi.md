---
swagger: "2.0"
x-collection-name: Data.Gov
x-complete: 0
info:
  title: Data.gov API Add Reuses Reuse Badges
  description: Create a new badge for a given reuse
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
  /organizations/{org}/badges/:
    post:
      summary: Add Organizations Org Badges
      description: Create a new badge for a given organization
      operationId: postOrganizationsOrgBadges
      x-api-path-slug: organizationsorgbadges-post
      parameters:
      - in: path
        name: org
        description: The organization ID or slug
      - in: body
        name: payload
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Org
      - Badges
  /organizations/{org}/badges/{badge_kind}/:
    delete:
      summary: Delete Organizations Org Badges Badge Kind
      description: Delete a badge for a given organization
      operationId: deleteOrganizationsOrgBadgesBadgeKind
      x-api-path-slug: organizationsorgbadgesbadge-kind-delete
      parameters:
      - in: path
        name: badge_kind
      - in: path
        name: org
        description: The organization ID or slug
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Org
      - Badges
      - Badge
      - Kind
  /reuses/badges/:
    get:
      summary: Get Reuses Badges
      description: List all available reuse badges and their labels
      operationId: getReusesBadges
      x-api-path-slug: reusesbadges-get
      responses:
        200:
          description: OK
      tags:
      - Reuses
      - Badges
  /reuses/{reuse}/badges/:
    post:
      summary: Add Reuses Reuse Badges
      description: Create a new badge for a given reuse
      operationId: postReusesReuseBadges
      x-api-path-slug: reusesreusebadges-post
      parameters:
      - in: body
        name: payload
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: reuse
        description: The reuse ID or slug
      responses:
        200:
          description: OK
      tags:
      - Reuses
      - Reuse
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