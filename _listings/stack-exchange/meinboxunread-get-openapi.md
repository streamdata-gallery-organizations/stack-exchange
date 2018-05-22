---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange My Inbox Unread
  description: "Returns the unread items in the user identified by access_token's
    inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n
    \nThis method returns a list of inbox items."
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
  /access-tokens/{accessTokens}:
    get:
      summary: Get Acces Tokens
      description: "Reads the properties for a set of access tokens.\n \n{accessTokens}
        can contain up to 20 access tokens. These are obtained by authenticating a
        user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
      operationId: reads-the-properties-for-a-set-of-access-tokens-accesstokens-can-contain-up-to-20-access-tokens-thes
      x-api-path-slug: accesstokensaccesstokens-get
      parameters:
      - in: path
        name: accessTokens
        description: String list (semicolon delimited)
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      responses:
        200:
          description: OK
      tags:
      - Authentication
      - Access Tokens
  /access-tokens/{accessTokens}/invalidate:
    get:
      summary: Invalidate Acces Tokens
      description: "Immediately expires the access tokens passed. This method is meant
        to allow an application to discard any active access tokens it no longer needs.\n
        \n{accessTokens} can contain up to 20 access tokens. These are obtained by
        authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
      operationId: immediately-expires-the-access-tokens-passed-this-method-is-meant-to-allow-an-application-to-discard
      x-api-path-slug: accesstokensaccesstokensinvalidate-get
      parameters:
      - in: path
        name: accessTokens
        description: String list (semicolon delimited)
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      responses:
        200:
          description: OK
      tags:
      - Authentication
      - Access Tokens
  /answers:
    get:
      summary: Get Answers
      description: "Returns all the undeleted answers in the system.\n \nThe sorts
        accepted by this method operate on the follow fields of the answer object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of answers."
      operationId: returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol
      x-api-path-slug: answers-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: Filter the discussion
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: max
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
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
      - Answers
  /answers/{ids}:
    get:
      summary: Get Answer
      description: "Gets the set of answers identified by ids.\n \nThis is meant for
        batch fetcing of questions. A useful trick to poll for updates is to sort
        by activity, with a minimum date of the last time you polled.\n \n{ids} can
        contain up to 100 semicolon delimited ids, to find ids programatically look
        for answer_id on answer objects.\n \nThe sorts accepted by this method operate
        on the follow fields of the answer object:\n - activity - last_activity_date\n
        - creation - creation_date\n - votes - score\n  activity is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of answers."
      operationId: gets-the-set-of-answers-identified-by-ids-this-is-meant-for-batch-fetcing-of-questions-a-useful-tric
      x-api-path-slug: answersids-get
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
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
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
      - Answers
  /answers/{ids}/comments:
    get:
      summary: Get Answer Comments
      description: "Gets the comments on a set of answers.\n \nIf you know that you
        have an answer id and need the comments, use this method. If you know you
        have a question id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n
        \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically
        look for answer_id on answer objects.\n \nThe sorts accepted by this method
        operate on the follow fields of the comment object:\n - creation - creation_date\n
        - votes - score\n  creation is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of comments."
      operationId: gets-the-comments-on-a-set-of-answers-if-you-know-that-you-have-an-answer-id-and-need-the-comments-u
      x-api-path-slug: answersidscomments-get
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
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
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
      - Answers
      - comments
  /apps/{accessTokens}/de-authenticate:
    get:
      summary: De-Authenticate Token
      description: "Passing valid access_tokens to this method causes the application
        that created them to be de-authorized by the user associated with each access_token.
        This will remove the application from their apps tab, and cause all other
        existing access_tokens to be destroyed.\n \nThis method is meant for uninstalling
        applications, recovering from access_token leaks, or simply as a stronger
        form of /access-tokens/{accessTokens}/invalidate.\n \nNothing prevents a user
        from re-authenticate to an application that has de-authenticated itself, the
        user will be prompted to approve the application again however.\n \n{accessTokens}
        can contain up to 20 access tokens. These are obtained by authenticating a
        user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
      operationId: passing-valid-access-tokens-to-this-method-causes-the-application-that-created-them-to-be-deauthoriz
      x-api-path-slug: appsaccesstokensdeauthenticate-get
      parameters:
      - in: path
        name: accessTokens
        description: String list (semicolon delimited)
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      responses:
        200:
          description: OK
      tags:
      - Authentication
      - Access Tokens
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
  /comments:
    get:
      summary: Get Comments
      description: "Gets all the comments on the site.\n \nIf you're filtering for
        interesting comments (by score, creation date, etc.) make use of the sort
        paramter with appropriate min and max values.\n \nIf you're looking to query
        conversations between users, instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid}
        methods.\n \nThe sorts accepted by this method operate on the follow fields
        of the comment object:\n - creation - creation_date\n - votes - score\n  creation
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of comments."
      operationId: gets-all-the-comments-on-the-site-if-youre-filtering-for-interesting-comments-by-score-creation-date
      x-api-path-slug: comments-get
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
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
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
      - Comments
  /comments/{ids}:
    get:
      summary: Get Comment
      description: "Gets the comments identified in id.\n \nThis method is most useful
        if you have a cache of comment ids obtained through other means (such as /questions/{id}/comments)
        but suspect the data may be stale.\n \n{ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for comment_id on comment
        objects.\n \nThe sorts accepted by this method operate on the follow fields
        of the comment object:\n - creation - creation_date\n - votes - score\n  creation
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of comments."
      operationId: gets-the-comments-identified-in-id-this-method-is-most-useful-if-you-have-a-cache-of-comment-ids-obt
      x-api-path-slug: commentsids-get
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
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
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
      - Comments
  /comments/{id}/delete:
    post:
      summary: Delete Comment
      description: "Deletes a comment.\n \nUse an access_token with write_access to
        delete a comment.\n \nIn practice, this method will never return an object."
      operationId: deletes-a-comment-use-an-access-token-with-write-access-to-delete-a-comment-in-practice-this-method-
      x-api-path-slug: commentsiddelete-post
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: path
        name: id
      - in: query
        name: preview
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Comments
  /comments/{id}/edit:
    post:
      summary: Edit Comment
      description: "Edit an existing comment.\n \nUse an access_token with write_access
        to edit an existing comment.\n \nThis method return the created comment."
      operationId: edit-an-existing-comment-use-an-access-token-with-write-access-to-edit-an-existing-comment-this-meth
      x-api-path-slug: commentsidedit-post
      parameters:
      - in: query
        name: body
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: path
        name: id
      - in: query
        name: preview
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Comments
  /errors:
    get:
      summary: Get Errors
      description: "Returns the various error codes that can be produced by the API.\n
        \nThis method is provided for discovery, documentation, and testing purposes,
        it is not expected many applications will consume it during normal operation.\n
        \nFor testing purposes, look into the /errors/{id} method which simulates
        errors given a code.\n \nThis method returns a list of errors."
      operationId: returns-the-various-error-codes-that-can-be-produced-by-the-api-this-method-is-provided-for-discover
      x-api-path-slug: errors-get
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
        name: page
      - in: query
        name: pagesize
      responses:
        200:
          description: OK
      tags:
      - Errors
  /errors/{id}:
    get:
      summary: Get Error
      description: "This method allows you to generate an error.\n \nThis method is
        only intended for use when testing an application or library. Unlike other
        methods in the API, its contract is not frozen, and new error codes may be
        added at any time.\n \nThis method results in an error, which will be expressed
        with a 400 HTTP status code and setting the error* properties on the wrapper
        object."
      operationId: this-method-allows-you-to-generate-an-error-this-method-is-only-intended-for-use-when-testing-an-app
      x-api-path-slug: errorsid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Errors
  /events:
    get:
      summary: Get Event
      description: "Returns a stream of events that have occurred on the site.\n \nThe
        API considers the following \"events\":\n - posting a question\n - posting
        an answer\n - posting a comment\n - editing a post\n - creating a user\n  \n
        \nEvents are only accessible for 15 minutes after they occurred, and by default
        only events in the last 5 minutes are returned. You can specify the age of
        the oldest event returned by setting the since parameter.\n \nIt is advised
        that developers batch events by ids and make as few subsequent requests to
        other methods as possible.\n \nThis method returns a list of events."
      operationId: returns-a-stream-of-events-that-have-occurred-on-the-site-the-api-considers-the-following-events--po
      x-api-path-slug: events-get
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
        name: page
      - in: query
        name: pagesize
      - in: query
        name: since
        description: Unix date
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Events
  /filters/create:
    get:
      summary: Create Filter
      description: "Creates a new filter given a list of includes, excludes, a base
        filter, and whether or not this filter should be \"unsafe\".\n \nFilter \"safety\"
        is defined as follows. Any string returned as a result of an API call with
        a safe filter will be inline-able into HTML without script-injection concerns.
        That is to say, no additional sanitizing (encoding, HTML tag stripping, etc.)
        will be necessary on returned strings. Applications that wish to handle sanitizing
        themselves should create an unsafe filter. All filters are safe by default,
        under the assumption that double-encoding bugs are more desirable than script
        injections.\n \nIf no base filter is specified, the default filter is assumed.
        When building a filter from scratch, the none built-in filter is useful.\n
        \nWhen the size of the parameters being sent to this method grows to large,
        problems can occur. This method will accept POST requests to mitigate this.\n
        \nIt is not expected that many applications will call this method at runtime,
        filters should be pre-calculated and \"baked in\" in the common cases. Furthermore,
        there are a number of built-in filters which cover common use cases.\n \nThis
        method returns a single filter."
      operationId: creates-a-new-filter-given-a-list-of-includes-excludes-a-base-filter-and-whether-or-not-this-filter-
      x-api-path-slug: filterscreate-get
      parameters:
      - in: query
        name: base
      - in: query
        name: exclude
        description: String list (semicolon delimited)
      - in: query
        name: include
        description: String list (semicolon delimited)
      - in: query
        name: unsafe
      responses:
        200:
          description: OK
      tags:
      - Files
  /filters/{filters}:
    get:
      summary: Get Filters
      description: "Returns the fields included by the given filters, and the \"safeness\"
        of those filters.\n \nIt is not expected that this method will be consumed
        by many applications at runtime, it is provided to aid in debugging.\n \n{filters}
        can contain up to 20 semicolon delimited filters. Filters are obtained via
        calls to /filters/create, or by using a built-in filter.\n \nThis method returns
        a list of filters."
      operationId: returns-the-fields-included-by-the-given-filters-and-the-safeness-of-those-filters-it-is-not-expecte
      x-api-path-slug: filtersfilters-get
      parameters:
      - in: path
        name: filters
        description: String list (semicolon delimited)
      responses:
        200:
          description: OK
      tags:
      - Files
  /inbox:
    get:
      summary: Get Inbox
      description: "Returns a user's inbox.\n \nThis method requires an access_token,
        with a scope containing \"read_inbox\".\n \nThis method returns a list of
        inbox items."
      operationId: returns-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containing-read-inbox-this-m
      x-api-path-slug: inbox-get
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
        name: page
      - in: query
        name: pagesize
      responses:
        200:
          description: OK
      tags:
      - Email
      - Inbox
  /inbox/unread:
    get:
      summary: Unread Inbox
      description: "Returns the unread items in a user's inbox.\n \nThis method requires
        an access_token, with a scope containing \"read_inbox\".\n \nThis method returns
        a list of inbox items."
      operationId: returns-the-unread-items-in-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containi
      x-api-path-slug: inboxunread-get
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
        name: page
      - in: query
        name: pagesize
      - in: query
        name: since
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Email
      - Inbox
  /info:
    get:
      summary: Get Information
      description: "Returns a collection of statistics about the site.\n \nData to
        facilitate per-site customization, discover related sites, and aggregate statistics
        is all returned by this method.\n \nThis data is cached very aggressively,
        by design. Query sparingly, ideally no more than once an hour.\n \nThis method
        returns an info object."
      operationId: returns-a-collection-of-statistics-about-the-site-data-to-facilitate-persite-customization-discover-
      x-api-path-slug: info-get
      parameters:
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Information
  /me:
    get:
      summary: Get Me
      description: "Returns the user associated with the passed access_token.\n \nThis
        method returns a user."
      operationId: returns-the-user-associated-with-the-passed-access-token-this-method-returns-a-user
      x-api-path-slug: me-get
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
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
      - in: query
        name: min
        description: sort = reputation => numbersort = creation => datesort = name
          => stringsort = modified => date
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
      - Self
  /me/answers:
    get:
      summary: My Answers
      description: "Returns the answers owned by the user associated with the given
        access_token.\n \nThis method returns a list of answers."
      operationId: returns-the-answers-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l
      x-api-path-slug: meanswers-get
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
        description: sort = activity => datesort = creation => datesort = votes =>
          number
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          number
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
      - Answers
  /me/associated:
    get:
      summary: My Assocated
      description: "Returns all of a user's associated accounts, given an access_token
        for them.\n \nThis method returns a list of network users."
      operationId: returns-all-of-a-users-associated-accounts-given-an-access-token-for-them-this-method-returns-a-list
      x-api-path-slug: meassociated-get
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
        name: page
      - in: query
        name: pagesize
      responses:
        200:
          description: OK
      tags:
      - Associated
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
  /me/comments:
    get:
      summary: My Comments
      description: "Returns the comments owned by the user associated with the given
        access_token.\n \nThis method returns a list of comments."
      operationId: returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-
      x-api-path-slug: mecomments-get
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
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
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
      - Comments
  /me/comments/{toId}:
    get:
      summary: My Comments
      description: "Returns the comments owned by the user associated with the given
        access_token that are in reply to the user identified by {toId}.\n \nThis
        method returns a list of comments."
      operationId: returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-that-are-in-reply-to-t
      x-api-path-slug: mecommentstoid-get
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
        description: sort = creation => datesort = votes => number
      - in: query
        name: min
        description: sort = creation => datesort = votes => number
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
      - in: path
        name: toId
      responses:
        200:
          description: OK
      tags:
      - Comments
  /me/favorites:
    get:
      summary: My Favorites
      description: "Returns the questions favorites by the user associated with the
        given access_token.\n \nThis method returns a list of questions."
      operationId: returns-the-questions-favorites-by-the-user-associated-with-the-given-access-token-this-method-retur
      x-api-path-slug: mefavorites-get
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
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = added => date
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = added => date
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
      - Favorites
  /me/inbox:
    get:
      summary: My Inbox
      description: "Returns the user identified by access_token's inbox.\n \nThis
        method requires an access_token, with a scope containing \"read_inbox\".\n
        \nThis method returns a list of inbox items."
      operationId: returns-the-user-identified-by-access-tokens-inbox-this-method-requires-an-access-token-with-a-scope
      x-api-path-slug: meinbox-get
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
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Email
      - Inbox
  /me/inbox/unread:
    get:
      summary: My Inbox Unread
      description: "Returns the unread items in the user identified by access_token's
        inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n
        \nThis method returns a list of inbox items."
      operationId: returns-the-unread-items-in-the-user-identified-by-access-tokens-inbox-this-method-requires-an-acces
      x-api-path-slug: meinboxunread-get
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
        name: page
      - in: query
        name: pagesize
      - in: query
        name: since
        description: Unix date
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Email
      - Inbox
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