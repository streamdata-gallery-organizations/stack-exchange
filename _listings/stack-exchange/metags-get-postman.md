{
  "info": {
    "name": "Stack Exchange My Tags",
    "_postman_id": "efabee92-9dbf-4ff5-ad38-979933f48436",
    "description": "Returns the tags the user identified by the access_token passed is active in.\n \nThis method returns a list of tags.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "1aaaccd0-4dea-4a87-860a-1f188a8160d2",
          "name": "returns-the-tags-the-user-identified-by-the-access-token-passed-is-active-in-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/tags?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the tags the user identified by the access_token passed is active in"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "291173a0-2397-49a8-ad0f-9f5d32efc1ac"
            }
          ]
        }
      ]
    }
  ]
}