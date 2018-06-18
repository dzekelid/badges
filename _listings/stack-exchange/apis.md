---
name: Stack Exchange
x-slug: stack-exchange
description: After someone asks a question, members of the community propose answers.
  Others vote on those answers. Very quickly, the answers with the most votes rise
  to the top. You don???t have to read through a lot of discussion to find the best
  answer.    Like to...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
x-kinRank: "8"
x-alexaRank: "126"
tags: Badges
created: "2018-06-17"
modified: "2018-06-17"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/apis.md
specificationVersion: "0.14"
apis:
- name: Stack Exchange Get Badges
  x-api-slug: stack-exchange
  description: "Returns all the badges in the system.\n \nBadge sorts are a tad complicated.
    For the purposes of sorting (and min/max) tag_based is considered to be greater
    than named.\n \nThis means that you can get a list of all tag based badges by
    passing min=tag_based, and conversely all the named badges by passing max=named,
    with sort=type.\n \nFor ranks, bronze is greater than silver which is greater
    than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver
    for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//badges
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badges-get-openapi.md
- name: Stack Exchange Get Badge Name
  x-api-slug: stack-exchange
  description: "Gets all explicitly named badges in the system.\n \nA named badged
    stands in opposition to a tag-based badge. These are referred to as general badges
    on the sites themselves.\n \nFor the rank sort, bronze is greater than silver
    which is greater than gold. Along with sort=rank, set max=gold for just gold badges,
    max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank
    is the default sort.\n \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//badges/name
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesname-get-openapi.md
- name: Stack Exchange Get Badge Recipients
  x-api-slug: stack-exchange
  description: "Returns recently awarded badges in the system.\n \nAs these badges
    have been awarded, they will have the badge.user property set.\n \nThis method
    returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//badges/recipients
  tags: Badges,Recipients
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesrecipients-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesrecipients-get-openapi.md
- name: Stack Exchange Get Badge Tags
  x-api-slug: stack-exchange
  description: "Returns the badges that are awarded for participation in specific
    tags.\n \nFor the rank sort, bronze is greater than silver which is greater than
    gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver
    for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//badges/tags
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgestags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgestags-get-openapi.md
- name: Stack Exchange Get Badge
  x-api-slug: stack-exchange
  description: "Gets the badges identified in id.\n \nNote that badge ids are not
    constant across sites, and thus should be looked up via the /badges method. A
    badge id on a single site is, however, guaranteed to be stable.\n \nBadge sorts
    are a tad complicated. For the purposes of sorting (and min/max) tag_based is
    considered to be greater than named.\n \nThis means that you can get a list of
    all tag based badges by passing min=tag_based, and conversely all the named badges
    by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver
    which is greater than gold. Along with sort=rank, set max=gold for just gold badges,
    max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank
    is the default sort.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for badge_id on badge objects.\n \nThis method
    returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//badges/{ids}
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesids-get-openapi.md
- name: Stack Exchange Get Badge Recipients
  x-api-slug: stack-exchange
  description: "Returns recently awarded badges in the system, constrained to a certain
    set of badges.\n \nAs these badges have been awarded, they will have the badge.user
    property set.\n \n{ids} can contain up to 100 semicolon delimited ids, to find
    ids programatically look for badge_id on badge objects.\n \nThis method returns
    a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//badges/{ids}/recipients
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesidsrecipients-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/badgesidsrecipients-get-openapi.md
- name: Stack Exchange My Badges
  x-api-slug: stack-exchange
  description: "Returns the badges earned by the user associated with the given access_token.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//me/badges
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/mebadges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/mebadges-get-openapi.md
- name: Stack Exchange Get User Badges
  x-api-slug: stack-exchange
  description: "Get the badges the users in {ids} have earned.\n \nBadge sorts are
    a tad complicated. For the purposes of sorting (and min/max) tag_based is considered
    to be greater than named.\n \nThis means that you can get a list of all tag based
    badges a user has by passing min=tag_based, and conversely all the named badges
    by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver
    which is greater than gold. Along with sort=rank, set max=gold for just gold badges,
    max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank
    is the default sort.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for user_id on user or shallow_user objects.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/badges
  tags: Users,Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/usersidsbadges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/usersidsbadges-get-openapi.md
- name: Stack Exchange
  x-api-slug: stack-exchange
  description: After someone asks a question, members of the community propose answers.
    Others vote on those answers. Very quickly, the answers with the most votes rise
    to the top. You don???t have to read through a lot of discussion to find the best
    answer.    Like to...
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Badges
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/badges/master/_listings/stack-exchange/openapi.md
x-common:
- type: x-authentication
  url: https://api.stackexchange.com/docs/authentication
- type: x-base
  url: https://api.stackexchange.com/
- type: x-blog
  url: http://stackexchange.com/blogs
- type: x-blog-rss
  url: http://blog.stackoverflow.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/stack-exchange
- type: x-crunchbase
  url: https://crunchbase.com/organization/stack-exchange
- type: x-developer
  url: http://api.stackexchange.com/
- type: x-email
  url: legal@stackexchange.com
- type: x-email
  url: team@stackexchange.com
- type: x-email
  url: team+api@stackexchange.com
- type: x-error-codes
  url: https://api.stackexchange.com/docs/error-handling
- type: x-github
  url: https://github.com/StackExchange
- type: x-javascript-sdk
  url: https://api.stackexchange.com/docs/js-lib
- type: x-privacy
  url: https://stackexchange.com/legal/privacy-policy
- type: x-rate-limits
  url: https://api.stackexchange.com/docs/throttle
- type: x-selfservice-registration
  url: https://stackapps.com/users/login?returnurl=/apps/oauth/register
- type: x-support
  url: https://stackexchange.com/about/contact
- type: x-terms-of-service
  url: http://stackexchange.com/legal/api-terms-of-use
- type: x-twitter
  url: https://twitter.com/StackExchange
- type: x-website
  url: http://stackexchange.com
- type: x-website
  url: https://stackexchange.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---