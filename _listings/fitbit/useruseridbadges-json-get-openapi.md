---
swagger: "2.0"
x-collection-name: Fitbit
x-complete: 0
info:
  title: Fitbit Get User User Badges.json
  description: Get user's badges in the format requested. Response includes all badges
    for the user as seen on the Fitbit website badge locker (both activity and weight
    related). We return weight and distance badges based on the user's unit profile
    preference as on the website.
  version: 1.0.0
host: api.fitbit.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user/{user-id}/badges.json:
    get:
      summary: Get User User Badges.json
      description: Get user's badges in the format requested. Response includes all
        badges for the user as seen on the Fitbit website badge locker (both activity
        and weight related). We return weight and distance badges based on the user's
        unit profile preference as on the website.
      operationId: getUserUserBadges.json
      x-api-path-slug: useruseridbadges-json-get
      responses:
        200:
          description: OK
      tags:
      - User
      - User-id
      - Badges.json
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