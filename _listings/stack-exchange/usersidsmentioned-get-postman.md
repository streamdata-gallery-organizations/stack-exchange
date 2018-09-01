{
  "info": {
    "name": "Stack Exchange Get User Mentioned",
    "_postman_id": "0860a47e-0eda-4b75-8572-9bbaa5c3ce60",
    "description": "Gets all the comments that the users in {ids} were mentioned in.\n \nNote, to count as a mention the comment must be considered to be \"in reply to\" a user. Most importantly, this means that a comment can only be in reply to a single user.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "311b9466-ba1f-4e85-9519-d0ddfac27fd8",
          "name": "gets-all-the-comments-that-the-users-in-ids-were-mentioned-in-note-to-count-as-a-mention-the-comment",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/mentioned"
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
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
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
                  "key": "sort",
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
            "description": "Gets all the comments that the users in {ids} were mentioned in"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b47b31d6-621b-45e8-8e9c-ffdb2502fe84"
            }
          ]
        }
      ]
    }
  ]
}