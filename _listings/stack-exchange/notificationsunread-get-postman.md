{
  "info": {
    "name": "Stack Exchange Get Notifications Unread",
    "_postman_id": "ef083f5b-d34d-42af-8401-87a383a9a1f8",
    "description": "Returns a user's unread notifications.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "notifications",
      "item": [
        {
          "id": "38cc36cc-f2a5-4f16-8e92-afd27ff7ab22",
          "name": "returns-a-users-unread-notifications-this-method-requires-an-access-token-with-a-scope-containing-re",
          "request": {
            "url": "http://api.stackexchange.com/2.2/notifications/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's unread notifications"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cca10ac1-b4af-47a6-bbec-804e20cf11b2"
            }
          ]
        }
      ]
    }
  ]
}