{
  "info": {
    "name": "Stack Exchange Get User Top Answers Tags",
    "_postman_id": "944a7d5a-d818-4867-ab75-b01c2bacabbd",
    "description": "Returns a single user's top tags by answer score.\n \nThis a subset of the data returned on a user's tags tab.\n \n{id} can contain a single id, to find it programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of top_tag objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "aef2ca6b-d1fe-4d21-94ef-c6407413b565",
          "name": "returns-a-single-users-top-tags-by-answer-score-this-a-subset-of-the-data-returned-on-a-users-tags-t",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:id/top-answer-tags"
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
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a single user's top tags by answer score"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec371cf2-bdbe-4f5d-bfa6-3b7477161849"
            }
          ]
        }
      ]
    }
  ]
}