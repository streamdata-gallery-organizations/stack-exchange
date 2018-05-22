{
  "info": {
    "name": "Stack Exchange Get User Top Question Tags",
    "_postman_id": "4285f32c-7b65-444e-8cc7-219d4097a826",
    "description": "Returns a single user's top tags by question score.\n \nThis a subset of the data returned on a user's tags tab.\n \n{id} can contain a single id, to find it programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of top_tag objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "74fedce3-e9a2-4858-9230-e5e2ef545124",
          "name": "returns-a-single-users-top-tags-by-question-score-this-a-subset-of-the-data-returned-on-a-users-tags",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:id/top-question-tags"
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
            "description": "Returns a single user's top tags by question score"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90ff3386-7f19-4ee1-bb2a-924f61038444"
            }
          ]
        }
      ]
    }
  ]
}