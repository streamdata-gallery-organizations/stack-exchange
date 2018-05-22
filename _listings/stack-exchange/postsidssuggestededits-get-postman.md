{
  "info": {
    "name": "Stack Exchange Get Posts Suggested Edits",
    "_postman_id": "c89ec74f-35e9-4953-b548-3ec9d9729fc4",
    "description": "Returns suggsted edits on the posts identified in ids.\n \n - creation - creation_date\n - approval - approval_date\n - rejection - rejection_date\n  creation is the default sort.\n \n {ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n \nThis method returns a list of suggested-edits.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "posts",
      "item": [
        {
          "id": "6bf1f1b0-3c11-43f2-861b-fe64d811f4ee",
          "name": "returns-suggsted-edits-on-the-posts-identified-in-ids---creation--creation-date--approval--approval-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:ids/suggested-edits"
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
            "description": "Returns suggsted edits on the posts identified in ids"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "031d7500-9498-47d8-a1fa-e4e63e9d8b70"
            }
          ]
        }
      ]
    }
  ]
}