---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 0
info:
  title: Stack Exchange Invalidate Acces Tokens
  description: "Immediately expires the access tokens passed. This method is meant
    to allow an application to discard any active access tokens it no longer needs.\n
    \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating
    a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
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