{
  "info": {
    "name": "Stack Exchange Suggested Edits",
    "_postman_id": "b448b728-0560-4d4d-899d-03a0105529ac",
    "description": "Returns the suggested edits the user identified by access_token has submitted.\n \nThis method returns a list of suggested-edits.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "suggested edits",
      "item": [
        {
          "id": "e7bb60d3-e544-4906-a682-c885cea1dc4d",
          "name": "returns-the-suggested-edits-the-user-identified-by-access-token-has-submitted-this-method-returns-a-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/suggested-edits?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the suggested edits the user identified by access_token has submitted"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2a398e8b-80ba-4a68-b3fa-04d8945713da"
            }
          ]
        }
      ]
    }
  ]
}