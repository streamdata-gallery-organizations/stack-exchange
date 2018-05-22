{
  "info": {
    "name": "Stack Exchange My Top Question Tags",
    "_postman_id": "ee990ced-b02b-4610-9764-3c6ff65e8c93",
    "description": "Returns the user identified by access_token's top 30 tags by question score.\n \nThis method returns a list of top tag objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "a2af657d-54ba-4355-92d6-785d47ff0cf8",
          "name": "returns-the-user-identified-by-access-tokens-top-30-tags-by-question-score-this-method-returns-a-lis",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/top-question-tags?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user identified by access_token's top 30 tags by question score"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "841f4d48-67ef-4226-a46f-712c1748b129"
            }
          ]
        }
      ]
    }
  ]
}