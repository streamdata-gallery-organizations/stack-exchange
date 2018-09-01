{
  "info": {
    "name": "Stack Exchange Add Comment Post",
    "_postman_id": "c1590b4b-75f1-434d-bbe3-17b1cd4e6c9a",
    "description": "Create a new comment.\n \nUse an access_token with write_access to create a new comment on a post.\n \nThis method returns the created comment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "posts",
      "item": [
        {
          "id": "0f5c4139-3492-4d4a-a81e-23a7df3e0d9a",
          "name": "create-a-new-comment-use-an-access-token-with-write-access-to-create-a-new-comment-on-a-post-this-me",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:id/comments/add"
              ],
              "query": [
                {
                  "key": "body",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "key": "preview",
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Create a new comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b63521ec-d8cc-4d19-8c8a-fdf0d0af95f7"
            }
          ]
        }
      ]
    }
  ]
}