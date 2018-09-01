{
  "info": {
    "name": "Stack Exchange My Timeline",
    "_postman_id": "96b85204-4d8c-4da7-a21a-ca976497191d",
    "description": "Returns a subset of the actions the user identified by the passed access_token has taken on the site.\n \nThis method returns a list of user timeline objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "ffd124b8-cc48-4061-82f3-03c476be9dae",
          "name": "returns-a-subset-of-the-actions-the-user-identified-by-the-passed-access-token-has-taken-on-the-site",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/timeline?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a subset of the actions the user identified by the passed access_token has taken on the site"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c84a2803-1604-4d2a-9fec-7d3b9ce9bc76"
            }
          ]
        }
      ]
    }
  ]
}