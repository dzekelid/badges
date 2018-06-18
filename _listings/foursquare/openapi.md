---
swagger: "2.0"
x-collection-name: Foursquare
x-complete: 1
info:
  title: Foursquare
  description: checkin-explore-your-city-and-connect-people-and-places-bapi-v2-b
  version: 1.0.0
host: api.foursquare.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{USER_ID}/badges:
    get:
      summary: Get Users Badges
      description: users/search (POST)
      operationId: userssearch-post
      x-api-path-slug: usersuser-idbadges-get
      parameters:
      - in: query
        name: USER_ID
        description: ID for user to view badges for
      - in: path
        name: USER_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Users
      - Badges
---