---
swagger: "2.0"
x-collection-name: Fitbit
x-complete: 1
info:
  title: Fitbit
  description: bring-fitbit-health-data-into-your-apps-including-user-activities-sleep-heart-glucose-and-blood-pressure-information-
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
---