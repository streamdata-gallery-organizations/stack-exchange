---
name: Stack Exchange
x-slug: stack-exchange
description: Stack Exchange is a network of question and answer websites on diverse
  topics in many different fields, each site covering a specific topic, where questions,
  answers, and users are subject to a reputation award process. The sites are modeled
  after Stack Overflow, a forum for computer programming questions that was the original
  site in this network. The reputation system is designed to allow the sites to be
  self-moderating.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
x-kinRank: "8"
x-alexaRank: ""
tags: Stack Exchange
created: "2018-05-22"
modified: "2018-05-22"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/apis.md
specificationVersion: "0.14"
apis:
- name: Stack Exchange Get Acces Tokens
  x-api-slug: stack-exchange
  description: "Reads the properties for a set of access tokens.\n \n{accessTokens}
    can contain up to 20 access tokens. These are obtained by authenticating a user
    using OAuth 2.0.\n \nThis method returns a list of access_tokens."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//access-tokens/{accessTokens}
  tags: Authentication,Access Tokens
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/accesstokensaccesstokens-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/accesstokensaccesstokens-get-openapi.md
- name: Stack Exchange Invalidate Acces Tokens
  x-api-slug: stack-exchange
  description: "Immediately expires the access tokens passed. This method is meant
    to allow an application to discard any active access tokens it no longer needs.\n
    \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating
    a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//access-tokens/{accessTokens}/invalidate
  tags: Authentication,Access Tokens
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/accesstokensaccesstokensinvalidate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/accesstokensaccesstokensinvalidate-get-openapi.md
- name: Stack Exchange Get Answers
  x-api-slug: stack-exchange
  description: "Returns all the undeleted answers in the system.\n \nThe sorts accepted
    by this method operate on the follow fields of the answer object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//answers
  tags: Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/answers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/answers-get-openapi.md
- name: Stack Exchange Get Answer
  x-api-slug: stack-exchange
  description: "Gets the set of answers identified by ids.\n \nThis is meant for batch
    fetcing of questions. A useful trick to poll for updates is to sort by activity,
    with a minimum date of the last time you polled.\n \n{ids} can contain up to 100
    semicolon delimited ids, to find ids programatically look for answer_id on answer
    objects.\n \nThe sorts accepted by this method operate on the follow fields of
    the answer object:\n - activity - last_activity_date\n - creation - creation_date\n
    - votes - score\n  activity is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//answers/{ids}
  tags: Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/answersids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/answersids-get-openapi.md
- name: Stack Exchange Get Answer Comments
  x-api-slug: stack-exchange
  description: "Gets the comments on a set of answers.\n \nIf you know that you have
    an answer id and need the comments, use this method. If you know you have a question
    id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for answer_id on answer objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the comment object:\n - creation - creation_date\n - votes
    - score\n  creation is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//answers/{ids}/comments
  tags: Answers,comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/answersidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/answersidscomments-get-openapi.md
- name: Stack Exchange De-Authenticate Token
  x-api-slug: stack-exchange
  description: "Passing valid access_tokens to this method causes the application
    that created them to be de-authorized by the user associated with each access_token.
    This will remove the application from their apps tab, and cause all other existing
    access_tokens to be destroyed.\n \nThis method is meant for uninstalling applications,
    recovering from access_token leaks, or simply as a stronger form of /access-tokens/{accessTokens}/invalidate.\n
    \nNothing prevents a user from re-authenticate to an application that has de-authenticated
    itself, the user will be prompted to approve the application again however.\n
    \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating
    a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//apps/{accessTokens}/de-authenticate
  tags: Authentication,Access Tokens
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/appsaccesstokensdeauthenticate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/appsaccesstokensdeauthenticate-get-openapi.md
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//badges
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badges-get-openapi.md
- name: Stack Exchange Get Badge Name
  x-api-slug: stack-exchange
  description: "Gets all explicitly named badges in the system.\n \nA named badged
    stands in opposition to a tag-based badge. These are referred to as general badges
    on the sites themselves.\n \nFor the rank sort, bronze is greater than silver
    which is greater than gold. Along with sort=rank, set max=gold for just gold badges,
    max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank
    is the default sort.\n \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//badges/name
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesname-get-openapi.md
- name: Stack Exchange Get Badge Recipients
  x-api-slug: stack-exchange
  description: "Returns recently awarded badges in the system.\n \nAs these badges
    have been awarded, they will have the badge.user property set.\n \nThis method
    returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//badges/recipients
  tags: Badges,Recipients
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesrecipients-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesrecipients-get-openapi.md
- name: Stack Exchange Get Badge Tags
  x-api-slug: stack-exchange
  description: "Returns the badges that are awarded for participation in specific
    tags.\n \nFor the rank sort, bronze is greater than silver which is greater than
    gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver
    for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//badges/tags
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgestags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgestags-get-openapi.md
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//badges/{ids}
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesids-get-openapi.md
- name: Stack Exchange Get Badge Recipients
  x-api-slug: stack-exchange
  description: "Returns recently awarded badges in the system, constrained to a certain
    set of badges.\n \nAs these badges have been awarded, they will have the badge.user
    property set.\n \n{ids} can contain up to 100 semicolon delimited ids, to find
    ids programatically look for badge_id on badge objects.\n \nThis method returns
    a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//badges/{ids}/recipients
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesidsrecipients-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/badgesidsrecipients-get-openapi.md
- name: Stack Exchange Get Comments
  x-api-slug: stack-exchange
  description: "Gets all the comments on the site.\n \nIf you're filtering for interesting
    comments (by score, creation date, etc.) make use of the sort paramter with appropriate
    min and max values.\n \nIf you're looking to query conversations between users,
    instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid} methods.\n
    \nThe sorts accepted by this method operate on the follow fields of the comment
    object:\n - creation - creation_date\n - votes - score\n  creation is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate.\n \nThis method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//comments
  tags: Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/comments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/comments-get-openapi.md
- name: Stack Exchange Get Comment
  x-api-slug: stack-exchange
  description: "Gets the comments identified in id.\n \nThis method is most useful
    if you have a cache of comment ids obtained through other means (such as /questions/{id}/comments)
    but suspect the data may be stale.\n \n{ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for comment_id on comment objects.\n \nThe
    sorts accepted by this method operate on the follow fields of the comment object:\n
    - creation - creation_date\n - votes - score\n  creation is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//comments/{ids}
  tags: Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/commentsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/commentsids-get-openapi.md
- name: Stack Exchange Delete Comment
  x-api-slug: stack-exchange
  description: "Deletes a comment.\n \nUse an access_token with write_access to delete
    a comment.\n \nIn practice, this method will never return an object."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//comments/{id}/delete
  tags: Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/commentsiddelete-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/commentsiddelete-post-openapi.md
- name: Stack Exchange Edit Comment
  x-api-slug: stack-exchange
  description: "Edit an existing comment.\n \nUse an access_token with write_access
    to edit an existing comment.\n \nThis method return the created comment."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//comments/{id}/edit
  tags: Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/commentsidedit-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/commentsidedit-post-openapi.md
- name: Stack Exchange Get Errors
  x-api-slug: stack-exchange
  description: "Returns the various error codes that can be produced by the API.\n
    \nThis method is provided for discovery, documentation, and testing purposes,
    it is not expected many applications will consume it during normal operation.\n
    \nFor testing purposes, look into the /errors/{id} method which simulates errors
    given a code.\n \nThis method returns a list of errors."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//errors
  tags: Errors
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/errors-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/errors-get-openapi.md
- name: Stack Exchange Get Error
  x-api-slug: stack-exchange
  description: "This method allows you to generate an error.\n \nThis method is only
    intended for use when testing an application or library. Unlike other methods
    in the API, its contract is not frozen, and new error codes may be added at any
    time.\n \nThis method results in an error, which will be expressed with a 400
    HTTP status code and setting the error* properties on the wrapper object."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//errors/{id}
  tags: Errors
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/errorsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/errorsid-get-openapi.md
- name: Stack Exchange Get Event
  x-api-slug: stack-exchange
  description: "Returns a stream of events that have occurred on the site.\n \nThe
    API considers the following \"events\":\n - posting a question\n - posting an
    answer\n - posting a comment\n - editing a post\n - creating a user\n  \n \nEvents
    are only accessible for 15 minutes after they occurred, and by default only events
    in the last 5 minutes are returned. You can specify the age of the oldest event
    returned by setting the since parameter.\n \nIt is advised that developers batch
    events by ids and make as few subsequent requests to other methods as possible.\n
    \nThis method returns a list of events."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//events
  tags: Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/events-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/events-get-openapi.md
- name: Stack Exchange Create Filter
  x-api-slug: stack-exchange
  description: "Creates a new filter given a list of includes, excludes, a base filter,
    and whether or not this filter should be \"unsafe\".\n \nFilter \"safety\" is
    defined as follows. Any string returned as a result of an API call with a safe
    filter will be inline-able into HTML without script-injection concerns. That is
    to say, no additional sanitizing (encoding, HTML tag stripping, etc.) will be
    necessary on returned strings. Applications that wish to handle sanitizing themselves
    should create an unsafe filter. All filters are safe by default, under the assumption
    that double-encoding bugs are more desirable than script injections.\n \nIf no
    base filter is specified, the default filter is assumed. When building a filter
    from scratch, the none built-in filter is useful.\n \nWhen the size of the parameters
    being sent to this method grows to large, problems can occur. This method will
    accept POST requests to mitigate this.\n \nIt is not expected that many applications
    will call this method at runtime, filters should be pre-calculated and \"baked
    in\" in the common cases. Furthermore, there are a number of built-in filters
    which cover common use cases.\n \nThis method returns a single filter."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//filters/create
  tags: Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/filterscreate-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/filterscreate-get-openapi.md
- name: Stack Exchange Get Filters
  x-api-slug: stack-exchange
  description: "Returns the fields included by the given filters, and the \"safeness\"
    of those filters.\n \nIt is not expected that this method will be consumed by
    many applications at runtime, it is provided to aid in debugging.\n \n{filters}
    can contain up to 20 semicolon delimited filters. Filters are obtained via calls
    to /filters/create, or by using a built-in filter.\n \nThis method returns a list
    of filters."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//filters/{filters}
  tags: Files
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/filtersfilters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/filtersfilters-get-openapi.md
- name: Stack Exchange Get Inbox
  x-api-slug: stack-exchange
  description: "Returns a user's inbox.\n \nThis method requires an access_token,
    with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox
    items."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//inbox
  tags: Email,Inbox
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/inbox-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/inbox-get-openapi.md
- name: Stack Exchange Unread Inbox
  x-api-slug: stack-exchange
  description: "Returns the unread items in a user's inbox.\n \nThis method requires
    an access_token, with a scope containing \"read_inbox\".\n \nThis method returns
    a list of inbox items."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//inbox/unread
  tags: Email,Inbox
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/inboxunread-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/inboxunread-get-openapi.md
- name: Stack Exchange Get Information
  x-api-slug: stack-exchange
  description: "Returns a collection of statistics about the site.\n \nData to facilitate
    per-site customization, discover related sites, and aggregate statistics is all
    returned by this method.\n \nThis data is cached very aggressively, by design.
    Query sparingly, ideally no more than once an hour.\n \nThis method returns an
    info object."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//info
  tags: Information
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/info-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/info-get-openapi.md
- name: Stack Exchange Get Me
  x-api-slug: stack-exchange
  description: "Returns the user associated with the passed access_token.\n \nThis
    method returns a user."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me
  tags: Self
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/me-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/me-get-openapi.md
- name: Stack Exchange My Answers
  x-api-slug: stack-exchange
  description: "Returns the answers owned by the user associated with the given access_token.\n
    \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/answers
  tags: Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meanswers-get-openapi.md
- name: Stack Exchange My Assocated
  x-api-slug: stack-exchange
  description: "Returns all of a user's associated accounts, given an access_token
    for them.\n \nThis method returns a list of network users."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/associated
  tags: Associated
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meassociated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meassociated-get-openapi.md
- name: Stack Exchange My Badges
  x-api-slug: stack-exchange
  description: "Returns the badges earned by the user associated with the given access_token.\n
    \nThis method returns a list of badges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/badges
  tags: Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mebadges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mebadges-get-openapi.md
- name: Stack Exchange My Comments
  x-api-slug: stack-exchange
  description: "Returns the comments owned by the user associated with the given access_token.\n
    \nThis method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/comments
  tags: Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mecomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mecomments-get-openapi.md
- name: Stack Exchange My Comments
  x-api-slug: stack-exchange
  description: "Returns the comments owned by the user associated with the given access_token
    that are in reply to the user identified by {toId}.\n \nThis method returns a
    list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/comments/{toId}
  tags: Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mecommentstoid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mecommentstoid-get-openapi.md
- name: Stack Exchange My Favorites
  x-api-slug: stack-exchange
  description: "Returns the questions favorites by the user associated with the given
    access_token.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/favorites
  tags: Favorites
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mefavorites-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mefavorites-get-openapi.md
- name: Stack Exchange My Inbox
  x-api-slug: stack-exchange
  description: "Returns the user identified by access_token's inbox.\n \nThis method
    requires an access_token, with a scope containing \"read_inbox\".\n \nThis method
    returns a list of inbox items."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/inbox
  tags: Email,Inbox
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meinbox-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meinbox-get-openapi.md
- name: Stack Exchange My Inbox Unread
  x-api-slug: stack-exchange
  description: "Returns the unread items in the user identified by access_token's
    inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n
    \nThis method returns a list of inbox items."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/inbox/unread
  tags: Email,Inbox
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meinboxunread-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meinboxunread-get-openapi.md
- name: Stack Exchange My Mentions
  x-api-slug: stack-exchange
  description: "Returns the comments mentioning the user associated with the given
    access_token.\n \nThis method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/mentioned
  tags: Mentioned
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mementioned-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mementioned-get-openapi.md
- name: Stack Exchange My Merges
  x-api-slug: stack-exchange
  description: "Returns a record of merges that have occurred involving a user identified
    by an access_token.\n \nThis method allows you to take now invalid account ids
    and find what account they've become, or take currently valid account ids and
    find which ids were equivalent in the past.\n \nThis is most useful when confirming
    that an account_id is in fact \"new\" to an application.\n \nAccount merges can
    happen for a wide range of reasons, applications should not make assumptions that
    merges have particular causes.\n \nNote that accounts are managed at a network
    level, users on a site may be merged due to an account level merge but there is
    no guarantee that a merge has an effect on any particular site.\n \nThis method
    returns a list of account_merge."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/merges
  tags: Merges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/memerges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/memerges-get-openapi.md
- name: Stack Exchange My Notiications
  x-api-slug: stack-exchange
  description: "Returns a user's notifications, given an access_token.\n \nThis method
    requires an access_token, with a scope containing \"read_inbox\".\n \nThis method
    returns a list of notifications."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/notifications
  tags: Notifications
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/menotifications-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/menotifications-get-openapi.md
- name: Stack Exchange My Notiications Unread
  x-api-slug: stack-exchange
  description: "Returns a user's unread notifications, given an access_token.\n \nThis
    method requires an access_token, with a scope containing \"read_inbox\".\n \nThis
    method returns a list of notifications."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/notifications/unread
  tags: Notifications
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/menotificationsunread-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/menotificationsunread-get-openapi.md
- name: Stack Exchange My Priveleges
  x-api-slug: stack-exchange
  description: "Returns the privileges the user identified by access_token has.\n
    \nThis method returns a list of privileges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/privileges
  tags: Privileges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meprivileges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/meprivileges-get-openapi.md
- name: Stack Exchange My Questions
  x-api-slug: stack-exchange
  description: "Returns the questions owned by the user associated with the given
    access_token.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/questions
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestions-get-openapi.md
- name: Stack Exchange My Questions Featured
  x-api-slug: stack-exchange
  description: "Returns the questions that have active bounties offered by the user
    associated with the given access_token.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/questions/featured
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsfeatured-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsfeatured-get-openapi.md
- name: Stack Exchange My Questions No Answers
  x-api-slug: stack-exchange
  description: "Returns the questions owned by the user associated with the given
    access_token that have no answers.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/questions/no-answers
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsnoanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsnoanswers-get-openapi.md
- name: Stack Exchange My Questions Unaccepted
  x-api-slug: stack-exchange
  description: "Returns the questions owned by the user associated with the given
    access_token that have no accepted answer.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/questions/unaccepted
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsunaccepted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsunaccepted-get-openapi.md
- name: Stack Exchange My Questions Unanswered
  x-api-slug: stack-exchange
  description: "Returns the questions owned by the user associated with the given
    access_token that are not considered answered.\n \nThis method returns a list
    of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/questions/unanswered
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsunanswered-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mequestionsunanswered-get-openapi.md
- name: Stack Exchange My Reputation
  x-api-slug: stack-exchange
  description: "Returns the reputation changed for the user associated with the given
    access_token.\n \nThis method returns a list of reputation changes."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/reputation
  tags: Reputation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mereputation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mereputation-get-openapi.md
- name: Stack Exchange My Reputation History
  x-api-slug: stack-exchange
  description: "Returns user's public reputation history.\n \nThis method returns
    a list of reputation_history."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/reputation-history
  tags: Reputation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mereputationhistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mereputationhistory-get-openapi.md
- name: Stack Exchange My Reputation History Full
  x-api-slug: stack-exchange
  description: "Returns user's full reputation history, including private events.\n
    \n This method requires an access_token, with a scope containing \"private_info\".\n
    \nThis method returns a list of reputation_history."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/reputation-history/full
  tags: Reputation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mereputationhistoryfull-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mereputationhistoryfull-get-openapi.md
- name: Stack Exchange Suggested Edits
  x-api-slug: stack-exchange
  description: "Returns the suggested edits the user identified by access_token has
    submitted.\n \nThis method returns a list of suggested-edits."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/suggested-edits
  tags: Suggested Edits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mesuggestededits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mesuggestededits-get-openapi.md
- name: Stack Exchange My Tags
  x-api-slug: stack-exchange
  description: "Returns the tags the user identified by the access_token passed is
    active in.\n \nThis method returns a list of tags."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/tags
  tags: Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metags-get-openapi.md
- name: Stack Exchange My Tags Top Answers
  x-api-slug: stack-exchange
  description: "Returns the top 30 answers the user associated with the given access_token
    has posted in response to questions with the given tags.\n \nThis method returns
    a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/tags/{tags}/top-answers
  tags: Tags,Anwers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metagstagstopanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metagstagstopanswers-get-openapi.md
- name: Stack Exchange My Tags Top Questions
  x-api-slug: stack-exchange
  description: "Returns the top 30 questions the user associated with the given access_token
    has posted in response to questions with the given tags.\n \nThis method returns
    a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/tags/{tags}/top-questions
  tags: Tags,Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metagstagstopquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metagstagstopquestions-get-openapi.md
- name: Stack Exchange My Timeline
  x-api-slug: stack-exchange
  description: "Returns a subset of the actions the user identified by the passed
    access_token has taken on the site.\n \nThis method returns a list of user timeline
    objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/timeline
  tags: Tags,Timeline
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metimeline-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metimeline-get-openapi.md
- name: Stack Exchange My Top Answer Tags
  x-api-slug: stack-exchange
  description: "Returns the user identified by access_token's top 30 tags by answer
    score.\n \nThis method returns a list of top tag objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/top-answer-tags
  tags: Tags,Anwers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metopanswertags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metopanswertags-get-openapi.md
- name: Stack Exchange My Top Question Tags
  x-api-slug: stack-exchange
  description: "Returns the user identified by access_token's top 30 tags by question
    score.\n \nThis method returns a list of top tag objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/top-question-tags
  tags: Tags,Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metopquestiontags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/metopquestiontags-get-openapi.md
- name: Stack Exchange My Write Permissions
  x-api-slug: stack-exchange
  description: "Returns the write permissions a user has via the api, given an access
    token.\n \nThe Stack Exchange API gives users the ability to create, edit, and
    delete certain types. This method returns whether the passed user is capable of
    performing those actions at all, as well as how many times a day they can.\n \nThis
    method does not consider the user's current quota (ie. if they've already exhausted
    it for today) nor any additional restrictions on write access, such as editing
    deleted comments.\n \nThis method returns a list of write_permissions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//me/write-permissions
  tags: Write Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mewritepermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/mewritepermissions-get-openapi.md
- name: Stack Exchange Get Notifications
  x-api-slug: stack-exchange
  description: "Returns a user's notifications.\n \nThis method requires an access_token,
    with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//notifications
  tags: Notifications
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/notifications-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/notifications-get-openapi.md
- name: Stack Exchange Get Notifications Unread
  x-api-slug: stack-exchange
  description: "Returns a user's unread notifications.\n \nThis method requires an
    access_token, with a scope containing \"read_inbox\".\n \nThis method returns
    a list of notifications."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//notifications/unread
  tags: Notifications
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/notificationsunread-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/notificationsunread-get-openapi.md
- name: Stack Exchange Get Posts
  x-api-slug: stack-exchange
  description: "Fetches all posts (questions and answers) on the site.\n \nIn many
    ways this method is the union of /questions and /answers, returning both sets
    of data albeit only the common fields.\n \nMost applications should use the question
    or answer specific methods, but /posts is available for those rare cases where
    any activity is of intereset. Examples of such queries would be: \"all posts on
    Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n \nThe sorts accepted
    by this method operate on the follow fields of the post object:\n - activity -
    last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    posts."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//posts
  tags: Posts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/posts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/posts-get-openapi.md
- name: Stack Exchange Get Post
  x-api-slug: stack-exchange
  description: "Fetches a set of posts by ids.\n \nThis method is meant for grabbing
    an object when unsure whether an id identifies a question or an answer. This is
    most common with user entered data.\n \n{ids} can contain up to 100 semicolon
    delimited ids, to find ids programatically look for post_id, answer_id, or question_id
    on post, answer, and question objects respectively.\n \nThe sorts accepted by
    this method operate on the follow fields of the post object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of posts."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}
  tags: Posts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsids-get-openapi.md
- name: Stack Exchange Get Post Comments
  x-api-slug: stack-exchange
  description: "Gets the comments on the posts identified in ids, regardless of the
    type of the posts.\n \nThis method is meant for cases when you are unsure of the
    type of the post id provided. Generally, this would be due to obtaining the post
    id directly from a user.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for post_id, answer_id, or question_id on post,
    answer, and question objects respectively.\n \nThe sorts accepted by this method
    operate on the follow fields of the comment object:\n - creation - creation_date\n
    - votes - score\n  creation is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}/comments
  tags: Posts,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidscomments-get-openapi.md
- name: Stack Exchange Get Post Revisions
  x-api-slug: stack-exchange
  description: "Returns edit revisions for the posts identified in ids.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n
    \nThis method returns a list of revisions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}/revisions
  tags: Posts,Revisions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidsrevisions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidsrevisions-get-openapi.md
- name: Stack Exchange Get Posts Suggested Edits
  x-api-slug: stack-exchange
  description: "Returns suggsted edits on the posts identified in ids.\n \n - creation
    - creation_date\n - approval - approval_date\n - rejection - rejection_date\n
    \ creation is the default sort.\n \n {ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for post_id, answer_id, or question_id on
    post, answer, and question objects respectively.\n \nThis method returns a list
    of suggested-edits."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}/suggested-edits
  tags: Posts,Suggested Edits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidssuggestededits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidssuggestededits-get-openapi.md
- name: Stack Exchange Add Comment Post
  x-api-slug: stack-exchange
  description: "Create a new comment.\n \nUse an access_token with write_access to
    create a new comment on a post.\n \nThis method returns the created comment."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//posts/{id}/comments/add
  tags: Posts,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidcommentsadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/postsidcommentsadd-post-openapi.md
- name: Stack Exchange Get Privileges
  x-api-slug: stack-exchange
  description: "Returns the earnable privileges on a site.\n \nPrivileges define abilities
    a user can earn (via reputation) on any Stack Exchange site.\n \nWhile fairly
    stable, over time they do change. New ones are introduced with new features, and
    the reputation requirements change as a site matures.\n \nThis method returns
    a list of privileges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//privileges
  tags: Privileges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/privileges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/privileges-get-openapi.md
- name: Stack Exchange Get Questions
  x-api-slug: stack-exchange
  description: "Gets all the questions on the site.\n \nThis method allows you make
    fairly flexible queries across the entire corpus of questions on a site. For example,
    getting all questions asked in the the week of Jan 1st 2011 with scores of 10
    or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n
    \nTo constrain questions returned to those with a set of tags, use the tagged
    parameter with a semi-colon delimited list of tags. This is an and contraint,
    passing tagged=c;java will return only those questions with both tags. As such,
    passing more than 5 tags will always return zero results.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n - hot -
    by the formula ordering the hot tab Does not accept min or max\n - week - by the
    formula ordering the week tab Does not accept min or max\n - month - by the formula
    ordering the month tab Does not accept min or max\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questions-get-openapi.md
- name: Stack Exchange Get Questions Featured
  x-api-slug: stack-exchange
  description: "Returns all the questions with active bounties in the system.\n \nThe
    sorts accepted by this method operate on the follow fields of the question object:\n
    - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
    \ activity is the default sort.\n \n It is possible to create moderately complex
    queries using sort, min, max, fromdate, and todate.\n \nThis method returns a
    list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/featured
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsfeatured-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsfeatured-get-openapi.md
- name: Stack Exchange Get Questions No Answers
  x-api-slug: stack-exchange
  description: "Returns questions which have received no answers.\n \nCompare with
    /questions/unanswered which mearly returns questions that the sites consider insufficiently
    well answered.\n \nThis method corresponds roughly with the this site tab.\n \nTo
    constrain questions returned to those with a set of tags, use the tagged parameter
    with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java
    will return only those questions with both tags. As such, passing more than 5
    tags will always return zero results.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/no-answers
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsnoanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsnoanswers-get-openapi.md
- name: Stack Exchange Get Questions Unanswered
  x-api-slug: stack-exchange
  description: "Returns questions the site considers to be unanswered.\n \nNote that
    just because a question has an answer, that does not mean it is considered answered.
    While the rules are subject to change, at this time a question must have at least
    one upvoted answer to be considered answered.\n \nTo constrain questions returned
    to those with a set of tags, use the tagged parameter with a semi-colon delimited
    list of tags. This is an and contraint, passing tagged=c;java will return only
    those questions with both tags. As such, passing more than 5 tags will always
    return zero results.\n \nCompare with /questions/no-answers.\n \nThis method corresponds
    roughly with the unanswered tab.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/unanswered
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsunanswered-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsunanswered-get-openapi.md
- name: Stack Exchange Get Questions
  x-api-slug: stack-exchange
  description: "Returns the questions identified in {ids}.\n \nThis is most useful
    for fetching fresh data when maintaining a cache of question ids, or polling for
    changes.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids
    programatically look for question_id on question objects.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}
  tags: Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsids-get-openapi.md
- name: Stack Exchange Get Question Answers
  x-api-slug: stack-exchange
  description: "Gets the answers to a set of questions identified in id.\n \nThis
    method is most useful if you have a set of interesting questions, and you wish
    to obtain all of their answers at once or if you are polling for new or updates
    answers (in conjunction with sort=activity).\n \n{ids} can contain up to 100 semicolon
    delimited ids, to find ids programatically look for question_id on question objects.\n
    \nThe sorts accepted by this method operate on the follow fields of the answer
    object:\n - activity - last_activity_date\n - creation - creation_date\n - votes
    - score\n  activity is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}/answers
  tags: Questions,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidsanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidsanswers-get-openapi.md
- name: Stack Exchange Get Question Comments
  x-api-slug: stack-exchange
  description: "Gets the comments on a question.\n \nIf you know that you have an
    question id and need the comments, use this method. If you know you have a answer
    id, use /answers/{ids}/comments. If you are unsure, use /posts/{ids}/comments.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for question_id on question objects.\n \nThe sorts accepted by this method
    operate on the follow fields of the comment object:\n - creation - creation_date\n
    - votes - score\n  creation is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}/comments
  tags: Questions,Linked
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidscomments-get-openapi.md
- name: Stack Exchange Get Question Linked
  x-api-slug: stack-exchange
  description: "Gets questions which link to those questions identified in {ids}.\n
    \nThis method only considers questions that are linked within a site, and will
    never return questions from another Stack Exchange site.\n \nA question is considered
    \"linked\" when it explicitly includes a hyperlink to another question, there
    are no other heuristics.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for question_id on question objects.\n \nThe
    sorts accepted by this method operate on the follow fields of the question object:\n
    - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
    - rank - a priority sort by site applies, subject to change at any time Does not
    accept min or max\n  activity is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}/linked
  tags: Questions,Linked
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidslinked-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidslinked-get-openapi.md
- name: Stack Exchange Get Question Related
  x-api-slug: stack-exchange
  description: "Returns questions that the site considers related to those identified
    in {ids}.\n \nThe algorithm for determining if questions are related is not documented,
    and subject to change at any time. Futhermore, these values are very heavily cached,
    and may not update immediately after a question has been editted. It is also not
    guaranteed that a question will be considered related to any number (even non-zero)
    of questions, and a consumer should be able to handle a variable number of returned
    questions.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids
    programatically look for question_id on question objects.\n \nThe sorts accepted
    by this method operate on the follow fields of the question object:\n - activity
    - last_activity_date\n - creation - creation_date\n - votes - score\n - rank -
    a priority sort by site applies, subject to change at any time Does not accept
    min or max\n  activity is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}/related
  tags: Questions,Related
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidsrelated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidsrelated-get-openapi.md
- name: Stack Exchange Get Question AnsweTimeliners
  x-api-slug: stack-exchange
  description: "Returns a subset of the events that have happened to the questions
    identified in id.\n \nThis provides data similar to that found on a question's
    timeline page.\n \nVoting data is scrubbed to deter inferencing of voter identity.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for question_id on question objects.\n \nThis method returns a list of question
    timeline events."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//questions/{ids}/timeline
  tags: Questions,Timeline
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidstimeline-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/questionsidstimeline-get-openapi.md
- name: Stack Exchange Get Revisions
  x-api-slug: stack-exchange
  description: "Returns edit revisions identified by ids in {ids}.\n \n{ids} can contain
    up to 20 semicolon delimited ids, to find ids programatically look for revision_guid
    on revision objects. Note that unlike most other id types in the API, revision_guid
    is a string.\n \nThis method returns a list of revisions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//revisions/{ids}
  tags: Revisions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/revisionsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/revisionsids-get-openapi.md
- name: Stack Exchange Search
  x-api-slug: stack-exchange
  description: "Searches a site for any questions which fit the given criteria.\n
    \nThis method is intentionally quite limited. For more general searching, you
    should use a proper internet search engine restricted to the domain of the site
    in question.\n \nAt least one of tagged or intitle must be set on this method.
    nottagged is only used if tagged is also set, for performance reasons.\n \ntagged
    and nottagged are semi-colon delimited list of tags. At least 1 tag in tagged
    will be on each returned question if it is passed, making it the OR equivalent
    of the AND version of tagged on /questions.\n \nThe sorts accepted by this method
    operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n - relevance - matches the relevance
    tab on the site itself Does not accept min or max\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//search
  tags: Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/search-get-openapi.md
- name: Stack Exchange Advanced Search
  x-api-slug: stack-exchange
  description: "Searches a site for any questions which fit the given criteria.\n
    \nSearch criteria are expressed using the following parameters:\n  - q - a free
    form text parameter, will match all question properties based on an undocumented
    algorithm.\n - accepted - true to return only questions with accepted answers,
    false to return only those without. Omit to elide constraint.\n - answers - the
    minimum number of answers returned questions must have.\n - body - text which
    must appear in returned questions' bodies.\n - closed - true to return only closed
    questions, false to return only open ones. Omit to elide constraint.\n - migrated
    - true to return only questions migrated away from a site, false to return only
    those not. Omit to elide constraint.\n - notice - true to return only questions
    with post notices, false to return only those without. Omit to elide constraint.\n
    - nottagged - a semicolon delimited list of tags, none of which will be present
    on returned questions.\n - tagged - a semicolon delimited list of tags, of which
    at least one will be present on all returned questions.\n - title - text which
    must appear in returned questions' titles.\n - user - the id of the user who must
    own the questions returned.\n - url - a url which must be contained in a post,
    may include a wildcard.\n - views - the minimum number of views returned questions
    must have.\n - wiki - true to return only community wiki questions, false to return
    only non-community wiki ones. Omit to elide constraint.\n  \nAt least one additional
    parameter must be set if nottagged is set, for performance reasons.\n \nThe sorts
    accepted by this method operate on the follow fields of the question object:\n
    - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
    - relevance - matches the relevance tab on the site itself Does not accept min
    or max\n  activity is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//search/advanced
  tags: Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/searchadvanced-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/searchadvanced-get-openapi.md
- name: Stack Exchange Get Similar
  x-api-slug: stack-exchange
  description: "Returns questions which are similar to a hypothetical one based on
    a title and tag combination.\n \nThis method is roughly equivalent to a site's
    related questions suggestion on the ask page.\n \nThis method is useful for correlating
    data outside of a Stack Exchange site with similar content within one.\n \nNote
    that title must always be passed as a parameter. tagged and nottagged are optional,
    semi-colon delimited lists of tags.\n \nIf tagged is passed it is treated as a
    preference, there is no guarantee that questions returned will have any of those
    tags. nottagged is treated as a requirement, no questions will be returned with
    those tags.\n \nThe sorts accepted by this method operate on the follow fields
    of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
    - votes - score\n - relevance - order by \"how similar\" the questions are, most
    likely candidate first with a descending order Does not accept min or max\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//similar
  tags: Similar
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/similar-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/similar-get-openapi.md
- name: Stack Exchange Get Sites
  x-api-slug: stack-exchange
  description: "Returns all sites in the network.\n \nThis method allows for discovery
    of new sites, and changes to existing ones. Be aware that unlike normal API methods,
    this method should be fetched very infrequently, it is very unusual for these
    values to change more than once on any given day. It is suggested that you cache
    its return for at least one day, unless your app encounters evidence that it has
    changed (such as from the /info method).\n \nThe pagesize parameter for this method
    is unbounded, in acknowledgement that for many applications repeatedly fetching
    from /sites would complicate start-up tasks needlessly.\n \nThis method returns
    a list of sites."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//sites
  tags: Sites
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/sites-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/sites-get-openapi.md
- name: Stack Exchange Get Suggested Edits
  x-api-slug: stack-exchange
  description: "Returns all the suggested edits in the systems.\n \nThis method returns
    a list of suggested-edits.\n \nThe sorts accepted by this method operate on the
    follow fields of the suggested_edit object:\n - creation - creation_date\n - approval
    - approval_date Does not return unapproved suggested_edits\n - rejection - rejection_date
    Does not return unrejected suggested_edits\n  creation is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//suggested-edits
  tags: Suggested Edits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/suggestededits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/suggestededits-get-openapi.md
- name: Stack Exchange Get Suggested Edit
  x-api-slug: stack-exchange
  description: "Returns suggested edits identified in ids.\n \n{ids} can contain up
    to 100 semicolon delimited ids, to find ids programatically look for suggested_edit_id
    on suggested_edit objects.\n \nThe sorts accepted by this method operate on the
    follow fields of the suggested_edit object:\n - creation - creation_date\n - approval
    - approval_date Does not return unapproved suggested_edits\n - rejection - rejection_date
    Does not return unrejected suggested_edits\n  creation is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of suggested-edits."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//suggested-edits/{ids}
  tags: Suggested Edits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/suggestededitsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/suggestededitsids-get-openapi.md
- name: Stack Exchange Get Tags
  x-api-slug: stack-exchange
  description: "Returns the tags found on a site.\n \nThe inname parameter lets a
    consumer filter down to tags that contain a certain substring. For example, inname=own
    would return both \"download\" and \"owner\" amongst others.\n \nThis method returns
    a list of tags.\n \nThe sorts accepted by this method operate on the follow fields
    of the tag object:\n - popular - count\n - activity - the creation_date of the
    last question asked with the tag\n - name - name\n  popular is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags
  tags: Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tags-get-openapi.md
- name: Stack Exchange Get Tags Moderator Only
  x-api-slug: stack-exchange
  description: "Returns the tags found on a site that only moderators can use.\n \nThe
    inname parameter lets a consumer filter down to tags that contain a certain substring.
    For example, inname=own would return both \"download\" and \"owner\" amongst others.\n
    \nThis method returns a list of tags.\n \nThe sorts accepted by this method operate
    on the follow fields of the tag object:\n - popular - count\n - activity - the
    creation_date of the last question asked with the tag\n - name - name\n  popular
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/moderator-only
  tags: Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagsmoderatoronly-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagsmoderatoronly-get-openapi.md
- name: Stack Exchange Get Tags Requred
  x-api-slug: stack-exchange
  description: "Returns the tags found on a site that fulfill required tag constraints
    on questions.\n \nThe inname parameter lets a consumer filter down to tags that
    contain a certain substring. For example, inname=own would return both \"download\"
    and \"owner\" amongst others.\n \nThis method returns a list of tags.\n \nThe
    sorts accepted by this method operate on the follow fields of the tag object:\n
    - popular - count\n - activity - the creation_date of the last question asked
    with the tag\n - name - name\n  popular is the default sort.\n \n It is possible
    to create moderately complex queries using sort, min, max, fromdate, and todate."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/required
  tags: Tags,Required
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagsrequired-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagsrequired-get-openapi.md
- name: Stack Exchange Get Tags Synonyms
  x-api-slug: stack-exchange
  description: "Returns all tag synonyms found a site.\n \nWhen searching for synonyms
    of specific tags, it is better to use /tags/{tags}/synonyms over this method.\n
    \nThe sorts accepted by this method operate on the follow fields of the tag_synonym
    object:\n - creation - creation_date\n - applied - applied_count\n - activity
    - last_applied_date\n  creation is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of tag_synonyms."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/synonyms
  tags: Tags,Synonyms
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagssynonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagssynonyms-get-openapi.md
- name: Stack Exchange Get Tags FAQ
  x-api-slug: stack-exchange
  description: "Returns the frequently asked questions for the given set of tags in
    {tags}.\n \nFor a question to be returned, it must have all the tags in {tags}
    and be considered \"frequently asked\". The exact algorithm for determining whether
    a question is considered a FAQ is subject to change at any time.\n \n{tags} can
    contain up to 5 individual tags per request.\n \nThis method returns a list of
    questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tags}/faq
  tags: Tags,FAQ
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagsfaq-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagsfaq-get-openapi.md
- name: Stack Exchange Get Tags Info
  x-api-slug: stack-exchange
  description: "Returns tag objects representing the tags in {tags} found on the site.\n
    \nThis method diverges from the standard naming patterns to avoid to conflicting
    with existing methods, due to the free form nature of tag names.\n \nThis method
    returns a list of tags.\n \nThe sorts accepted by this method operate on the follow
    fields of the tag object:\n - popular - count\n - activity - the creation_date
    of the last question asked with the tag\n - name - name\n  popular is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tags}/info
  tags: Tags,Information
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagsinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagsinfo-get-openapi.md
- name: Stack Exchange Get Tags Related
  x-api-slug: stack-exchange
  description: "Returns the tags that are most related to those in {tags}.\n \nIncluding
    multiple tags in {tags} is equivalent to asking for \"tags related to tag #1 and
    tag #2\" not \"tags related to tag #1 or tag #2\".\n \ncount on tag objects returned
    is the number of question with that tag that also share all those in {tags}.\n
    \n{tags} can contain up to 4 individual tags per request.\n \nThis method returns
    a list of tags."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tags}/related
  tags: Tags,Related
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagsrelated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagsrelated-get-openapi.md
- name: Stack Exchange Get Tags Synonyms
  x-api-slug: stack-exchange
  description: "Gets all the synonyms that point to the tags identified in {tags}.
    If you're looking to discover all the tag synonyms on a site, use the /tags/synonyms
    methods instead of call this method on all tags.\n \n{tags} can contain up to
    20 individual tags per request.\n \nThe sorts accepted by this method operate
    on the follow fields of the tag_synonym object:\n - creation - creation_date\n
    - applied - applied_count\n - activity - last_applied_date\n  creation is the
    default sort.\n \n It is possible to create moderately complex queries using sort,
    min, max, fromdate, and todate.\n \nThis method returns a list of tag synonyms."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tags}/synonyms
  tags: Tags,Synonyms
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagssynonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagssynonyms-get-openapi.md
- name: Stack Exchange Get Tags Wikis
  x-api-slug: stack-exchange
  description: "Returns the wikis that go with the given set of tags in {tags}.\n
    \nBe aware that not all tags have wikis.\n \n{tags} can contain up to 20 individual
    tags per request.\n \nThis method returns a list of tag wikis."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tags}/wikis
  tags: Tags,Wikis
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagswikis-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagswikis-get-openapi.md
- name: Stack Exchange Get Tags Top Answers
  x-api-slug: stack-exchange
  description: "Returns the top 30 answerers active in a single tag, of either all-time
    or the last 30 days.\n \nThis is a view onto the data presented on the tag info
    page on the sites.\n \nThis method returns a list of tag score objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tag}/top-answerers/{period}
  tags: Tags,Top Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagtopanswerersperiod-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagtopanswerersperiod-get-openapi.md
- name: Stack Exchange Get Tags Top Askers
  x-api-slug: stack-exchange
  description: "Returns the top 30 askers active in a single tag, of either all-time
    or the last 30 days.\n \nThis is a view onto the data presented on the tag info
    page on the sites.\n \nThis method returns a list of tag score objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//tags/{tag}/top-askers/{period}
  tags: Tags,Top Askers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagtopaskersperiod-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/tagstagtopaskersperiod-get-openapi.md
- name: Stack Exchange Get Users
  x-api-slug: stack-exchange
  description: "Returns all users on a site.\n \nThis method returns a list of users.\n
    \nThe sorts accepted by this method operate on the follow fields of the user object:\n
    - reputation - reputation\n - creation - creation_date\n - name - display_name\n
    - modified - last_modified_date\n  reputation is the default sort.\n \n It is
    possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThe inname parameter lets consumers filter the results down to
    just those users with a certain substring in their display name. For example,
    inname=kevin will return all users with both users named simply \"Kevin\" or those
    with Kevin as one of (or part of) their names; such as \"Kevin Montrose\"."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users
  tags: Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/users-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/users-get-openapi.md
- name: Stack Exchange Get User Moderators
  x-api-slug: stack-exchange
  description: "Gets those users on a site who can exercise moderation powers.\n \nNote,
    employees of Stack Exchange Inc. will be returned if they have been granted moderation
    powers on a site even if they have never been appointed or elected explicitly.
    This method checks abilities, not the manner in which they were obtained.\n \nThe
    sorts accepted by this method operate on the follow fields of the user object:\n
    - reputation - reputation\n - creation - creation_date\n - name - display_name\n
    - modified - last_modified_date\n  reputation is the default sort.\n \n It is
    possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of users."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/moderators
  tags: Users,Moderators
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersmoderators-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersmoderators-get-openapi.md
- name: Stack Exchange Get Users Moderators Elected
  x-api-slug: stack-exchange
  description: "Returns those users on a site who both have moderator powers, and
    were actually elected.\n \nThis method excludes Stack Exchange Inc. employees,
    unless they were actually elected moderators on a site (which can only have happened
    prior to their employment).\n \nThe sorts accepted by this method operate on the
    follow fields of the user object:\n - reputation - reputation\n - creation - creation_date\n
    - name - display_name\n - modified - last_modified_date\n  reputation is the default
    sort.\n \n It is possible to create moderately complex queries using sort, min,
    max, fromdate, and todate.\n \nThis method returns a list of users."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/moderators/elected
  tags: Users,Moderators
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersmoderatorselected-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersmoderatorselected-get-openapi.md
- name: Stack Exchange Get User
  x-api-slug: stack-exchange
  description: "Gets the users identified in ids in {ids}.\n \nTypically this method
    will be called to fetch user profiles when you have obtained user ids from some
    other source, such as /questions.\n \n{ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for user_id on user or shallow_user objects.\n
    \nThe sorts accepted by this method operate on the follow fields of the user object:\n
    - reputation - reputation\n - creation - creation_date\n - name - display_name\n
    - modified - last_modified_date\n  reputation is the default sort.\n \n It is
    possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of users."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}
  tags: Users
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersids-get-openapi.md
- name: Stack Exchange Get User Answers
  x-api-slug: stack-exchange
  description: "Returns the answers the users in {ids} have posted.\n \n{ids} can
    contain up to 100 semicolon delimited ids, to find ids programatically look for
    user_id on user or shallow_user objects.\n \nThe sorts accepted by this method
    operate on the follow fields of the answer object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/answers
  tags: Users,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsanswers-get-openapi.md
- name: Stack Exchange Get User Associated
  x-api-slug: stack-exchange
  description: "Returns all of a user's associated accounts, given their account_ids
    in {ids}.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids
    programatically look for account_id on user objects.\n \nThis method returns a
    list of network_users."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/associated
  tags: Users,Associated
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsassociated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsassociated-get-openapi.md
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/badges
  tags: Users,Badges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsbadges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsbadges-get-openapi.md
- name: Stack Exchange Get User Comments
  x-api-slug: stack-exchange
  description: "Get the comments posted by users in {ids}.\n \n{ids} can contain up
    to 100 semicolon delimited ids, to find ids programatically look for user_id on
    user or shallow_user objects.\n \nThe sorts accepted by this method operate on
    the follow fields of the comment object:\n - creation - creation_date\n - votes
    - score\n  creation is the default sort.\n \n It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/comments
  tags: Users,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidscomments-get-openapi.md
- name: Stack Exchange Get User Comments Told
  x-api-slug: stack-exchange
  description: "Get the comments that the users in {ids} have posted in reply to the
    single user identified in {toid}.\n \nThis method is useful for extracting conversations,
    especially over time or across multiple posts.\n \n{ids} can contain up to 100
    semicolon delimited ids, to find ids programatically look for user_id on user
    or shallow_user objects. {toid} can contain only 1 id, found in the same manner
    as those in {ids}.\n \nThe sorts accepted by this method operate on the follow
    fields of the comment object:\n - creation - creation_date\n - votes - score\n
    \ creation is the default sort.\n \n It is possible to create moderately complex
    queries using sort, min, max, fromdate, and todate.\n \nThis method returns a
    list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/comments/{toid}
  tags: Users,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidscommentstoid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidscommentstoid-get-openapi.md
- name: Stack Exchange Get User Favorites
  x-api-slug: stack-exchange
  description: "Get the questions that users in {ids} have favorited.\n \nThis method
    is effectively a view onto a user's favorites tab.\n \n{ids} can contain up to
    100 semicolon delimited ids, to find ids programatically look for user_id on user
    or shallow_user objects.\n \nThe sorts accepted by this method operate on the
    follow fields of the question object:\n - activity - last_activity_date\n - creation
    - creation_date\n - votes - score\n - added - when the user favorited the question\n
    \ activity is the default sort.\n \n It is possible to create moderately complex
    queries using sort, min, max, fromdate, and todate.\n \nThis method returns a
    list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/favorites
  tags: Users,Favorites
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsfavorites-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsfavorites-get-openapi.md
- name: Stack Exchange Get User Mentioned
  x-api-slug: stack-exchange
  description: "Gets all the comments that the users in {ids} were mentioned in.\n
    \nNote, to count as a mention the comment must be considered to be \"in reply
    to\" a user. Most importantly, this means that a comment can only be in reply
    to a single user.\n \n{ids} can contain up to 100 semicolon delimited ids, to
    find ids programatically look for user_id on user or shallow_user objects.\n \nThe
    sorts accepted by this method operate on the follow fields of the comment object:\n
    - creation - creation_date\n - votes - score\n  It is possible to create moderately
    complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns
    a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/mentioned
  tags: Users,Mentioned
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsmentioned-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsmentioned-get-openapi.md
- name: Stack Exchange Get User Merges
  x-api-slug: stack-exchange
  description: "Returns a record of merges that have occurred involving the passed
    account ids.\n \nThis method allows you to take now invalid account ids and find
    what account they've become, or take currently valid account ids and find which
    ids were equivalent in the past.\n \nThis is most useful when confirming that
    an account_id is in fact \"new\" to an application.\n \nAccount merges can happen
    for a wide range of reasons, applications should not make assumptions that merges
    have particular causes.\n \nNote that accounts are managed at a network level,
    users on a site may be merged due to an account level merge but there is no guarantee
    that a merge has an effect on any particular site.\n \nThis method returns a list
    of account_merge."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/merges
  tags: Users,Merges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsmerges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsmerges-get-openapi.md
- name: Stack Exchange Get User Questions
  x-api-slug: stack-exchange
  description: "Gets the questions asked by the users in {ids}.\n \n{ids} can contain
    up to 100 semicolon delimited ids, to find ids programatically look for user_id
    on user or shallow_user objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/questions
  tags: Users,Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestions-get-openapi.md
- name: Stack Exchange Get User Questions Featured
  x-api-slug: stack-exchange
  description: "Gets the questions on which the users in {ids} have active bounties.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this
    method operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/questions/featured
  tags: Users,Featured
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsfeatured-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsfeatured-get-openapi.md
- name: Stack Exchange Get User Questions No Answers
  x-api-slug: stack-exchange
  description: "Gets the questions asked by the users in {ids} which have no answers.\n
    \nQuestions returns by this method actually have zero undeleted answers. It is
    completely disjoint /users/{ids}/questions/unanswered and /users/{ids}/questions/unaccepted,
    which only return questions with at least one answer, subject to other contraints.\n
    \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
    look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this
    method operate on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/questions/no-answers
  tags: Users,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsnoanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsnoanswers-get-openapi.md
- name: Stack Exchange Get User Questions Unnacepted
  x-api-slug: stack-exchange
  description: "Gets the questions asked by the users in {ids} which have at least
    one answer, but no accepted answer.\n \nQuestions returned by this method have
    answers, but the owner has not opted to accept any of them.\n \n{ids} can contain
    up to 100 semicolon delimited ids, to find ids programatically look for user_id
    on user or shallow_user objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/questions/unaccepted
  tags: Users,Unaccepted
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsunaccepted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsunaccepted-get-openapi.md
- name: Stack Exchange Get User Questions Unanswered
  x-api-slug: stack-exchange
  description: "Gets the questions asked by the users in {ids} which the site consideres
    unanswered, while still having at least one answer posted.\n \nThese rules are
    subject to change, but currently any question without at least one upvoted or
    accepted answer is considered unanswered.\n \nTo get the set of questions that
    a user probably considers unanswered, the returned questions should be unioned
    with those returned by /users/{id}/questions/no-answers. These methods are distinct
    so that truly unanswered (that is, zero posted answers) questions can be easily
    separated from mearly poorly or inadequately answered ones.\n \n{ids} can contain
    up to 100 semicolon delimited ids, to find ids programatically look for user_id
    on user or shallow_user objects.\n \nThe sorts accepted by this method operate
    on the follow fields of the question object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/questions/unanswered
  tags: Users,Unanswerd
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsunanswered-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsquestionsunanswered-get-openapi.md
- name: Stack Exchange Get User Reputation
  x-api-slug: stack-exchange
  description: "Gets a subset of the reputation changes for users in {ids}.\n \nReputation
    changes are intentionally scrubbed of some data to make it difficult to correlate
    votes on particular posts with user reputation changes. That being said, this
    method returns enough data for reasonable display of reputation trends.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for user_id on user or shallow_user objects.\n \nThis method returns a list of
    reputation objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/reputation
  tags: Users,Reputation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsreputation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsreputation-get-openapi.md
- name: Stack Exchange Get User Reputation History
  x-api-slug: stack-exchange
  description: "Returns users' public reputation history.\n \nThis method returns
    a list of reputation_history."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/reputation-history
  tags: Users,Reputation,History
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsreputationhistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidsreputationhistory-get-openapi.md
- name: Stack Exchange Get User Suggested Edits
  x-api-slug: stack-exchange
  description: "Returns the suggested edits a users in {ids} have submitted.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for user_id on user or shallow_user objects.\n \nThe sorts accepted by this method
    operate on the follow fields of the suggested_edit object:\n - creation - creation_date\n
    - approval - approval_date Does not return unapproved suggested_edits\n - rejection
    - rejection_date Does not return unrejected suggested_edits\n  creation is the
    default sort.\n \n It is possible to create moderately complex queries using sort,
    min, max, fromdate, and todate.\n \nThis method returns a list of suggested-edits."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/suggested-edits
  tags: Users,Suggested Edits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidssuggestededits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidssuggestededits-get-openapi.md
- name: Stack Exchange Get User Tags
  x-api-slug: stack-exchange
  description: "Returns the tags the users identified in {ids} have been active in.\n
    \nThis route corresponds roughly to user's stats tab, but does not include tag
    scores. A subset of tag scores are available (on a single user basis) in /users/{id}/top-answer-tags
    and /users/{id}/top-question-tags.\n \n{ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for user_id on user or shallow_user objects.\n
    \nThe sorts accepted by this method operate on the follow fields of the tag object:\n
    - popular - count\n - activity - the creation_date of the last question asked
    with the tag\n - name - name\n  popular is the default sort.\n \n It is possible
    to create moderately complex queries using sort, min, max, fromdate, and todate.\n
    \nThis method returns a list of tags."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/tags
  tags: Users,Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidstags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidstags-get-openapi.md
- name: Stack Exchange Get User Timeline
  x-api-slug: stack-exchange
  description: "Returns a subset of the actions the users in {ids} have taken on the
    site.\n \nThis method returns users' posts, edits, and earned badges in the order
    they were accomplished. It is possible to filter to just a window of activity
    using the fromdate and todate parameters.\n \n{ids} can contain up to 100 semicolon
    delimited ids, to find ids programatically look for user_id on user or shallow_user
    objects.\n \nThis method returns a list of user timeline objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{ids}/timeline
  tags: Users,Timiline
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidstimeline-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidstimeline-get-openapi.md
- name: Stack Exchange Get User Inbox
  x-api-slug: stack-exchange
  description: "Returns a user's inbox.\n \nThis method requires an access_token,
    with a scope containing \"read_inbox\".\n \nThis method is effectively an alias
    for /inbox. It is provided for consumers who make strong assumptions about operating
    within the context of a single site rather than the Stack Exchange network as
    a whole.\n \n{id} can contain a single id, to find it programatically look for
    user_id on user or shallow_user objects.\n \nThis method returns a list of inbox
    items."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/inbox
  tags: Users,Email,Inbox
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidinbox-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidinbox-get-openapi.md
- name: Stack Exchange Get User Inbox Unread
  x-api-slug: stack-exchange
  description: "Returns the unread items in a user's inbox.\n \nThis method requires
    an access_token, with a scope containing \"read_inbox\".\n \nThis method is effectively
    an alias for /inbox/unread. It is provided for consumers who make strong assumptions
    about operating within the context of a single site rather than the Stack Exchange
    network as a whole.\n \n{id} can contain a single id, to find it programatically
    look for user_id on user or shallow_user objects.\n \nThis method returns a list
    of inbox items."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/inbox/unread
  tags: Users,Email,Inbox
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidinboxunread-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidinboxunread-get-openapi.md
- name: Stack Exchange Get User Notifications
  x-api-slug: stack-exchange
  description: "Returns a user's notifications.\n \nThis method requires an access_token,
    with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/notifications
  tags: Users,Notifications
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidnotifications-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidnotifications-get-openapi.md
- name: Stack Exchange Get User Notifications Unread
  x-api-slug: stack-exchange
  description: "Returns a user's unread notifications.\n \nThis method requires an
    access_token, with a scope containing \"read_inbox\".\n \nThis method returns
    a list of notifications."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/notifications/unread
  tags: Users,Notifications
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidnotificationsunread-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidnotificationsunread-get-openapi.md
- name: Stack Exchange Get User Preveleges
  x-api-slug: stack-exchange
  description: "Returns the privileges a user has.\n \nApplications are encouraged
    to calculate privileges themselves, without repeated queries to this method. A
    simple check against the results returned by /privileges and user.user_type would
    be sufficient.\n \n{id} can contain only a single, to find it programatically
    look for user_id on user or shallow_user objects.\n \nThis method returns a list
    of privileges."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/privileges
  tags: Users,Privileges
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidprivileges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidprivileges-get-openapi.md
- name: Stack Exchange Get User Reputation History Full
  x-api-slug: stack-exchange
  description: "Returns a user's full reputation history, including private events.\n
    \nThis method requires an access_token, with a scope containing \"private_info\".\n
    \nThis method returns a list of reputation_history."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/reputation-history/full
  tags: Users,Reputation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidreputationhistoryfull-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidreputationhistoryfull-get-openapi.md
- name: Stack Exchange Get User Tags Top Answers
  x-api-slug: stack-exchange
  description: "Returns the top 30 answers a user has posted in response to questions
    with the given tags.\n \n{id} can contain a single id, to find it programatically
    look for user_id on user or shallow_user objects. {tags} is limited to 5 tags,
    passing more will result in an error.\n \nThe sorts accepted by this method operate
    on the follow fields of the answer object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of answers."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/tags/{tags}/top-answers
  tags: Users,Tags,Answers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtagstagstopanswers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtagstagstopanswers-get-openapi.md
- name: Stack Exchange Get User Tags Top Questions
  x-api-slug: stack-exchange
  description: "Returns the top 30 questions a user has asked with the given tags.\n
    \n{id} can contain a single id, to find it programatically look for user_id on
    user or shallow_user objects. {tags} is limited to 5 tags, passing more will result
    in an error.\n \nThe sorts accepted by this method operate on the follow fields
    of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
    - votes - score\n  activity is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of questions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/tags/{tags}/top-questions
  tags: Users,Tags,Questions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtagstagstopquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtagstagstopquestions-get-openapi.md
- name: Stack Exchange Get User Top Answers Tags
  x-api-slug: stack-exchange
  description: "Returns a single user's top tags by answer score.\n \nThis a subset
    of the data returned on a user's tags tab.\n \n{id} can contain a single id, to
    find it programatically look for user_id on user or shallow_user objects.\n \nThis
    method returns a list of top_tag objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/top-answer-tags
  tags: Users,Top Answer Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtopanswertags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtopanswertags-get-openapi.md
- name: Stack Exchange Get User Top Question Tags
  x-api-slug: stack-exchange
  description: "Returns a single user's top tags by question score.\n \nThis a subset
    of the data returned on a user's tags tab.\n \n{id} can contain a single id, to
    find it programatically look for user_id on user or shallow_user objects.\n \nThis
    method returns a list of top_tag objects."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/top-question-tags
  tags: Users,Top Question Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtopquestiontags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidtopquestiontags-get-openapi.md
- name: Stack Exchange Get User Write Permissions
  x-api-slug: stack-exchange
  description: "Returns the write permissions a user has via the api.\n \nThe Stack
    Exchange API gives users the ability to create, edit, and delete certain types.
    This method returns whether the passed user is capable of performing those actions
    at all, as well as how many times a day they can.\n \nThis method does not consider
    the user's current quota (ie. if they've already exhausted it for today) nor any
    additional restrictions on write access, such as editing deleted comments.\n \nThis
    method returns a list of write_permissions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2//users/{id}/write-permissions
  tags: Write Permissions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidwritepermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/usersidwritepermissions-get-openapi.md
- name: Stack Exchange
  x-api-slug: stack-exchange
  description: Stack Exchange is a network of question and answer websites on diverse
    topics in many different fields, each site covering a specific topic, where questions,
    answers, and users are subject to a reputation award process. The sites are modeled
    after Stack Overflow, a forum for computer programming questions that was the
    original site in this network. The reputation system is designed to allow the
    sites to be self-moderating.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/253_logo.png
  humanURL: https://stackexchange.com/
  baseURL: https://api.stackexchange.com//2.2
  tags: Stack Exchange
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/stack-exchange/master/_listings/stack-exchange/openapi.md
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
- type: x-developer
  url: http://api.stackexchange.com/
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
  url: https://stackexchange.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---