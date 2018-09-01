{
  "info": {
    "name": "Stack Exchange My Comments",
    "_postman_id": "6bac0c8b-2590-4e84-a68a-c575f1ed4da4",
    "description": "Returns the comments owned by the user associated with the given access_token that are in reply to the user identified by {toId}.\n \nThis method returns a list of comments.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "comments",
      "item": [
        {
          "id": "89587f05-8b6c-4849-872b-b7be48f6d6ca",
          "name": "returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-that-are-in-reply-to-t",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "me/comments/:toId"
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
                  "id": "toId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments owned by the user associated with the given access_token that are in reply to the user identified by {toId}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b564475-1e7c-4c6f-8ada-71650165a8aa"
            }
          ]
        }
      ]
    }
  ]
}