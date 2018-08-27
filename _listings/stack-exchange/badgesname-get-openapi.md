---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Get Badge Name
  description: "Gets all explicitly named badges in the system.\n \nA named badged
    stands in opposition to a tag-based badge. These are referred to as general badges
    on the sites themselves.\n \nFor the rank sort, bronze is greater than silver
    which is greater than gold. Along with sort=rank, set max=gold for just gold badges,
    max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank
    is the default sort.\n \nThis method returns a list of badges."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /badges:
    get:
      summary: Get Badges
      description: "Returns all the badges in the system.\n \nBadge sorts are a tad
        complicated. For the purposes of sorting (and min/max) tag_based is considered
        to be greater than named.\n \nThis means that you can get a list of all tag
        based badges by passing min=tag_based, and conversely all the named badges
        by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than
        silver which is greater than gold. Along with sort=rank, set max=gold for
        just gold badges, max=silver&min=silver for just silver, and min=bronze for
        just bronze.\n \nrank is the default sort.\n \nThis method returns a list
        of badges."
      operationId: returns-all-the-badges-in-the-system-badge-sorts-are-a-tad-complicated-for-the-purposes-of-sorting-a
      x-api-path-slug: badges-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: sort = rank => stringsort = name => stringsort = type => string
      - in: query
        name: min
        description: sort = rank => stringsort = name => stringsort = type => string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Badges
  /badges/name:
    get:
      summary: Get Badge Name
      description: "Gets all explicitly named badges in the system.\n \nA named badged
        stands in opposition to a tag-based badge. These are referred to as general
        badges on the sites themselves.\n \nFor the rank sort, bronze is greater than
        silver which is greater than gold. Along with sort=rank, set max=gold for
        just gold badges, max=silver&min=silver for just silver, and min=bronze for
        just bronze.\n \nrank is the default sort.\n \nThis method returns a list
        of badges."
      operationId: gets-all-explicitly-named-badges-in-the-system-a-named-badged-stands-in-opposition-to-a-tagbased-bad
      x-api-path-slug: badgesname-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: sort = rank => stringsort = name => string
      - in: query
        name: min
        description: sort = rank => stringsort = name => string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
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