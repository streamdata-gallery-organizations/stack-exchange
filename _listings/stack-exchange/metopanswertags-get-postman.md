{
  "info": {
    "name": "Stack Exchange My Top Answer Tags",
    "_postman_id": "6d080534-b7fb-4d6f-beec-84adf2785782",
    "description": "Returns the user identified by access_token's top 30 tags by answer score.\n \nThis method returns a list of top tag objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "1cb5ce77-6c78-408b-8781-f6c92371e937",
          "name": "returns-the-user-identified-by-access-tokens-top-30-tags-by-answer-score-this-method-returns-a-list-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/top-answer-tags?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user identified by access_token's top 30 tags by answer score"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d421a0f0-410e-4e68-991d-e122c2e473ad"
            }
          ]
        }
      ]
    }
  ]
}