{
  "info": {
    "name": "Stack Exchange My Comments",
    "_postman_id": "1292603b-c86c-4fff-9128-049da00b43cc",
    "description": "Returns the comments owned by the user associated with the given access_token.\n \nThis method returns a list of comments.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "comments",
      "item": [
        {
          "id": "f46e7467-b478-4188-b20c-ce85f18e8a35",
          "name": "returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/comments?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments owned by the user associated with the given access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "27ea222d-1ade-45e7-bb6b-8eb5ce377c18"
            }
          ]
        }
      ]
    }
  ]
}