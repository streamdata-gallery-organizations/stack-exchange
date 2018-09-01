{
  "info": {
    "name": "Stack Exchange Get User Inbox",
    "_postman_id": "9a0df7ce-feeb-4a29-b69d-549ca380a16f",
    "description": "Returns a user's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method is effectively an alias for /inbox. It is provided for consumers who make strong assumptions about operating within the context of a single site rather than the Stack Exchange network as a whole.\n \n{id} can contain a single id, to find it programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of inbox items.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "59b0bf85-6806-4d2c-be88-98720f6adb4a",
          "name": "returns-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containing-read-inbox-this-m",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:id/inbox"
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
            "description": "Returns a user's inbox"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8725ca96-1cee-4d25-ad84-3486eac8dd0b"
            }
          ]
        }
      ]
    }
  ]
}