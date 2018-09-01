{
  "info": {
    "name": "Stack Exchange Edit Comment",
    "_postman_id": "9bb018ba-71de-4cf7-8749-e29c446c93a8",
    "description": "Edit an existing comment.\n \nUse an access_token with write_access to edit an existing comment.\n \nThis method return the created comment.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "comments",
      "item": [
        {
          "id": "cd671287-78e0-41c6-ba05-9e671c986b76",
          "name": "edit-an-existing-comment-use-an-access-token-with-write-access-to-edit-an-existing-comment-this-meth",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:id/edit"
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
            "description": "Edit an existing comment"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2892b031-4eb5-4685-83fa-66e07b4816c8"
            }
          ]
        }
      ]
    }
  ]
}