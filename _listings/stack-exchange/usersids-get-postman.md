{
  "info": {
    "name": "Stack Exchange Get User",
    "_postman_id": "cabac2f0-16eb-4a50-8a1d-8cc12fa935f2",
    "description": "Gets the users identified in ids in {ids}.\n \nTypically this method will be called to fetch user profiles when you have obtained user ids from some other source, such as /questions.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this method operate on the follow fields of the user object:\n - reputation - reputation\n - creation - creation_date\n - name - display_name\n - modified - last_modified_date\n  reputation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of users.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "03fe65c1-e577-4b39-a09b-b1aa7f369c9e",
          "name": "gets-the-users-identified-in-ids-in-ids-typically-this-method-will-be-called-to-fetch-user-profiles-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids"
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
            "description": "Gets the users identified in ids in {ids}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18197521-72e9-4de0-87ed-6f2506911e5d"
            }
          ]
        }
      ]
    }
  ]
}