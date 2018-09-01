---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Get Questions Unanswered
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
  /me/mentioned:
    get:
      summary: My Mentions
      description: "Returns the comments mentioning the user associated with the given
        access_token.\n \nThis method returns a list of comments."
      operationId: returns-the-comments-mentioning-the-user-associated-with-the-given-access-token-this-method-returns-
      x-api-path-slug: mementioned-get
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
      - Mentioned
  /me/merges:
    get:
      summary: My Merges
      description: "Returns a record of merges that have occurred involving a user
        identified by an access_token.\n \nThis method allows you to take now invalid
        account ids and find what account they've become, or take currently valid
        account ids and find which ids were equivalent in the past.\n \nThis is most
        useful when confirming that an account_id is in fact \"new\" to an application.\n
        \nAccount merges can happen for a wide range of reasons, applications should
        not make assumptions that merges have particular causes.\n \nNote that accounts
        are managed at a network level, users on a site may be merged due to an account
        level merge but there is no guarantee that a merge has an effect on any particular
        site.\n \nThis method returns a list of account_merge."
      operationId: returns-a-record-of-merges-that-have-occurred-involving-a-user-identified-by-an-access-token-this-me
      x-api-path-slug: memerges-get
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
      - Merges
  /me/notifications:
    get:
      summary: My Notiications
      description: "Returns a user's notifications, given an access_token.\n \nThis
        method requires an access_token, with a scope containing \"read_inbox\".\n
        \nThis method returns a list of notifications."
      operationId: returns-a-users-notifications-given-an-access-token-this-method-requires-an-access-token-with-a-scop
      x-api-path-slug: menotifications-get
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
      - Notifications
  /me/notifications/unread:
    get:
      summary: My Notiications Unread
      description: "Returns a user's unread notifications, given an access_token.\n
        \nThis method requires an access_token, with a scope containing \"read_inbox\".\n
        \nThis method returns a list of notifications."
      operationId: returns-a-users-unread-notifications-given-an-access-token-this-method-requires-an-access-token-with
      x-api-path-slug: menotificationsunread-get
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
      - Notifications
  /me/privileges:
    get:
      summary: My Priveleges
      description: "Returns the privileges the user identified by access_token has.\n
        \nThis method returns a list of privileges."
      operationId: returns-the-privileges-the-user-identified-by-access-token-has-this-method-returns-a-list-of-privile
      x-api-path-slug: meprivileges-get
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
      - Privileges
  /me/questions:
    get:
      summary: My Questions
      description: "Returns the questions owned by the user associated with the given
        access_token.\n \nThis method returns a list of questions."
      operationId: returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a
      x-api-path-slug: mequestions-get
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
      - Questions
  /me/questions/featured:
    get:
      summary: My Questions Featured
      description: "Returns the questions that have active bounties offered by the
        user associated with the given access_token.\n \nThis method returns a list
        of questions."
      operationId: returns-the-questions-that-have-active-bounties-offered-by-the-user-associated-with-the-given-access
      x-api-path-slug: mequestionsfeatured-get
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
      - Questions
  /me/questions/no-answers:
    get:
      summary: My Questions No Answers
      description: "Returns the questions owned by the user associated with the given
        access_token that have no answers.\n \nThis method returns a list of questions."
      operationId: returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-that-have-no-answers-
      x-api-path-slug: mequestionsnoanswers-get
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
      - Questions
  /me/questions/unaccepted:
    get:
      summary: My Questions Unaccepted
      description: "Returns the questions owned by the user associated with the given
        access_token that have no accepted answer.\n \nThis method returns a list
        of questions."
      operationId: returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-that-have-no-accepted
      x-api-path-slug: mequestionsunaccepted-get
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
      - Questions
  /me/questions/unanswered:
    get:
      summary: My Questions Unanswered
      description: "Returns the questions owned by the user associated with the given
        access_token that are not considered answered.\n \nThis method returns a list
        of questions."
      operationId: returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-that-are-not-consider
      x-api-path-slug: mequestionsunanswered-get
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
      - Questions
  /me/reputation:
    get:
      summary: My Reputation
      description: "Returns the reputation changed for the user associated with the
        given access_token.\n \nThis method returns a list of reputation changes."
      operationId: returns-the-reputation-changed-for-the-user-associated-with-the-given-access-token-this-method-retur
      x-api-path-slug: mereputation-get
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
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Reputation
  /me/reputation-history:
    get:
      summary: My Reputation History
      description: "Returns user's public reputation history.\n \nThis method returns
        a list of reputation_history."
      operationId: returns-users-public-reputation-history-this-method-returns-a-list-of-reputation-history
      x-api-path-slug: mereputationhistory-get
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
      - Reputation
  /me/reputation-history/full:
    get:
      summary: My Reputation History Full
      description: "Returns user's full reputation history, including private events.\n
        \n This method requires an access_token, with a scope containing \"private_info\".\n
        \nThis method returns a list of reputation_history."
      operationId: returns-users-full-reputation-history-including-private-events--this-method-requires-an-access-token
      x-api-path-slug: mereputationhistoryfull-get
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
      - Reputation
  /me/suggested-edits:
    get:
      summary: Suggested Edits
      description: "Returns the suggested edits the user identified by access_token
        has submitted.\n \nThis method returns a list of suggested-edits."
      operationId: returns-the-suggested-edits-the-user-identified-by-access-token-has-submitted-this-method-returns-a-
      x-api-path-slug: mesuggestededits-get
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
        description: sort = creation => datesort = approval => datesort = rejection
          => date
      - in: query
        name: min
        description: sort = creation => datesort = approval => datesort = rejection
          => date
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
      - Suggested Edits
  /me/tags:
    get:
      summary: My Tags
      description: "Returns the tags the user identified by the access_token passed
        is active in.\n \nThis method returns a list of tags."
      operationId: returns-the-tags-the-user-identified-by-the-access-token-passed-is-active-in-this-method-returns-a-l
      x-api-path-slug: metags-get
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
        description: sort = popular => numbersort = activity => datesort = name =>
          string
      - in: query
        name: min
        description: sort = popular => numbersort = activity => datesort = name =>
          string
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
      - Tags
  /me/tags/{tags}/top-answers:
    get:
      summary: My Tags Top Answers
      description: "Returns the top 30 answers the user associated with the given
        access_token has posted in response to questions with the given tags.\n \nThis
        method returns a list of answers."
      operationId: returns-the-top-30-answers-the-user-associated-with-the-given-access-token-has-posted-in-response-to
      x-api-path-slug: metagstagstopanswers-get
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
      - in: path
        name: tags
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Anwers
  /me/tags/{tags}/top-questions:
    get:
      summary: My Tags Top Questions
      description: "Returns the top 30 questions the user associated with the given
        access_token has posted in response to questions with the given tags.\n \nThis
        method returns a list of questions."
      operationId: returns-the-top-30-questions-the-user-associated-with-the-given-access-token-has-posted-in-response-
      x-api-path-slug: metagstagstopquestions-get
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
          numbersort = hot => nonesort = week => nonesort = month => nonesort = relevance
          => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = hot => nonesort = week => nonesort = month => nonesort = relevance
          => none
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
      - in: path
        name: tags
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Questions
  /me/timeline:
    get:
      summary: My Timeline
      description: "Returns a subset of the actions the user identified by the passed
        access_token has taken on the site.\n \nThis method returns a list of user
        timeline objects."
      operationId: returns-a-subset-of-the-actions-the-user-identified-by-the-passed-access-token-has-taken-on-the-site
      x-api-path-slug: metimeline-get
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
      - Tags
      - Timeline
  /me/top-answer-tags:
    get:
      summary: My Top Answer Tags
      description: "Returns the user identified by access_token's top 30 tags by answer
        score.\n \nThis method returns a list of top tag objects."
      operationId: returns-the-user-identified-by-access-tokens-top-30-tags-by-answer-score-this-method-returns-a-list-
      x-api-path-slug: metopanswertags-get
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
      - Tags
      - Anwers
  /me/top-question-tags:
    get:
      summary: My Top Question Tags
      description: "Returns the user identified by access_token's top 30 tags by question
        score.\n \nThis method returns a list of top tag objects."
      operationId: returns-the-user-identified-by-access-tokens-top-30-tags-by-question-score-this-method-returns-a-lis
      x-api-path-slug: metopquestiontags-get
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
      - Tags
      - Questions
  /me/write-permissions:
    get:
      summary: My Write Permissions
      description: "Returns the write permissions a user has via the api, given an
        access token.\n \nThe Stack Exchange API gives users the ability to create,
        edit, and delete certain types. This method returns whether the passed user
        is capable of performing those actions at all, as well as how many times a
        day they can.\n \nThis method does not consider the user's current quota (ie.
        if they've already exhausted it for today) nor any additional restrictions
        on write access, such as editing deleted comments.\n \nThis method returns
        a list of write_permissions."
      operationId: returns-the-write-permissions-a-user-has-via-the-api-given-an-access-token-the-stack-exchange-api-gi
      x-api-path-slug: mewritepermissions-get
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
      - Write Permissions
  /notifications:
    get:
      summary: Get Notifications
      description: "Returns a user's notifications.\n \nThis method requires an access_token,
        with a scope containing \"read_inbox\".\n \nThis method returns a list of
        notifications."
      operationId: returns-a-users-notifications-this-method-requires-an-access-token-with-a-scope-containing-read-inbo
      x-api-path-slug: notifications-get
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
      - Notifications
  /notifications/unread:
    get:
      summary: Get Notifications Unread
      description: "Returns a user's unread notifications.\n \nThis method requires
        an access_token, with a scope containing \"read_inbox\".\n \nThis method returns
        a list of notifications."
      operationId: returns-a-users-unread-notifications-this-method-requires-an-access-token-with-a-scope-containing-re
      x-api-path-slug: notificationsunread-get
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
      - Notifications
  /posts:
    get:
      summary: Get Posts
      description: "Fetches all posts (questions and answers) on the site.\n \nIn
        many ways this method is the union of /questions and /answers, returning both
        sets of data albeit only the common fields.\n \nMost applications should use
        the question or answer specific methods, but /posts is available for those
        rare cases where any activity is of intereset. Examples of such queries would
        be: \"all posts on Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n
        \nThe sorts accepted by this method operate on the follow fields of the post
        object:\n - activity - last_activity_date\n - creation - creation_date\n -
        votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of posts."
      operationId: fetches-all-posts-questions-and-answers-on-the-site-in-many-ways-this-method-is-the-union-of-questio
      x-api-path-slug: posts-get
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
      - Posts
  /posts/{ids}:
    get:
      summary: Get Post
      description: "Fetches a set of posts by ids.\n \nThis method is meant for grabbing
        an object when unsure whether an id identifies a question or an answer. This
        is most common with user entered data.\n \n{ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for post_id, answer_id, or
        question_id on post, answer, and question objects respectively.\n \nThe sorts
        accepted by this method operate on the follow fields of the post object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of posts."
      operationId: fetches-a-set-of-posts-by-ids-this-method-is-meant-for-grabbing-an-object-when-unsure-whether-an-id-
      x-api-path-slug: postsids-get
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
      - Posts
  /posts/{ids}/comments:
    get:
      summary: Get Post Comments
      description: "Gets the comments on the posts identified in ids, regardless of
        the type of the posts.\n \nThis method is meant for cases when you are unsure
        of the type of the post id provided. Generally, this would be due to obtaining
        the post id directly from a user.\n \n{ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for post_id, answer_id, or
        question_id on post, answer, and question objects respectively.\n \nThe sorts
        accepted by this method operate on the follow fields of the comment object:\n
        - creation - creation_date\n - votes - score\n  creation is the default sort.\n
        \n It is possible to create moderately complex queries using sort, min, max,
        fromdate, and todate.\n \nThis method returns a list of comments."
      operationId: gets-the-comments-on-the-posts-identified-in-ids-regardless-of-the-type-of-the-posts-this-method-is-
      x-api-path-slug: postsidscomments-get
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
      - Posts
      - Comments
  /posts/{ids}/revisions:
    get:
      summary: Get Post Revisions
      description: "Returns edit revisions for the posts identified in ids.\n \n{ids}
        can contain up to 100 semicolon delimited ids, to find ids programatically
        look for post_id, answer_id, or question_id on post, answer, and question
        objects respectively.\n \nThis method returns a list of revisions."
      operationId: returns-edit-revisions-for-the-posts-identified-in-ids-ids-can-contain-up-to-100-semicolon-delimited
      x-api-path-slug: postsidsrevisions-get
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
      - Posts
      - Revisions
  /posts/{ids}/suggested-edits:
    get:
      summary: Get Posts Suggested Edits
      description: "Returns suggsted edits on the posts identified in ids.\n \n -
        creation - creation_date\n - approval - approval_date\n - rejection - rejection_date\n
        \ creation is the default sort.\n \n {ids} can contain up to 100 semicolon
        delimited ids, to find ids programatically look for post_id, answer_id, or
        question_id on post, answer, and question objects respectively.\n \nThis method
        returns a list of suggested-edits."
      operationId: returns-suggsted-edits-on-the-posts-identified-in-ids---creation--creation-date--approval--approval-
      x-api-path-slug: postsidssuggestededits-get
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
        description: sort = creation => datesort = approval => datesort = rejection
          => date
      - in: query
        name: min
        description: sort = creation => datesort = approval => datesort = rejection
          => date
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
      - Posts
      - Suggested Edits
  /posts/{id}/comments/add:
    post:
      summary: Add Comment Post
      description: "Create a new comment.\n \nUse an access_token with write_access
        to create a new comment on a post.\n \nThis method returns the created comment."
      operationId: create-a-new-comment-use-an-access-token-with-write-access-to-create-a-new-comment-on-a-post-this-me
      x-api-path-slug: postsidcommentsadd-post
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
      - Posts
      - Comments
  /privileges:
    get:
      summary: Get Privileges
      description: "Returns the earnable privileges on a site.\n \nPrivileges define
        abilities a user can earn (via reputation) on any Stack Exchange site.\n \nWhile
        fairly stable, over time they do change. New ones are introduced with new
        features, and the reputation requirements change as a site matures.\n \nThis
        method returns a list of privileges."
      operationId: returns-the-earnable-privileges-on-a-site-privileges-define-abilities-a-user-can-earn-via-reputation
      x-api-path-slug: privileges-get
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
      - Privileges
  /questions:
    get:
      summary: Get Questions
      description: "Gets all the questions on the site.\n \nThis method allows you
        make fairly flexible queries across the entire corpus of questions on a site.
        For example, getting all questions asked in the the week of Jan 1st 2011 with
        scores of 10 or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n
        \nTo constrain questions returned to those with a set of tags, use the tagged
        parameter with a semi-colon delimited list of tags. This is an and contraint,
        passing tagged=c;java will return only those questions with both tags. As
        such, passing more than 5 tags will always return zero results.\n \nThe sorts
        accepted by this method operate on the follow fields of the question object:\n
        - activity - last_activity_date\n - creation - creation_date\n - votes - score\n
        - hot - by the formula ordering the hot tab Does not accept min or max\n -
        week - by the formula ordering the week tab Does not accept min or max\n -
        month - by the formula ordering the month tab Does not accept min or max\n
        \ activity is the default sort.\n \n It is possible to create moderately complex
        queries using sort, min, max, fromdate, and todate.\n \nThis method returns
        a list of questions."
      operationId: gets-all-the-questions-on-the-site-this-method-allows-you-make-fairly-flexible-queries-across-the-en
      x-api-path-slug: questions-get
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
          numbersort = hot => nonesort = week => nonesort = month => nonesort = relevance
          => none
      - in: query
        name: min
        description: sort = activity => datesort = creation => datesort = votes =>
          numbersort = hot => nonesort = week => nonesort = month => nonesort = relevance
          => none
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
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
  /questions/featured:
    get:
      summary: Get Questions Featured
      description: "Returns all the questions with active bounties in the system.\n
        \nThe sorts accepted by this method operate on the follow fields of the question
        object:\n - activity - last_activity_date\n - creation - creation_date\n -
        votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of questions."
      operationId: returns-all-the-questions-with-active-bounties-in-the-system-the-sorts-accepted-by-this-method-opera
      x-api-path-slug: questionsfeatured-get
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
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
  /questions/no-answers:
    get:
      summary: Get Questions No Answers
      description: "Returns questions which have received no answers.\n \nCompare
        with /questions/unanswered which mearly returns questions that the sites consider
        insufficiently well answered.\n \nThis method corresponds roughly with the
        this site tab.\n \nTo constrain questions returned to those with a set of
        tags, use the tagged parameter with a semi-colon delimited list of tags. This
        is an and contraint, passing tagged=c;java will return only those questions
        with both tags. As such, passing more than 5 tags will always return zero
        results.\n \nThe sorts accepted by this method operate on the follow fields
        of the question object:\n - activity - last_activity_date\n - creation - creation_date\n
        - votes - score\n  activity is the default sort.\n \n It is possible to create
        moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
        method returns a list of questions."
      operationId: returns-questions-which-have-received-no-answers-compare-with-questionsunanswered-which-mearly-retur
      x-api-path-slug: questionsnoanswers-get
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
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
  /questions/unanswered:
    get:
      summary: Get Questions Unanswered
      description: "Returns questions the site considers to be unanswered.\n \nNote
        that just because a question has an answer, that does not mean it is considered
        answered. While the rules are subject to change, at this time a question must
        have at least one upvoted answer to be considered answered.\n \nTo constrain
        questions returned to those with a set of tags, use the tagged parameter with
        a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java
        will return only those questions with both tags. As such, passing more than
        5 tags will always return zero results.\n \nCompare with /questions/no-answers.\n
        \nThis method corresponds roughly with the unanswered tab.\n \nThe sorts accepted
        by this method operate on the follow fields of the question object:\n - activity
        - last_activity_date\n - creation - creation_date\n - votes - score\n  activity
        is the default sort.\n \n It is possible to create moderately complex queries
        using sort, min, max, fromdate, and todate.\n \nThis method returns a list
        of questions."
      operationId: returns-questions-the-site-considers-to-be-unanswered-note-that-just-because-a-question-has-an-answe
      x-api-path-slug: questionsunanswered-get
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
        name: tagged
        description: String list (semicolon delimited)
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - Questions
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