{
  "info": {
    "name": "Stack Exchange Get Notifications",
    "_postman_id": "003f435f-eb95-4528-bfee-67206c9570f4",
    "description": "Returns a user's notifications.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "notifications",
      "item": [
        {
          "id": "4ac8e3d5-1b9c-4d3c-b2c7-6c1d94abd373",
          "name": "returns-a-users-notifications-this-method-requires-an-access-token-with-a-scope-containing-read-inbo",
          "request": {
            "url": "http://api.stackexchange.com/2.2/notifications?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's notifications"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "488ca715-27c7-446e-9963-3d51e42e08ee"
            }
          ]
        }
      ]
    }
  ]
}