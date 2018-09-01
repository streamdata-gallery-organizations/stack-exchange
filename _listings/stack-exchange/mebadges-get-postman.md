{
  "info": {
    "name": "Stack Exchange My Badges",
    "_postman_id": "f6f746d9-b9b8-4ae0-b55e-0c131cd3599a",
    "description": "Returns the badges earned by the user associated with the given access_token.\n \nThis method returns a list of badges.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "badges",
      "item": [
        {
          "id": "7b9d8d04-ce38-4484-a5ee-563b5153d557",
          "name": "returns-the-badges-earned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/badges?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the badges earned by the user associated with the given access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b94f2a38-3210-40b7-92e0-d03b556acd27"
            }
          ]
        }
      ]
    }
  ]
}