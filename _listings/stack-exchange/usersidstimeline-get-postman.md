{
  "info": {
    "name": "Stack Exchange Get User Timeline",
    "_postman_id": "bf0a1136-ca13-4445-9643-40144d626e52",
    "description": "Returns a subset of the actions the users in {ids} have taken on the site.\n \nThis method returns users' posts, edits, and earned badges in the order they were accomplished. It is possible to filter to just a window of activity using the fromdate and todate parameters.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of user timeline objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "e755d394-4509-4e81-ab2a-833824873bf5",
          "name": "returns-a-subset-of-the-actions-the-users-in-ids-have-taken-on-the-site-this-method-returns-users-po",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/timeline"
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
            "description": "Returns a subset of the actions the users in {ids} have taken on the site"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "64ab6282-b3d8-4585-af36-65c5499b2694"
            }
          ]
        }
      ]
    }
  ]
}