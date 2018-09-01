{
  "info": {
    "name": "Stack Exchange My Favorites",
    "_postman_id": "c4892a9c-7bdc-4422-9fcb-369c34b7ca7d",
    "description": "Returns the questions favorites by the user associated with the given access_token.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "favorites",
      "item": [
        {
          "id": "3195de98-df91-42f5-8ea2-19ae0233b34f",
          "name": "returns-the-questions-favorites-by-the-user-associated-with-the-given-access-token-this-method-retur",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/favorites?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions favorites by the user associated with the given access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4964a8de-48d8-4322-bbe6-3415b22bde3d"
            }
          ]
        }
      ]
    }
  ]
}