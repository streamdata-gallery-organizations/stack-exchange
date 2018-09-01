{
  "info": {
    "name": "Stack Exchange Get User Tags",
    "_postman_id": "3dfc0ca5-c7d3-4cf2-b4db-06ae4c4fa336",
    "description": "Returns the tags the users identified in {ids} have been active in.\n \nThis route corresponds roughly to user's stats tab, but does not include tag scores. A subset of tag scores are available (on a single user basis) in /users/{id}/top-answer-tags and /users/{id}/top-question-tags.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this method operate on the follow fields of the tag object:\n - popular - count\n - activity - the creation_date of the last question asked with the tag\n - name - name\n  popular is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of tags.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "8d59f6c9-ab40-44e9-bd5b-2e4932e8de0e",
          "name": "returns-the-tags-the-users-identified-in-ids-have-been-active-in-this-route-corresponds-roughly-to-u",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/tags"
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
            "description": "Returns the tags the users identified in {ids} have been active in"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56886839-cabc-44fe-828f-dadc59622c66"
            }
          ]
        }
      ]
    }
  ]
}