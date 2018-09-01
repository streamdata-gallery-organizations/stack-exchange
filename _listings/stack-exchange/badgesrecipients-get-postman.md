{
  "info": {
    "name": "Stack Exchange Get Badge Recipients",
    "_postman_id": "f7b83f04-e3c4-49e3-ab13-7f9cca7f839d",
    "description": "Returns recently awarded badges in the system.\n \nAs these badges have been awarded, they will have the badge.user property set.\n \nThis method returns a list of badges.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "badges",
      "item": [
        {
          "id": "0c6aba53-59b1-42a9-97ae-c092a1b6594a",
          "name": "returns-recently-awarded-badges-in-the-system-as-these-badges-have-been-awarded-they-will-have-the-b",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/recipients?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns recently awarded badges in the system"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f0a1ebd-b85e-4d38-9e11-daa328c46ed4"
            }
          ]
        }
      ]
    }
  ]
}