{
  "info": {
    "name": "Stack Exchange Get User Reputation",
    "_postman_id": "47e177ef-76c3-49fa-ad57-64add60ff674",
    "description": "Gets a subset of the reputation changes for users in {ids}.\n \nReputation changes are intentionally scrubbed of some data to make it difficult to correlate votes on particular posts with user reputation changes. That being said, this method returns enough data for reasonable display of reputation trends.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of reputation objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "960bbcaa-440d-4639-b6a4-24d6bbb6d5b6",
          "name": "gets-a-subset-of-the-reputation-changes-for-users-in-ids-reputation-changes-are-intentionally-scrubb",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/reputation"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "site",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a subset of the reputation changes for users in {ids}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "86c39a8e-1f99-4f3a-8c07-69c360bee14a"
            }
          ]
        }
      ]
    }
  ]
}