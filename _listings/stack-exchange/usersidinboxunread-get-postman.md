{
  "info": {
    "name": "Stack Exchange Get User Inbox Unread",
    "_postman_id": "23170c64-ee24-49bd-8493-1cb3a5c1e78e",
    "description": "Returns the unread items in a user's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method is effectively an alias for /inbox/unread. It is provided for consumers who make strong assumptions about operating within the context of a single site rather than the Stack Exchange network as a whole.\n \n{id} can contain a single id, to find it programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of inbox items.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "721488ea-616b-4f77-9758-a668b0ce0868",
          "name": "returns-the-unread-items-in-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containi",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:id/inbox/unread"
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
                  "key": "since",
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
            "description": "Returns the unread items in a user's inbox"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a12da473-51dd-4756-b9ae-0301bfe95dd8"
            }
          ]
        }
      ]
    }
  ]
}