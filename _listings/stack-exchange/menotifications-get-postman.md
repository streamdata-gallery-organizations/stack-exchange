{
  "info": {
    "name": "Stack Exchange My Notiications",
    "_postman_id": "6d4ca196-8da6-43df-93cf-6c59ee935cc6",
    "description": "Returns a user's notifications, given an access_token.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "notifications",
      "item": [
        {
          "id": "9ef5a560-5522-4f9d-805c-090f2f779d93",
          "name": "returns-a-users-notifications-given-an-access-token-this-method-requires-an-access-token-with-a-scop",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/notifications?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's notifications, given an access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01ac0314-f50f-4bfa-9d81-fbe065d4b042"
            }
          ]
        }
      ]
    }
  ]
}