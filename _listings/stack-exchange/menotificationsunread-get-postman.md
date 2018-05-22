{
  "info": {
    "name": "Stack Exchange My Notiications Unread",
    "_postman_id": "5c84dd59-0632-491e-b782-c66f14cad2f9",
    "description": "Returns a user's unread notifications, given an access_token.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "notifications",
      "item": [
        {
          "id": "2d31f418-2079-4d8e-9385-fe65434e668f",
          "name": "returns-a-users-unread-notifications-given-an-access-token-this-method-requires-an-access-token-with",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/notifications/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's unread notifications, given an access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bb370760-ce5b-4054-90e4-e079874ff88d"
            }
          ]
        }
      ]
    }
  ]
}