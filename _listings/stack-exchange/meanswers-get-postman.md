{
  "info": {
    "name": "Stack Exchange",
    "_postman_id": "e73002b0-10ba-4452-839e-e13a07714a4f",
    "description": "Stack Exchange is a network of 130+ Q&amp;A communities including Stack Overflow.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "answers",
      "item": [
        {
          "id": "b73bc4e1-1af4-49f5-ae93-9e0218c973d5",
          "name": "returns-the-answers-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the answers owned by the user associated with the given access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72ae7104-54da-43fd-b69f-3dd1dc10c32f"
            }
          ]
        }
      ]
    }
  ]
}