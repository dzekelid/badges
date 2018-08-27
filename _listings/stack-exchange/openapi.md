swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 1
info:
  title: Stack Exchange
  description: stack-exchange-is-a-network-of-130-qa-communities-including-stack-overflow-
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
  /badges/recipients:
    get:
      summary: Get Badge Recipients
      description: "Returns recently awarded badges in the system.\n \nAs these badges
        have been awarded, they will have the badge.user property set.\n \nThis method
        returns a list of badges."
      operationId: returns-recently-awarded-badges-in-the-system-as-these-badges-have-been-awarded-they-will-have-the-b
      x-api-path-slug: badgesrecipients-get
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
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Badges
      - Recipients
  /badges/tags:
    get:
      summary: Get Badge Tags
      description: "Returns the badges that are awarded for participation in specific
        tags.\n \nFor the rank sort, bronze is greater than silver which is greater
        than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver
        for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n
        \nThis method returns a list of badges."
      operationId: returns-the-badges-that-are-awarded-for-participation-in-specific-tags-for-the-rank-sort-bronze-is-g
      x-api-path-slug: badgestags-get
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
  /badges/{ids}:
    get:
      summary: Get Badge
      description: "Gets the badges identified in id.\n \nNote that badge ids are
        not constant across sites, and thus should be looked up via the /badges method.
        A badge id on a single site is, however, guaranteed to be stable.\n \nBadge
        sorts are a tad complicated. For the purposes of sorting (and min/max) tag_based
        is considered to be greater than named.\n \nThis means that you can get a
        list of all tag based badges by passing min=tag_based, and conversely all
        the named badges by passing max=named, with sort=type.\n \nFor ranks, bronze
        is greater than silver which is greater than gold. Along with sort=rank, set
        max=gold for just gold badges, max=silver&min=silver for just silver, and
        min=bronze for just bronze.\n \nrank is the default sort.\n \n{ids} can contain
        up to 100 semicolon delimited ids, to find ids programatically look for badge_id
        on badge objects.\n \nThis method returns a list of badges."
      operationId: gets-the-badges-identified-in-id-note-that-badge-ids-are-not-constant-across-sites-and-thus-should-b
      x-api-path-slug: badgesids-get
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
      - in: path
        name: ids
        description: Number list (semicolon delimited)
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
  /badges/{ids}/recipients:
    get:
      summary: Get Badge Recipients
      description: "Returns recently awarded badges in the system, constrained to
        a certain set of badges.\n \nAs these badges have been awarded, they will
        have the badge.user property set.\n \n{ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for badge_id on badge objects.\n
        \nThis method returns a list of badges."
      operationId: returns-recently-awarded-badges-in-the-system-constrained-to-a-certain-set-of-badges-as-these-badges
      x-api-path-slug: badgesidsrecipients-get
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
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Badges
  /me/badges:
    get:
      summary: My Badges
      description: "Returns the badges earned by the user associated with the given
        access_token.\n \nThis method returns a list of badges."
      operationId: returns-the-badges-earned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l
      x-api-path-slug: mebadges-get
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
  /users/{ids}/badges:
    get:
      summary: Get User Badges
      description: "Get the badges the users in {ids} have earned.\n \nBadge sorts
        are a tad complicated. For the purposes of sorting (and min/max) tag_based
        is considered to be greater than named.\n \nThis means that you can get a
        list of all tag based badges a user has by passing min=tag_based, and conversely
        all the named badges by passing max=named, with sort=type.\n \nFor ranks,
        bronze is greater than silver which is greater than gold. Along with sort=rank,
        set max=gold for just gold badges, max=silver&min=silver for just silver,
        and min=bronze for just bronze.\n \nrank is the default sort.\n \n{ids} can
        contain up to 100 semicolon delimited ids, to find ids programatically look
        for user_id on user or shallow_user objects.\n \nThis method returns a list
        of badges."
      operationId: get-the-badges-the-users-in-ids-have-earned-badge-sorts-are-a-tad-complicated-for-the-purposes-of-so
      x-api-path-slug: usersidsbadges-get
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
      - in: path
        name: ids
        description: Number list (semicolon delimited)
      - in: query
        name: max
        description: sort = rank => stringsort = name => stringsort = type => stringsort
          = awarded => date
      - in: query
        name: min
        description: sort = rank => stringsort = name => stringsort = type => stringsort
          = awarded => date
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
      - Users
      - Badges